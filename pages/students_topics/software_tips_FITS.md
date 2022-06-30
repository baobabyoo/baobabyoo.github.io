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
one or more binary **data table**
one or more **header files** that contain the necessary information to understand the data.
{: .fs-2 }

Since the binary data are not human readable, we cannot handle the FITS files with a text editor (e.g., vim) or other commercial or open resource software like MS Excel or Open Office. Here I provide some simple tips for manipulating FITS images that can be useful to radio astronomers.
{: .fs-2 }





### Viewers

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

We used the  [karma](https://www.atnf.csiro.au/computing/software/karma/) package a lot in the old days. The `kvis` function is very useful when you are interactively examining the gas kinematics of an astronomical object with a spectral line image cube.
