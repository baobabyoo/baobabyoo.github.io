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
