---
layout: default
title: FITS images
parent: Software Tips
grand_parent: To my students
nav_order: 1
---

### What are FITS images?

FITS stands for Flexible Image Transport System. The complete documentation can be found on this [webpage](https://fits.gsfc.nasa.gov/fits_documentation.html) hosted by NASA. 
{: .fs-2 }

In brief, FITS is a binary format to store astronomical data (either image(s) or certain types of table(s)). The reason why we need it is that our files are usually huge, making the ASCII format impractical. In addition, there usually needs some meta-data to explain how the data were taken and were processed (e.g., the angular resolution or spectral resolution of the image(s) stored in a specific FITS file, the date of the observations, etc), such that the data file can be self-contained without depending on external documentation. 
{: .fs-2 }

In light of this, a FITS file usually contains two parts:
- one or more binary **data table**
- one or more **header files** that contain the necessary information to understand the data.
{: .fs-2 }

Since the binary data are not human readable, we cannot handle the FITS files with a text editor (e.g., vim) or other commercial or open resource software like MS Excel or Open Office. Here I provide some simple tips for manipulating FITS images that can be useful to radio astronomers. If you are a graduate student or researcher, I recommend at least installing the [ds9](https://sites.google.com/cfa.harvard.edu/saoimageds9),  [CASA](https://casa.nrao.edu/), [Miriad](https://www.astro.umd.edu/~teuben/miriad/) software and the [Astropy](https://www.astropy.org/) and [APLpy](https://aplpy.github.io/) Python packages. If you have access to IDL, you should also install the [IDL Astronomy User's Library](https://idlastro.gsfc.nasa.gov/).
{: .fs-2 }

If you know something that is very useful, please recommend to me.
{: .fs-2 }


### (Pre)Viewers
The following software may be useful for a quick preview of your FITS images or tables, which are particularly handy during a casual discussion with the other colleagues. The links to them are provided. They are all reasonably easy to install.
{: .fs-2 }

###### ds9
For any astronomer, [ds9](https://sites.google.com/cfa.harvard.edu/saoimageds9) would be one of the most handy FITS image viewers. It is trivial to install no matter whether you are using Linux, Windows, or Mac OSX. There is no reason not using it. After installation, you can launch it by double-clicking its icon, otherwise, by typing
{: .fs-2 }
```
> ds9
```
{: .fs-1 }
in a Linux or OSX comand line. 
{: .fs-2 }

###### fv
[fv](https://heasarc.gsfc.nasa.gov/ftools/fv/) is a simple graphical interface for you to preview FITS tables. It can also export data to ASCII format. It is also very easy to install.
{: .fs-2 }

###### CASA-Viewer and CARTA

If you are a radio astronomer, it is most likely that you have installed the [CASA Software Package](https://casa.nrao.edu/). The `viewer` function of CASA is handy when you are previewing the radio interferometric images, although it crashes once in a while. It may be replaced by [CARTA](https://cartavis.org/) at some point although I have not adapted myself to it. If you are new to astronomy, I recommend beginning with CARTA. When your image file is large (e.g., >100 GB), presently, only CARTA allows you to preview the images reasonably smoothly.
{: .fs-2 }

###### Karma kvis

We used the  [karma](https://www.atnf.csiro.au/computing/software/karma/) package a lot in the old days. The `kvis` function is very useful when you are interactively examining the gas kinematics of an astronomical object with a spectral line image cube. I myself still use it once in a while although not everybody uses it nowadays.
{: .fs-2 }



### Converting images in various formats

###### Miriad
After sourcing the [Miriad](https://www.astro.umd.edu/~teuben/miriad/) software package, which is often used in the imaging of the SMA data, you can use the following commands to convert between the Miriad and FITS format images:
{: .fs-2 }

```
# The file names in in='' and out='' (string variables) 
# need to be replaced with your filenames

# converting from Miriad format to FITS format
fits in='mytarget.image.miriad' op=xyout out='mytarget.image.fits'

# converting from FITS to Miriad format
fits in='mytarget.image.fits' op=xyin out='mytarget.image.miriad'
```
{: .fs-1 }

They can be executed either by directly entering in a Linux/OSX command line or by executing as a BASH or CSH script. We can then program other software languages to manipulate or analyze the FITS format images, such as C/Fortran, IDL, or Python. For online documentation of the Miriad tasks please check the [Miriad task index](https://www.atnf.csiro.au/computing/software/miriad/taskindex.html).
{: .fs-2 }

You can regrid two Miriad images or image cubes to have identical spatial or spectral coordinates using the following command:
{: .fs-2 }
```
# The '\' symbols denotes line-breaking
regrid in='image1.image.miriad'  \
       out='image1.regrided.image.miriad' \
       axes=1,2 \
       tin='image2.image.miriad'
```
{: .fs-1 }

This is useful when you want to align the pixels of two images before any further analyses. In this example, `axes=1,2` means that we are regridding the two spatial axes. When you want to also regrid the spectral axis, you can use `axes=1,2,3`. It loads 'image1.image.miriad' and regrids it according to the header information in 'image2.image.miriad', and then outout the regridded image1 as a new file 'image1.image.miriad'.
{: .fs-2 }

###### CASA

After launching CASA, you can type `viewer` in the CASA command line environment to launch the GUI image previewer.
{: .fs-2 }

You can use the following [CASA Software Package](https://casa.nrao.edu/) commands to convert between the CASA and FITS format images:
{: .fs-2 }

```
# The file names (string variables) in imagename and fitsimage need 
# to be replaced with your filenames.

# converting from CASA format to FITS format
exportfits(
           imagename = 'mytarget.image',
           fitsimage = 'mytarget.image.fits',
           overwrite = True
          )
          
# converting from CASA format to FITS format
importfits(
           imagename = 'mytarget.image',
           fitsimage = 'mytarget.image.fits',
           overwrite = True
          )
          
# If your CASA image have redundant spectral or polarization dimension,
# and if you want to drop those redundant dimension, you can include the
# relevant options (dropstokes or dropdeg) like:
exportfits(
           imagename = 'mytarget.image',
           fitsimage = 'mytarget.image.fits',
           overwrite = True, dropdeg = True, dropstokes = True
          )
# This can be very useful since not all Python package can recognize 
# high-dimensional FITS images.
```
{: .fs-1 }

To crop a sub-image in CASA, you can use the CASA `imsubimage` task like:
{: .fs-2 }
```
# # box[[x1, y1], [x2, y2]] region
subimregion = "box[[1500pix, 1500pix], [4499pix, 4499pix]]"

img_name = 'mytarget'
imsubimage(imagename = img_name + '.image',
           outfile   = img_name + '.subim.image',
           region    = subimregion
          )
```
{: .fs-1 }

We also often use the CASA `imregrid` and `imsmooth` tasks to regrid a set of CASA format images to the same coordiante system and then smooth same synthesized beam size before exporting to FITS files for further analyses. Example of these commands are:
{: .fs-2 }
```
imregrid(
         # name of the image to be regrided
         imagename = imagename,
         # an existing image to serve as a template of coordiante grids
         template  = template_imagename,
         # output filename
         output    = imagename + '.regrid',
         # options in the regridding
         axes      = [0, 1], interpolation = 'linear',
         # whether or not overwritting the output file
         overwrite = True
        )
          
imsmooth(
         # name of the image to be smoothed
         imagename = image,
         # Shape of the smoothing kernel or final synthesized beam.
         # This example specified that the final synthesized beam should
         # be a gaussian beam with 0.53 arcsecond FWHM in the major and minor axes
         kernel    = 'gauss',
             major = '0.53arcsec', minor = '0.53arcsec', pa = '0deg',
             targetres = True,
         # output file name
         outfile   = image + '.smooth', 
         # whether or not overwritting the output file
         overwrite = True
        )
```
{: .fs-1 }

These CASA commands can be executed either by directly entering in a Linux/OSX command line or by executing as a Python3 script. 
{: .fs-2 }

To see a full list of available CASA tasks, please check [this webpage](https://casadocs.readthedocs.io/en/stable/api/casatasks.html). For online documentation of the CASA tasks please check the [CASA docs](https://casa.nrao.edu/casadocs). In the CASA command line, you can also check the documentation and input variables by entering `help taskname` and `inp`, e.g., in this case:
{: .fs-2 }

```
# check the documentation for importfits/exportfits
CASA> help importfits
CASA> help exportfits

# load the task importfits
CASA> tget importfits
# check the input variable of the loaded task
CASA> inp
```
{: .fs-1 }

After obtaining the FITS images, we can then program other software languages to manipulate or analyze the FITS format images, such as C/Fortran, IDL, or Python.
{: .fs-2 }


### Working with FITS using software languages

If you are programming C or Fortran, then [CFITSIO](https://heasarc.gsfc.nasa.gov/fitsio/) is the package you need. I do not think this is the way you will be going but am providing a reference to it just in case (e.g., sometimes you may need to check other people's programs which utilized this package). 
{: .fs-2 }

###### Python

If you are analyzing images, you might build a conda environment by the following Linux/OSX command line commands:
{: .fs-2 }
```
conda create --name astroimgAna python=3.9
pip install --upgrade pip
pip install jupyter
pip install astropy scipy
pip install jupyter matplotlib h5py aplpy pyregion PyAVM healpy
pip install pandas
```
{: .fs-1 }

I often make most of the following imports:
{: .fs-2 }
```
import os
import numpy as np

from astropy.io.fits import getdata
from astropy import wcs
from astropy.io import fits
from astropy import units as u
from astropy import constants as con
from astropy.coordinates import SkyCoord

import matplotlib
import matplotlib.pyplot as plt
import matplotlib as mpl
import matplotlib

import aplpy

matplotlib.use('PDF')
```
{: .fs-1 }

The following code is an example of importing FITS image as a [Header Data Unit ](https://docs.astropy.org/en/stable/io/fits/api/hdus.html) (HDU) and extracting certain header information in Python:
{: .fs-2 }
```
intensitymap = 'mytarget_StokesI.fits'
intensity_scale = 1000.0
if_success = False
try:
  
  # importing FITS image to a HDU
  Ihdu   = fits.open(intensitymap)
  
  # editing the FITS image by multiplying a scaling factor
  Ihdu[0].data = Ihdu[0].data * intensity_scale
  
  if_success = True

except:
  print('Unable to read the intensity FITS image. Please double check the image file.')
  print(intensitymap)

if ( if_success == True ):
  # Reading FITS header
  try:
    naxis1 = Ihdu[0].header['naxis1']
    naxis2 = Ihdu[0].header['naxis2']
    crval1 = Ihdu[0].header['crval1']
    crpix1 = Ihdu[0].header['crpix1']
    cdelt1 = Ihdu[0].header['cdelt1']
    crval2 = Ihdu[0].header['crval2']
    crpix2 = Ihdu[0].header['crpix2']
    cdelt2 = Ihdu[0].header['cdelt2']
    hduwcs = wcs.WCS( Ihdu[0].header)
  except:
    print( 'Warning. No coordinate headers' )

  try:
    bmaj = Ihdu[0].header['bmaj']
    bmin = Ihdu[0].header['bmin']
    bpa  = Ihdu[0].header['bpa']
  except:
    print('Warnning. No header for synthesized beam size')
```
{: .fs-1 }

After having these header information, we can make conversion between the world coordiante system (i.e., astronomical coordinate systems) and the pixel coordinate system using the some methods of [astropy.wcs](https://docs.astropy.org/en/stable/wcs/index.html). The following example convert the central pixel in the image to the R.A. and Decl. values and then convert them back ot the x and y pixel numbers:
{: .fs-2 }
```
xpix_temp = int(round( naxis1/2.0 ))
ypix_temp = int(round( naxis2/2.0 ))

world = hduwcs.wcs_pix2world([ [xpix_temp, ypix_temp] ], 0)
ra_center  = world[0][0]
dec_center = world[0][1]

pixcrd = hduwcs.wcs_world2pix([ [ra_center, dec_center] ], 0)
ra_center_pix  = pixcrd[0][0]
dec_center_pix = pixcrd[0][1]
```
{: .fs-1 }

The value of a certain pixel in a (two dimensional image) is simply:
{: .fs-2 }
```
value = Ihdu[0].data[ypix][xpix]
```
{: .fs-1 }

This allows you to analyze the image, for example, measuring aperature photometry.
{: .fs-2 }

The (two-dimensional) image can be output as a plot using the APLpy commands like:
{: .fs-2 }
```
figsize = [9.0, 9.0]
cmap           = 'viridis'
plot_ticks     = True
tick_font      = 25
tick_ypad      = 0
plot_colorbar  = True
colorbar_location = 'top'
colorbar_width = 0.3
colorbar_pad = 0.3
colorbar_font = 15
colorbar_label = 'Colorbar'
colorbar_labelpad = 0.3
colorbar_labelfont = 20
width = 1.0
height = 1.0
plot_scalebar = True
distance      = 140.0
scalebar_size = 100.0
scalebar_text = '100 au'
scalebar_color = (0,0,0)
scalebar_font = 25.0
scalebar_linewidth = 3.0
plot_beam = True
beam_color = 'black'

if_plot = False
try:
    self.fig = aplpy.FITSFigure(Ihdu, figsize=(figsize[0], figsize[1]))
    if_plot = True

except:
    print('Unable to load or plot hdu. Please double check the image file.')

if ( if_plot == True ):
    vmax = np.nanmax(Ihdu[0].data)*1.2
    vmin = 0.0

    fig.show_colorscale(
                        vmax = vmax, vmin = vmin,
                        interpolation = 'bicubic',
                        cmap = cmap
                       )

# ticks
fig.tick_labels.set_font(size=tick_font)
fig.axis_labels.set_font(size=tick_font)
fig.axis_labels.set_ypad(tick_ypad)
if (plot_ticks != True):
    fig.axis_labels.hide_x()
    fig.axis_labels.hide_y()
    fig.tick_labels.hide_x()
    fig.tick_labels.hide_y()

# recentering
if ( (ra_center != 0) or (dec_center !=0) ):
    print('recentering')
    fig.recenter(ra_center, dec_center, width=width, height=height)

# plot color bar
if (plot_colorbar == True):
    fig.add_colorbar()
    fig.colorbar.show()
    fig.colorbar.set_location(colorbar_location)
    fig.colorbar.set_width(colorbar_width)
    fig.colorbar.set_pad(colorbar_pad)
    fig.colorbar.set_font(size=colorbar_font, weight='medium', \
                               stretch='normal', family='sans-serif', \
                               style='normal', variant='normal')

    fig.colorbar.set_axis_label_text(colorbar_label)
    fig.colorbar.set_axis_label_font(size=colorbar_labelfont)
    fig.colorbar.set_axis_label_pad(colorbar_labelpad)
    
# plot scalebar
if (plot_scalebar == True):

    fig.add_scalebar( scalebar_size * (1.0/distance) / 3600.0)
    fig.scalebar.set_label(scalebar_text)
    fig.scalebar.set_color(scalebar_color)
    fig.scalebar.set_font(size=scalebar_font)
    fig.scalebar.set_linewidth(scalebar_linewidth)
```
{: .fs-1 }

If you would like to overplot another image as contours, try loading as another HDU (e.g., `chdu` in the following example) and complete the commands like:
```
fig.show_contour(chdu, colors=ccolor, linestyles=clinestyle,
                       levels=clevels,
                       linewidths=clinewidth)
```
{: .fs-1 }

Finally, to save an output figure, try ty complete the command like:
{: .fs-2 }
```
fig.save(outfigname, transparent=True)
```
{: .fs-1 }

You will make plots routinely. It is recommended to integrate the above commands in a script or a wrapper in a way that is convenient to you. If anything in this part is not clear to you, you can check the documentation for [APLpy]([APLpy](https://aplpy.github.io/)). You might need some patience and may need to try some things since not everything has been very clearly documented.
{: .fs-2 }

###### IDL
