---
layout: default
title: ALMA
parent: Telescopes Tips
grand_parent: To my students
nav_order: 3
---

### If this is your first time

If you are my postdoc, and if you need me to revise English or double check the technical setup, forward me your first draft at least **2 weeks** ahead of the proposal deadline.
{: .fs-1 }

If you are my student, forward me your first draft at least **4 weeks** ahead of the proposal deadline. I will spend time iterating with you many times for education purposes.
{: .fs-1 }

If you are my student/postdoc and if you are not a native English speaker, use [Grammarly](https://www.grammarly.com/) and/or [chatGPT](https://openai.com/blog/chatgpt) to at least remove the typos and basic grammatical errors.
{: .fs-1 }

### 1. Proposing

#### 1.1 Timeline and interface

##### 1.1.1 Proposal deadline
**There is only one proposal deadline every year. It is normally in late April or early May but please pay attention to the call for proposals.** The observing cycle starts in the same October/November of the year and last for a year.
{: .fs-2 }

##### 1.1.2 Capability

The ALMA array is routinely being upgraded. Therefore, the array capability varies from cycle to cycle.
{: .fs-2 }

In addition, in a cycle (i.e., a year's observations), ALMA may optimize its array configuration schedule either for high angular resolution observations (e.g., mostly in the spatially compact array configurations) or for high-frequency or sensitive line observations (e.g., mostly in the spatially extended array configurations). It will likely focus on the extended array configuration in Cycle-10 (late 2023 to late 2024), focus on the compact array configurations in Cycle-11, focus on the extended array configurations in Cycle-12, and so on. Therefore, you need to plan ahead your experiment and make sure you do not miss the deadline (otherwise, you can only come back to propose the same experiment after 2 years).

The exact capability of a cycle and the array configuration schedule is announced a month ahead of the proposal deadline. You can check them through the [Proposer's Guide](https://almascience.nao.ac.jp/proposing/proposers-guide) and [Technical Handbook](https://almascience.nao.ac.jp/proposing/technical-handbook) (Please change to the edition that is relevant to your proposal. The guides for the previous cycle is not totally usable.)
{: .fs-2 }

If you are an advanced user, you may find that the information in the Proposer's Guide or Technical Handbook imprecise, incorrect, or incomprehensive (e.g., prior to Cycle-9, the technical handbook stated that the absolute flux errors are X% without specifying that the X% refers to 2-sigma error, which is unconventional; before 2016, the alignments of the XX and YY receivers had been incorrectly documented.) This sometimes leads to incorrect proposal-preparation, proposal-review, and seriously incorrect journal publications. If you spot such issues, or if you are confused, please do reflect to the [Helpdesk](https://almascience.nao.ac.jp/help) ASAP with **no hesitation and no excuse for any delay. It can really make your proposal reviewed incorrectly and rejected unnecessarily.**
{: .fs-2 }

##### 1.1.2 Interfaces

To submit a proposal, you need an accoun ton the [ALMA User Portal](https://almascience.nao.ac.jp/) (there are mirror sites at NA, EA, and EU. Please choose according to your present affiliation or al). Then you need to download the GUI tool,
[ALMA-OT](https://almascience.nao.ac.jp/proposing/observing-tool/installer-page). ALMA-OT allows you to prepare your proposal offline, while you can also link to your ALMA-OT account which is required when you are submitting and updating a proposal. **Register the account and download the latest version of ALMA-OT if you have not. You should do this before reading into the remaining sections.**
{: .fs-2 }

 **Try to be familiarize with all the GUI tools/interface as early as possible. There are lots of technical details. You do not want to be confused just ahead of your submission.**
{: .fs-2 }


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

This procedure first list the details of the observations using the CASA **listobs()** task. Then it plots the visibility amplitudes versus spectral channels using the CASA **plotms()** task to allow visually inspecting whether or not there are strong emission/absorption lines in our passband (note that the visibility amplitudes are positively definite and therefore the absorption lines will also appear as positive peaks). Then it runs the inverse Fourier transform and deconvolution using the CASA **tclean()** task, and then corrects the [primary beam response function](https://baobabyoo.github.io/pages/students_topics/AstroBasic_RadioInterferometer.html#how-a-radio-interferometer-look-like) using the **impbcor** task. Here you have to carefully understand the parameters/keywords in the tclean task to be able to use it properly; they need to be optimized case-by-case. For example, in tclean(), we use the keyword `specmode   =  'mfs'` to produce a continuum image using the aggregated bandwidth provided by all (selected) spectral channels. For imaging the observations on a single field, we can use `gridder  =  'standard'`; to image the Stokes I mosaic observations (i.e., an image made with multiple antennae pointings), we have to use `gridder  =  'mosaicft'`; to image the full polarization mosaic observations, we have to use `gridder  =  'awprojectft'`.
{: .fs-2 }

Finally, this procedure uses the CASA **exportfits()** task to export the results of imaging to the FITS format binary files.
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

Below is the procedure:
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

The procedure to perform spectral line imaging is not too different from that of the continuum imaging. A major difference is that we need to use other `specmode` options in the CASA **tclean()** task. In addition, you may want to reset the **rest-frequency** to conveniently make the velocity gridding. You can look up the rest frequency of most of the molecular transitions that you might be interested in on the [Splatologue](https://splatalogue.online//) webpage. In addition, before running CASA **tclean()**, we usually (which is not always necessary, depending on your science case) visually inspect the visibility spectra using the CASA **plotms()** task, and separate the continuum and line emission using the CASA **uvcontsub()** task.
{: .fs-2 }

```
import os

##### flow control #######################################
thesteps = []
step_title = {
                0: 'List observational details',
                1: 'Inspecting spectrum',
                2: 'Separating continuum and line',
                3: 'Perform imaging',
                4: 'Primary beam correction',
                5: 'exporting FITS image'
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
filename = 'nh3'
fields    = ['l429']
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

    fitspec = {
               '0': {'0': {'chan': '111~283;356~444;512~591;662~851', 'fitorder': 0} }
              }

    linems = filename + '_contsub.ms'
    os.system('rm -rf ' + linems)
    uvcontsub(
              vis        = filename + '.ms',
              outputvis  = linems,
              fitspec    = fitspec, # check the help file with 'CASA> help uvcontsub' to see how to set this
              datacolumn = 'data',
              writemodel = False
             )


mystep = 3
if(mystep in thesteps):
    print ('Step ', mystep, step_title[mystep])

    linems = filename + '_contsub.ms'
    for stoke in stokes:
        for field in fields:

            imagename = field + '_' + stoke
            os.system('rm -rf ' + imagename + '.*')
            tclean( vis   = linems,
                    selectdata = True,
                        field = field,
                        spw   = '0',
                    datacolumn = 'data',
                    imagename  = imagename,
                    cell       = ['0.5arcsec'], imsize = [300,300],
                    stokes     = stoke,
                    specmode   = 'cube',  # Spectral line imaging with one or more channels
                        nchan = 200,
                        start = 400,
                        width = 1,
                        outframe = 'LSRK', # reference system of velocity (LSRK: local standard of rest system)
                        veltype  = 'radio',
                        restfreq = ['23.69449550GHz'],   # rest frequency of the NH3 hyperfine inversion line
                        interpolation = 'linear',
                    gridder    = 'standard',
                    pblimit    = 0.2,
                    deconvolver = 'hogbom',
                    weighting   = 'briggs',
                        robust  = 2.0,
                    restoringbeam =    'common',
                    niter      = 0,
                    interactive = interactive,
                    restart     = True,
                    threshold = '5e-3Jy'
              )


mystep = 4
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

mystep = 5
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
