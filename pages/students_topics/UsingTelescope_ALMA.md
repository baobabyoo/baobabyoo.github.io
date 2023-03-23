---
layout: default
title: ALMA
parent: Telescopes Tips
grand_parent: To my students
nav_order: 3
---

(under construction)


### 4. Data calibration and imaging

#### 4.1 Software

The official software package for processing ALMA data is the [CASA software package](https://casa.nrao.edu/).
{: .fs-2 }

You can try using the previewer [CARTA](https://cartavis.org/) which can open very large (TB size) image files very quickly/smoothly.
{: .fs-2 }

To install CASA, download the tarballs of its binary release from [here](https://casa.nrao.edu/casa_obtaining.shtml). Uncompress the tarball in linux using the linux command, e.g.,
{: .fs-2 }

```
tar -xvf casa-6.5.3-28-py3.8.tar.xz
```
{: .fs-2 }

Then `cd` into the *bin* directory under the uncompressed folder and then use the `pwd` command of linux to find the absolute path, e.g.,
{: .fs-2 }

```
cd ./casa-6.5.3-28-py3.8/bin
pwd
```
{: .fs-2 }

The return may look like `/home/hyliu/softwares/casa-6.5.3-28-py3.8/bin`. Open another terminal and open your startup shell script, for example, using *vim*, `vim ~/.bashrc` (in Mackbook, it may be `vim ~/.bashrc_profile`, also I have never successfully launch CASA with the M1/M2 chip Mac). Add the following line into the startup shell, for example:
{: .fs-2 }

```
alias casa653='/home/hyliu/softwares/casa-6.5.3-28-py3.8/bin/casa'
```
{: .fs-2 }

Then when you open another new terminal, you can launch the CASA interface by typing `casa653` (i.e., the alias you set when editing the startup shell script).
{: .fs-2 }

Note that with CentOS9 (a free linux distribution that is similar to Redhat), you may not be able to launch CASA successfully due to missing the library *libnsl.so.1*. If you have access to the *root* or *administrator* account(s) on your linux machine, you can install this package by typing:
{: .fs-2 }

```
sudo yum install libnsl
```
After this you should be able to launch CASA 6.
{: .fs-2 }

#### 4.2 Simple imaging scripts

##### 4.2.1 Continuum imaging (with flow control)

This procedure first list the details of the observations using the CASA **listobs()** task. Then it plots the visibility amplitudes versus spectral channels using the CASA **plotms()** task to allow visually inspecting whether or not there are strong emission/absorption lines in our passband (note that the visibility amplitudes are positively definite and therefore the absorption lines will also appear as positive peaks). Then it runs the inverse Fourier transform and deconvolution using the CASA **tclean()** task, and then corrects the [primary beam response function](https://baobabyoo.github.io/pages/students_topics/AstroBasic_RadioInterferometer.html#how-a-radio-interferometer-look-like) using the **impbcor** task. Here you have to carefully understand the parameters/keywords in the tclean task to be able to use it properly; they need to be optimized case-by-case. Finally, it uses the CASA **exportfits()** task to export the results of imaging to the FITS format binary files.
{: .fs-2 }

You can copy the content of this script to an ASCII file, e.g., imaging.py. To run the script from begin to end, in the CASA ipython interface, enter
{: .fs-2 }

```
CASA> execfile('imaging.py')
```
{: .fs-2 }

To execute one or a few steps at a time, try something like the following:
{: .fs-2 }

```
CASA> mysteps = [1,2]
CASA> execfile('imaging.py')
```
{: .fs-2 }
```
CASA> mysteps = [3]
CASA> execfile('imaging.py')
```
{: .fs-2 }

```
import os
# using the data taken from https://casaguides.nrao.edu/index.php/First_Look_at_Imaging
# To uncompress .tgz file, e.g.,
#    tar -zxvf file.tgz
# To uncompress .tar file
#    tar -xvf file.tar
#
# To load a CASA task, e.g.,
#   CASA> tget task_name
# To check helpfile
#   CASA> help task_name
#
# To execute a script in CASA ipython interface
#   CASA> execfile('script.py')

##### flow control #######################################
thesteps = []
step_title = {
                0: 'List observational details',
                1: 'Inspecting spectrum',
                2: 'Perform imaging',
                3: 'Primary beam correction',
                4: 'exporting FITS image'
             }

try:
  print ('List of steps to be executed ...', mysteps)
  thesteps = mysteps
except:
  print ('global variable mysteps not set.')
if (thesteps==[]):
  thesteps = range(0,len(step_title))
  print ('Executing all steps: ', thesteps)
##########################################################

##### Setup parameters ###################################
filename = 'sis14_twhya_selfcal'
fields    = ['3c279']
stokes    = ['I']
interactive = True
dropdeg     = True
##########################################################

mystep = 0
if(mystep in thesteps):
    print ('Step ', mystep, step_title[mystep])

    os.system('rm -rf ' + filename + '.listobs')
    listobs(vis = filename + '.ms',
            listfile = filename + '.listobs'
           )


mystep = 1
if(mystep in thesteps):
    print ('Step ', mystep, step_title[mystep])

    for field in fields:
        outfig = filename + '_' + field + '.spectrum.png'
        os.system('rm -rf ' + outfig)
        plotms( vis   = filename + '.ms',
                xaxis = 'channel', yaxis = 'amplitude',
                field = field,
                coloraxis = 'antenna1',
                plotfile  = outfig
              )


mystep = 2
if(mystep in thesteps):
    print ('Step ', mystep, step_title[mystep])

    for stoke in stokes:
        for field in fields:

            imagename = field + '_' + stoke
            os.system('rm -rf ' + imagename + '.*')
            tclean( vis   = filename + '.ms',
                    selectdata = True,
                        field = field,
                        spw   = '0',
                    datacolumn = 'corrected',
                    imagename  = imagename,
                    cell       = ['0.1arcsec'], imsize = [300,300],
                    stokes     = stoke,
                    specmode   = 'mfs',  # multi-freqency synthesis continuum imaging
                    gridder    = 'standard',
                    pblimit    = 0.2,
                    deconvolver = 'hogbom',
                    weighting   = 'briggs',
                        robust  = 2.0,
                    niter      = 10000,
                    interactive = interactive,
                    restart     = True,
                    threshold = '0.1Jy'
              )


mystep = 3
if(mystep in thesteps):
    print ('Step ', mystep, step_title[mystep])


    for stoke in stokes:
        for field in fields:

            imagename = field + '_' + stoke
            outfile   = field + '_' + stoke + '.pbcor.image'
            os.system('rm -rf ' + outfile)
            impbcor(imagename = imagename + '.image',
                    pbimage   = imagename + '.pb',
                    outfile   = outfile
                   )

mystep = 3
if(mystep in thesteps):
    print ('Step ', mystep, step_title[mystep])


    for stoke in stokes:
        for field in fields:

            imagename = field + '_' + stoke
            suffixes  = ['.image', '.pbcor.image']
            for suffix in suffixes:
                exportfits(
                            imagename = imagename + suffix,
                            fitsimage = imagename + suffix + '.fits',
                            overwrite = True,
                            dropdeg   = dropdeg
                          )
```
{: .fs-2 }


##### 4.2.2 Spectral line imaging (with flow control)
