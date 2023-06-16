---
layout: default
title: RADMC-3D v2.0
parent: Software Tips
grand_parent: To my students
nav_order: 4
---

### 1. Introduction

This is a software package for carrying out 3D Monte-Carlo radiative transfer simulations.
The official webpage is [here](https://www.ita.uni-heidelberg.de/~dullemond/software/radmc-3d/index.php).
The latest version (in 2023 Jun) is 2.0, which can be obtained via [Github](https://github.com/dullemond/radmc3d-2.0/tree/master).
Note that this code sticks with the cgs units.
{: .fs-2 }

An online documentation can be found in [this webpage](https://www.ita.uni-heidelberg.de/~dullemond/software/radmc-3d/manual_radmc3d/index.html).
The PDF version of the document can be found in [this link](https://www.ita.uni-heidelberg.de/~dullemond/software/radmc-3d/radmc3d.pdf).
{: .fs-2 }

### 2. Installing
A very detailed instruction is [here](https://www.ita.uni-heidelberg.de/~dullemond/software/radmc-3d/manual_radmc3d/installation.html). In spite that it may not be necessary, I recommend you to read through this instruction.

#### 2.1 Setting up the environment:
A very detailed instruction is [here](https://www.ita.uni-heidelberg.de/~dullemond/software/radmc-3d/manual_radmc3d/overview.html). In the following I provide some of my commands/experiences if you want to just follow blindly without understanding anything.

**Note that if you would like to be benefited by parallel computing, remember to use** `FF = ifort -openmp` **when editing the make file of radmc3d** (see below).

#### Using Linux CentOS:

#### Using Macbook with an Intel chip:
You need to use fortran compiler to compile the RADMC-3D source codes that you fetch via github. Open a terminal and type in the command line `which gfortran` to see which is the path to your gfortran executable. If it does not return a valid path, you need to install **gfortran** before proceeding.

I am working with a Macbook Pro with  Mac OS Ventura 13.4 and 2.3 GHz Quad-Core Intel Core i7 (32 GB RAM).

I first tried download the gfortran (`gfortran-Intel-11.3-Monterey.dmg`) installer from this [webpage](https://github.com/fxcoudert/gfortran-for-macOS/releases). After installing it (by double-clickings), the compiler seems to be there. But it cannot compile RADMC-3D correctly. Then I used the command `rm -rf /usr/local/bin/gfortran` to remove this gfortran.

Then I tried to install [Homebrew](https://brew.sh/) to build my environment. And then I typed `brew install gcc` to first install the latest **GNU Compiler Collection**. It automatically comes with a version of *gfortran*. Open a new terminal and try typing again `which gfortran` to see where it is. This version compiled RADMC-3D successfully.

#### Using Macbook with a M1 chip:
(Under construction. Please let me know if you have worked out a step-by-step guide.)

#### 2.2 Fetching the code from Github using the following command:
```
gitclone https://github.com/dullemond/radmc3d-2.0.git
```

#### 2.3 Building the code
Please follow the detailed instruction [here](https://www.ita.uni-heidelberg.de/~dullemond/software/radmc-3d/manual_radmc3d/quickstart.html).
Note that when doing `make install`, the command lines may have some prompt messages that need you to take care of, in particular, those about setting the environmental variables in the startup shell script. For example, after seeing these prompt messages,
```
'/Users/hyliu/Documents/softwares/radmc3d/v2p0/radmc3d-2.0/src'
You must have a bin/ directory in your home directory
-----Shall I make /Users/hyliu/bin for you?
y
y
Creating /Users/hyliu/bin for you...
The /Users/hyliu/bin directory exists, but it not in the PATH environment variable
You must put the
/Users/hyliu/bin directory
in the path yourself (in the .tcshrc file if you use the tcsh shell...)
If you do it now, don't forget to type 'rehash'.
```
I included this line `export PATH=//Users/hyliu/bin:$PATH` in my `~/.bashrc`.

If you are using Mac, some Python scripts for basic analyses may be located in the path similar to `/Users/hyliu/bin/python/radmc3d_tools`.


#### 2.4 Using the provided Python analysis tools

Please find the [instruction](https://www.ita.uni-heidelberg.de/~dullemond/software/radmc-3d/manual_radmc3d/installation.html#how-to-install-and-use-the-python-radmc3d-tools).


#### 2.5 Running simulations

The steps to conduct your own simulations are:
1. Using your own program to write the ASCII (or binary) input files that defines the model (e.g., density distribution, stellar spectral energy distribution, etc)
2. Use the RADMC-3D code to read your model and run simulations
3. Analyze the output images or spectra

The quickest way to startup is to modify the example-programs under the `/example` directory that can create the input files for certain physical problems (e.g., protoplanetary disks).

When building a model (e.g., with a Python code), you need to specify
- the grid structure
- the dust and/or gas density distributions
- dust opacity table
- the stellar positions and properties

We need to provide RADMC-3D a discrete wavelength table and RADMC-3D will make calculations at those wavelengths.
