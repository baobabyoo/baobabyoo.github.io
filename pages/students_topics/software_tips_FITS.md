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

You can use the following [CASA Software Package](https://casa.nrao.edu/) commands to convert between the Miriad and FITS format images:
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

To crop a sub-image in CASA, you can use the CASA `umsubimage` task like:
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
{: .fs-2 }

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

###### IDL
