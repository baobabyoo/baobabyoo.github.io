---
layout: default
title: Polarization images
parent: Software Tips
grand_parent: To my students
nav_order: 1
---

### 1. Creating polarization images using CASA

If you need more explanation, you can also read into this [CASA Guide](https://casaguides.nrao.edu/index.php?title=3C286_Band6Pol_Imaging_for_CASA_5.4) and scroll down to the section *Constructing Polarization Intensity and Angle Images*.
{: .fs-2 }

Once you have created Stokes I, Q, and U images, you can try the following CASA scripts. I sometimes use it to produce quicklook polarization intensity (PI), polarization percentage (Per), and polarization position angle (PA) images. The input images have to be in CASA image format. If you only have FITS images, you need to first import them to CASA. You can find some instruction about importing in [this page](https://baobabyoo.github.io/pages/students_topics/software_tips_FITS.html).
{: .fs-2 }

Usually, I create the PI, Per, and PA images using the Stokes I, Q, and U images without primary beam corrections. This makes it easier to set a noise threshold (i.e., ignoring the pixels that the values are below that threshold). We need to remember to perform primary beam correction for the Stokes I, Q, U, and PI images using the CASA task `impbcor` before making other quantitative analyses. 
{: .fs-2 }

```
mystep = 1
if(mystep in thesteps):
  casalog.post('Step '+str(mystep)+' '+step_title[mystep],'INFO')
  print 'Step ', mystep, step_title[mystep]

  stokes      = 'I'
  Iimagename   = '%s.rob%s.%s.image.tt0'%(outname, str(robust), stokes)
  stokes      = 'Q'
  Qimagename   = '%s.rob%s.%s.image.tt0'%(outname, str(robust), stokes)
  stokes      = 'U'
  Uimagename   = '%s.rob%s.%s.image.tt0'%(outname, str(robust), stokes)
  stokes      = 'V'
  Vimagename   = '%s.rob%s.%s.image.tt0'%(outname, str(robust), stokes)
  stokes      = 'PI'
  PIimagename   = '%s.rob%s.%s.image.tt0'%(outname, str(robust), stokes)
  stokes      = 'Per'
  Perimagename   = '%s.rob%s.%s.image.tt0'%(outname, str(robust), stokes)
  stokes      = 'PA'
  PAimagename   = '%s.rob%s.%s.image.tt0'%(outname, str(robust), stokes)


  # generate the linear polarization intensity image
  command = 'rm -rf ' + PIimagename
  os.system(command)
  mode = 'poli'
  imagename = [Qimagename, Uimagename]
  sigma     = '0.000027Jy/beam'
  immath(
         outfile=PIimagename,
         mode=mode,
         imagename=imagename,
         sigma=sigma
        )

  # derive the polarization position angle
  command = 'rm -rf ' + PAimagename
  os.system(command)
  mode = 'pola'
  imagename = [Qimagename, Uimagename]
  mask      = PIimagename + '>' + '0.0'
  immath(
         outfile=PAimagename,
         mode=mode,
         imagename=imagename,
#         mask=mask
        )

  # derive polarization percentage
  command = 'rm -rf ' + Perimagename
  os.system(command)
  mode  = 'evalexpr'
  expr  = 'IM0/IM1'
  imagename = [PIimagename, Iimagename]
  immath(
         outfile=Perimagename,
         mode=mode,
         imagename=imagename,
         expr=expr,
         mask=mask
        )
```
{: .fs-1 }



### 2. Creating polarization images using Miriad

Here I provide a Miriad script that I often adopt to create polarization PI, Per, and PA images. It first imports FITS images to Miriad format and then derives the polarization quantities with the `impol` Miriad task.
{: .fs-2 }

```
#!/bin/bash
  


filehead='G31p4_Qband_D.rob2'
fileend='image.tt0'
Stokes='I Q U'
for stoke in $Stokes
  do
    inname=$filehead.$stoke.$fileend'.fits'
    outname=$filehead.$stoke.$fileend'.miriad'
    rm -rf $outname
    echo 'importing '$inname
    fits in=$inname op=xyin out=$outname
  done


# evaluating polarization images
poli=$filehead'.PI.'$fileend'.miriad'
polm=$filehead'.Per.'$fileend'.miriad'
pa=$filehead'.PA.'$fileend'.miriad'

for file in $poli $polm $pa
  do
    rm -rf $file
  done


# derive polarization images (Stokes I, Q, U stddev: 27e-6 Jy)
QUIimg='G31p4_Qband_D.rob2.Q.image.tt0.miriad,G31p4_Qband_D.rob2.U.image.tt0.miriad,G31p4_Qband_D.rob2.I.image.tt0.miriad'
impol in=$QUIimg sigma=0.000050,0.000050 sncut=3,20 poli=$poli polm=$polm pa=$pa
cgdisp in=$filehead.I.$fileend'.miriad',$poli,$polm,$pa \
       type=c,p,amp,ang device=/xw \
       region='arcsec,box(-5,-5,5,5)' \
       options=full,beambl,wedge,blacklab \
       lines=1,2,4 vecfac=3.5,2 labtyp=hms,dms


# Export FITS image
for file in $poli $polm $pa
  do
    outfitsname=$file'.fits'
    rm -rf $outfitsname
    fits in=$file op=xyout out=$outfitsname
  done
```
{: .fs-1 }

Again, we have to perform primary beam correction before making any quantitative analyses. You can either import the FITS images to CASA and do the primary beam correction using CASA. Or we can do it within Miriad, using the commands like the following:
{: .fs-2 }

```
linmos in=$linename.acamodel.regrid.temp \
       out=$linename.acamodel.regrid.pbcor.temp
```
{: .fs-1 }

This usually works. However, if Miriad does not find the primary beam information correction, you can also manually include it in the header (e.g. ,approximate it with a Gaussian primary beam), for example:
{: .fs-2 }

```
#!/bin/csh

set pbfwhm = (27.327382 27.327382 45.54) # in arcsecond unit
set linerestfreq = 230.53800000 # in GHz unit
 
setheader:

foreach fileid ($fileids)

   set pb = '"gaus('$pbfwhm[$fileid]')"'
   puthd in=$linename'_'$fileid'.uv.miriad'/telescop \
         value='single' \
         type=a

   puthd in=$linename'_'$fileid'.uv.miriad'/pbtype \
         value=$pb \
         type=a

   puthd in=$linename'_'$fileid'.uv.miriad'/restfreq \
         value=$linerestfreq \
         type=d

end
```
{: .fs-1 }


### 3. Plotting

If you are handling the polarization data using Python, especially, if you are creating figures using the [APLpy](https://aplpy.github.io/) package, you will sometimes face a problem that the package(s) you use cannot recognize the Stokes dimension. In this case you can try to import the images to CASA and then drop the dummy dimension(s) when you are exporting back to FITS, for example:
{: .fs-2 }

```
import os
  
path = './'
Imap = path + 'G31p4_Qband_D.rob2.I.image.tt0'
Qmap = path + 'G31p4_Qband_D.rob2.Q.image.tt0'
Umap = path + 'G31p4_Qband_D.rob2.U.image.tt0'
PImap  = path + 'G31p4_Qband_D.rob2.PI.image.tt0.miriad'
pamap  = path + 'G31p4_Qband_D.rob2.PA.image.tt0.miriad'
Permap = path + 'G31p4_Qband_D.rob2.Per.image.tt0.miriad'


for imname in [Imap, PImap, pamap, Permap]:
    importfits(
                fitsimage = imname + '.fits',
                imagename = imname + '.image',
                overwrite = True
               )

    exportfits(
                imagename = imname + '.image',
                fitsimage = imname + '.dropdeg.fits',
                overwrite = True, dropdeg = True, dropstokes = True
              )
```
{: .fs-1 }

I use the following code to plot the polarization line segments (you need to create your own code to define sampling positions). This is a function in a big class. I am reluctant to edit it now. You should be able to more or less know how it works and edit to the way that fits your code the best, given that you are likely already experienced. You can feel free to contact my student, Greta Siu, in case of any problem.
{: .fs-2 }
```
    def plot_segments(self, length_arcsec=-999.0, color=(0,0,0), linestyle='solid', linewidth=2.0, delraperyr_mas=0.0, deldecperyr_mas=0.0, delyr=0.0):
        '''
        Plot the polarization line segments.

        Input :

        length_arc    [float] : Default: 1/3 of the synthesized beam FWHM of the intensity map

        Keywords :
        
        delraperyr_mas    [float] : For correcting proper motions (delta ra per year). Units: mas. Default: 0.0
        deldecperyr_mas   [float] : For correcting proper motions (delta dec per year). Units: mas. Default: 0.0
        delyr             [float] : For correcting proper motions. (date-to-go-to minus data-of-observation)

        '''

        delra_deg  = delraperyr_mas  * delyr * 0.001 / 3600.0
        deldec_deg = deldecperyr_mas * delyr * 0.001 / 3600.0
        delra_pix  = delra_deg  / self.cdelt1
        deldec_pix = deldec_deg / self.cdelt2


        if (length_arcsec == -999.0):
            length_arcsec = ( np.sqrt( self.bmaj * self.bmin ) * 3600.0 ) / 3.0

        halflength_pix = 0.5 * length_arcsec / (self.cdelt2 * 3600.0)

        for i in range(0, self.num_samplings):

            xpix = int(round(self.xpixgrid_list[i] ))
            ypix = int(round(self.ypixgrid_list[i] ))

            pa = self.paimage[ypix][xpix]

            xbeg = self.xpixgrid_list[i] + delra_pix  - halflength_pix * np.sin( np.pi * (pa/180.0) )
            ybeg = self.ypixgrid_list[i] + deldec_pix + halflength_pix * np.cos( np.pi * (pa/180.0) )
            xend = self.xpixgrid_list[i] + delra_pix  + halflength_pix * np.sin( np.pi * (pa/180.0) )
            yend = self.ypixgrid_list[i] + deldec_pix - halflength_pix * np.cos( np.pi * (pa/180.0) )

            world1 = self.hduwcs.wcs_pix2world([ [ xbeg, ybeg ] ], 0)
            world2 = self.hduwcs.wcs_pix2world([ [ xend, yend ] ], 0)

            linelist = [np.array([
                                  [  world1[0][0], world2[0][0]  ],
                                  [  world1[0][1], world2[0][1]  ]
                                 ])]

            if ( np.isfinite(pa) == True ):
                self.fig.show_lines(linelist,
                                    color=color, linestyle=linestyle, linewidth=linewidth)
```
{: .fs-1 }
