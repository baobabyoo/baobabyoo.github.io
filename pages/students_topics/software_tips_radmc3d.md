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
{: .fs-2 }

An online documentation can be found in [this webpage](https://www.ita.uni-heidelberg.de/~dullemond/software/radmc-3d/manual_radmc3d/index.html).
The PDF version of the document can be found in [this link](https://www.ita.uni-heidelberg.de/~dullemond/software/radmc-3d/radmc3d.pdf).
{: .fs-2 }

### 2. Installing

#### 2.1 Setting up the environment:

#### Using Linux CentOS:

#### Using Macbook with an Intel chip:
You need to use fortran compiler to compile the RADMC-3D source codes that you fetch via github. Open a terminal and type in the command line `which gfortran` to see which is the path to your gfortran executable. If it does not return a valid path, you need to install **gfortran** before proceeding. I am trying with a Macbook Pro with  Mac OS Ventura 13.4 and 2.3 GHz Quad-Core Intel Core i7 (32 GB RAM). I downloaded the gfortran (`gfortran-Intel-11.3-Monterey.dmg`) installer from this [webpage](https://github.com/fxcoudert/gfortran-for-macOS/releases). After installing it (by double-clickings), open a new terminal and try typing again `which gfortran` to see where it is.

#### Using Macbook with a M1 chip:
(Under construction. Please let me know if you have worked out a step-by-step guide.)

#### 2.2 Fetching the code from Github using the following command:
```
gitclone https://github.com/dullemond/radmc3d-2.0.git
```

#### 2.3 Building the code
Please follow the detailed instruction [here](https://www.ita.uni-heidelberg.de/~dullemond/software/radmc-3d/manual_radmc3d/quickstart.html).
