---
layout: default
title: Dust
parent: Topic
grand_parent: To my students
nav_order: 1
---

#### Interstellar Dust (SED or Polarization)


- **Background Physics**
    1. *General :* You need to read through this review artical [Hildebrand (1983)](https://ui.adsabs.harvard.edu/abs/1983QJRAS..24..267H/abstract).
    2. *Dust Polarization :* You need to read through this review artical [Hildebrand (2000)](https://ui.adsabs.harvard.edu/abs/2000PASP..112.1215H/abstract).
- **Some Minimum Knowledge about Planet-Formation**
    1. Please read [Kokubo and Ida (1998)](https://ui.adsabs.harvard.edu/abs/1998Icar..131..171K/abstract) and [Hansen and Murray (2013)](https://ui.adsabs.harvard.edu/abs/2013ApJ...775...53H/abstract).
- **Related to Our Research**
    1. *SED Analysis :* 
        1. Please read [Liu (2019)](https://ui.adsabs.harvard.edu/abs/2019ApJ...877L..22L/abstract) and the introduction section of [Liu et al. (2021)](https://ui.adsabs.harvard.edu/abs/2021ApJ...923..270L/abstract) to be up-to-date. 
        2. If you are performing SED fittings to Class II disks, [Beckwith et al. (1990)](https://ui.adsabs.harvard.edu/abs/1990AJ.....99..924B/abstract), [Beckwith and Sargent (1991)](https://ui.adsabs.harvard.edu/abs/1991ApJ...381..250B/abstract), and [Dullemond et al. (2018)](https://ui.adsabs.harvard.edu/abs/2018ApJ...869L..46D/abstract) are very important references.
        3. If you are are performing SED fittings to Class 0/I objects, [Li et al. (2017)](https://ui.adsabs.harvard.edu/abs/2017ApJ...840...72L/abstract), [Galvan-Madrid et al. (2018)](https://ui.adsabs.harvard.edu/abs/2018ApJ...868...39G/abstract), [Zamponi et al. (2021)](https://ui.adsabs.harvard.edu/abs/2021MNRAS.508.2583Z/abstract), and [Xu (2022)](https://ui.adsabs.harvard.edu/abs/2022arXiv220300941X/abstract) would be very important references. 
        4. If you are working on wide-field bolometric imaging for molecular clouds, [Lin et al. (2016)](https://ui.adsabs.harvard.edu/abs/2016ApJ...828...32L/abstract), [Lin et al. (2017)](https://ui.adsabs.harvard.edu/abs/2017ApJ...840...22L/abstract), and [Lin et al. (2019)](https://ui.adsabs.harvard.edu/abs/2019A%26A...631A..72L/abstract) are the most advanced journal publications. But talk to us for some latest development.
    2. *Polarization Mechanism :* For our recent investigation about (sub)millimeter dichroic extinction, please read [Liu et al. (2018)](https://ui.adsabs.harvard.edu/abs/2018A%26A...617A...3L/abstract), [Ko et al. (2020)](https://ui.adsabs.harvard.edu/abs/2020ApJ...889..172K/abstract), and [Liu (2021)](https://ui.adsabs.harvard.edu/abs/2021ApJ...914...25L/abstract). For polarized dust self-scattering, please read [Kataoka et al. (2016)](https://ui.adsabs.harvard.edu/abs/2016ApJ...820...54K/abstract) and references therein.
    3. *After reading the necessary ones for you mentioned above :* Come back to read the overviews of [Birnstiel et al. (2016)](https://ui.adsabs.harvard.edu/abs/2016SSRv..205...41B/abstract) and [Testi et al. (2014)](https://ui.adsabs.harvard.edu/abs/2014prpl.conf..339T/abstract) to obtain the context of the developments in this area, but keep in mind that not all of the information in those Pre-2019 publications are up to date. To be more updated, reading [Okuzumi et a. (2019)](https://ui.adsabs.harvard.edu/abs/2019ApJ...878..132O/abstract) is important.
- **Interferometry**
    1. *Textbook :* It is free to download the textbooks [Synthesis Imaging in Radio Astronomy II](https://www.aspbooks.org/a/volumes/table_of_contents/?book_id=292) and [Interferometry and Synthesis in Radio Astronomy](https://link.springer.com/book/10.1007/978-3-319-44431-4) online. You need to read through at least the first 5 chapters.
    2. *Getting hand dirty :* It is good to walk through some of these [CASA Guides](https://casaguides.nrao.edu/index.php?title=ALMAguides). The example with the observations on the [TW Hya](https://casaguides.nrao.edu/index.php?title=TWHydraBand7) protoplanetary disk may be the easiest to begin with. If you work on polarization data, you will need to walk through the case of [3C286](https://casaguides.nrao.edu/index.php?title=3C286_Polarization). If you need to calibrate the JVLA data yourself, go through cases at [here](https://casaguides.nrao.edu/index.php?title=Karl_G._Jansky_VLA_Tutorials).
    3. *SMA :* The official package for data calibration is [MIR IDL](https://lweb.cfa.harvard.edu/~cqi/mircook.html) although there is some discussion to switch over to [CASA](https://casa.nrao.edu/index.shtml) in the future.
    4. *Miriad Software Package :* We use it to image the calibrated SMA data or to perform polarization calibration for the SMA data. I found this package to be handy on many occasions and have been using it routinely. I am using a binary distribution that was downloaded from [here](https://www.astro.umd.edu/~teuben/miriad/). I recommend using the latest version compiled for CARMA. A documentation for individual Miriad tasks can be found [here](https://www.atnf.csiro.au/computing/software/miriad/taskindex.html).
- **Potentially Useful Packages for SED Analysis**
    1. *Galario :* Please check [Tazzari et al. (2018)](https://ui.adsabs.harvard.edu/abs/2018MNRAS.476.4527T/abstract) and this [Github](https://mtazzari.github.io/galario/) page.
    2. *Frankenstein :* Please check [Jenning et al. (2020)](https://ui.adsabs.harvard.edu/abs/2020MNRAS.495.3209J/abstract) and this [Github](https://github.com/discsim/frank) page.
    3. *synthesizer :* A very useful wrapper to perform MCRT radiative transfer modeling for dust polarization and then create synthetic ALMA or JVLA observations. Please check this [Github](https://github.com/jzamponi/synthesizer)
    4. *PyRaTE :* A code to estimate the Goldreich-Kylafis effect [Tritsis and Kylafis (2023)](https://arxiv.org/abs/2310.15230)
- **Useful online material
    1. *NASA PAH Database :* [here](http://www.astrochemistry.org/pahdb)
    2. *DSHARP opacity :* [here](https://github.com/birnstiel/dsharp_opac)
    3. *DIANNA opacity :* [here](https://diana.iwf.oeaw.ac.at/data-results-downloads/fortran-package/)

{: .fs-2 }
