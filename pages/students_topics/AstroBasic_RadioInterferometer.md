---
layout: default
title: Radio Interferometry
parent: Basic Astrophysics
grand_parent: To my students
nav_order: 9
---

## Radio Interferometry (or, aperture synthesis technique)

*If you want to use interferometry data or would like to chat about some existing interferometric observations, it may be important to take a little effort to memorize the boldfaced parts after making sure that you understand them. They come up very frequently in the conversation.*
{: .fs-1 }

**After you become a little more familiar with this material, a recommended way of using this webpage is to use the *find* tab of your browser to search for the keywords you are puzzling at**.
{: .fs-1 }

**If you have learned the basic about radio interferometry and you are trying to plan your own observational project (e.g., if you are preparing an observing script), just scroll down to the check list.**
{: .fs-1 }

### Lecture Notes

**2021-Jul-08/12 @ NTNU :** *Principle of interferometry, noise, and calibration strategy.* ( [Lecture Notes PDF](https://github.com/baobabyoo/baobabyoo.github.io/blob/main/pages/files/lecture_notes/2022/Radio_interferometry_2022Jul.pdf); go to the address and then click the **Download** button to download). These are my quick notes, which are not necessarily fully correct and may not be comphresensitve to those who did not attend the classes.
{: .fs-1 }


### Why interferometry?

Analyzing interferometric data can be hard. It has been a nightmare to many astronomy/astrophysics students. This technique worths 0.5 Nobel Prize ([to Sir Martin Ryle, in 1974](https://www.nobelprize.org/prizes/physics/1974/summary/)).
In my experience, it takes a full-time student 2-6 months to master this technique, to the level that they can process data and troubleshoot independently. During this time period, both the trainer and trainee need to devote considerable amount of time. So, in fact, most of our colleagues do not pick it up. People who have mastered radio interferometry are relatively unique.
{: .fs-2 }

So why use interferometry at all? How does the pain pay off?
{: .fs-2 }

**This is all about the need for resolution.**
{: .fs-2 }

For a telescope, with a lens or reflector that has a diameter *D*, at a wavelength *L*, the angular resolution is approximately **L/D [in units of radian]** (i.e., to convert it to degree unit, you multiple *L/D* by (180/pi); to convert from degree to arcsecond unit, you multiple another factor of 3600). At a certain wavelength, if you want to achieve better and better angular resolution, then you need to build bigger and bigger telescopes. This is particularly bad when you are observing at (sub)millimeter or radio (i.e., centimeter or decimeter) wavelength bands. In such cases, the *L* is much longer than the that in the optical or near-infrared observations. Those gigantic radio telescopes almost look like Gundams!
{: .fs-2 }

The Large Millimeter Telescope ([LMT](http://lmtgtm.org/); ~70-350 GHz) in Mexico has a dish with 50-meter diameter, which is almost as big as the playground in a typical elementary school in Taiwan. Presently, the biggest movable *single-dish* radio telescopes are the [Green Bank 100-meter telescope](https://greenbankobservatory.org/science/telescopes/gbt/) and [Effelsberg 100-meter telescope](https://www.mpifr-bonn.mpg.de/en/effelsberg).  Beyond this size, it becomes unrealistic to find material that is hard enough to make the mechanical structures. The surface of such big single-dish telescopes may considerably deform when you slew the telescope, due to gravity. It also deforms when the wind is blowing. Due to the large inertia, these big telescopes usually can only slew very slowly, which makes it difficult to observe multiple target sources or map a big region. To alleviate the mechanical problems, the bigger radio telescopes are not movable, for example, the [Arecibo](https://en.wikipedia.org/wiki/Arecibo_Observatory) telescope and the [FAST](https://en.wikipedia.org/wiki/Five-hundred-meter_Aperture_Spherical_Telescope) observatory. The observations with such static dishes are subject to some limitations, as expected.
{: .fs-2 }

The radio interferometry technique sheds light on this problem. Based on physics/mathematical principles, we can build an **array** of telescopes that have small dishes. The interferometry technique allows us to to-some-extent take this array as an equivalent, big single-dish telescope, of which the diameter is comparable with the **largest projected separation** of the smaller telescopes in our array. Here, *projection* means we project the spatial distribution of the array to a plane that is perpendicular to the line-of-sight (i.e., the line connecting from us toward the astronomical source being observed). We call the process to put together the signals taken from individuals of the small telescopes **making correlation**. The hardware or software device to make correlation is called **correlator**. Each of the small telescopes are easy to fabricate. The technical difficulties are deferred to the stage of making correlation. Most (but not all) of the difficulties are hidden from the users in the present date interferometric observatories.
{: .fs-2 }

Sometimes, you still need to deal with the not-yet-so-well correlated signals by **calibrating** them. When planning the interferometric observations, you need to follow a strategy to enable proper data calibration. These are what make it hard to use radio and (sub)millimeter interferometers. But it really isn't that bad already! Don't be scared away! Also, a Master's or Ph.D. program is not supposed to be trivial. If you are expecting something difficult enough to warrant a part of a degree, this is it.
{: .fs-2 }

Fortunately, we are really coming to the era that the big interferometric radio or (sub)millimeter observatories (e.g., [ALMA](https://www.almaobservatory.org/en/about-alma/)) are offering good user support. Nowadays, one can choose to use some of them in a way that most of the complicated mathematical principles are hidden from the user. To enable you to use [ALMA](https://www.almaobservatory.org/en/about-alma/) this way, or to enable you to make query to the [archival observations of ALMA](https://almascience.nao.ac.jp/aq/), in the following, I will introduce some of the basic concept and the terminologies. Then, I will introduce how we normally use these interferometric observatories. It will mostly stay at a qualitative level, which intends to be a minimal set of knowledge that you need to know before using ALMA like taking a picture with a point-and-shoot camera. If I have time, I may host the mathematical details at other places for the advanced users. The details about the ALMA hardwares can be referenced from the official ALMA [Technical Handbook](https://almascience.nao.ac.jp/proposing/technical-handbook). If you want to be a black belt ALMA user, at some point, it may become inevitable to read through this very thick technical handbook.
{: .fs-2 }

### How a radio interferometer look like?

###### Looking from outside

You can find the pictures of the modern radio or (sub)millimeter interferometers such as the [SMA](http://sma1.sma.hawaii.edu/smaoc.html) (200-400 GHz), [ALMA](https://www.almaobservatory.org/en/about-alma/) (90-1000 GHz), [JVLA](https://www.almaobservatory.org/en/about-alma/) (0.05-50 GHz), [GMRT](http://www.gmrt.ncra.tifr.res.in/) (0.1-1.5 GHz), [ASKAP](https://www.atnf.csiro.au/projects/askap/index.html) (0.7-1.8 GHz), [MeerKat](https://www.sarao.ac.za/gallery/meerkat/) (0.6-15 GHz), [VLBA](https://science.nrao.edu/facilities/vlba) (0.3-90 GHz), [EHT](https://eventhorizontelescope.org/array) (230 GHz), and so on. These are the *dish arrays* (i.e., each element in the array is a single-dish telescope). In fact, some of the dishes of the ALMA array are used as single-dish telescopes, which is called the *Total Power (TP)* array.
{: .fs-2 }

We correlate the signal collected from every pair of telescopes (i.e., every two of them) in our array. We call a pair of telescopes a **baseline**.
{: .fs-2 }

Besides dish array, there are also radio interferometers that are composed of dipole antennae without dishes, such as [LOFAR](https://www.astron.nl/telescopes/lofar/), [LWA](https://leo.phys.unm.edu/~lwa/index.html), [OVRO-LWA](http://www.tauceti.caltech.edu/LWA/). They are operating at low frequency bands (<1 GHz, typically). The dipole arrays are based on the same interferometric principle. However, the response functions of the dipoles are very different from those of the dishes telescopes. Usually, these dipole arrays can simultaneously observe almost the whole sky. For example, the OVRO-LWA observatory is performing all sky monitoring routinely. Otherwise, these dipole arrays can base on the *[beamforming](https://en.wikipedia.org/wiki/Beamforming)* technique to image some selected patches on the sky with high angular-resolution.
{: .fs-2 }

Finally, there are also optical and infrared interferometers, for example, the [Very Large Telescope Interferometer (VLTI)](https://www.eso.org/sci/facilities/paranal/telescopes/vlti.html) and the [CHARA](https://www.chara.gsu.edu/). They can achieve extremely high angular resolution thanks to the short operational wavelengths. Looking from outside, they appear very similar to the radio or (sub)millimeter interferometer arrays. But the receiver techniques and the way to correlate signals from individual telescopes are very different from those of the radio or (sub)millimeter interferometer arrays.
{: .fs-2 }

Owing to the research interests of my group, I will focus more on the radio and (sub)millimeter dish arrays in the following.
{: .fs-2 }

###### Observing with a radio or (sub)millimeter interferometer

The dish collects the incoming light. The bigger the dish size, the more light it can collect in a unit of time, meaning that the **sensitivity** is better. For both single-dish telescope or interferometry, **sensitivity** is usually expressed in intensity units, which has dimension of *energy per unit area per unit solid angle per unit time per unit observing-frequency*. For instance, we can express the sensitivity as the intensity of an equivalent black body, e.g., we say our brightness sensitivity is 1 Kelvin. This means that, after we are done with all the calibration and then produce an image, which includes both the *emission of the target source* and the *thermal white noise*, the root-mean-square of the intensity fluctuation contributed by the thermal white noise corresponds to the intensity of the black body emission at 1 K temperature. We call the temperature of such equivalent black body the **[brightness temperature](https://en.wikipedia.org/wiki/Brightness_temperature)**. For most of the present-date radio or (sub)millimeter interferometry, the noise statistics are indeed approximately Gaussian (i.e., white). Then for example, if your target source is a 6000 K black body emitter, such as our Sun, and if you want to resolve it at 10-sigma significance, then you need to achieve an rms noise level of 600 K. An ALMA image on the Sun can be found [here](https://www.almaobservatory.org/en/announcements/alma-starts-observing-the-sun/).
{: .fs-2 }

The longer you integrate on the target source with the observations, the better sensitivity (i.e., the lower rms noise level) you can achieve. Since the noise follows the Gaussian statistics, **the noise level is inversely proportional to the square-root of the on-source integration time**.
{: .fs-2 }

If the total number of telescopes is fixed, enlarging the dish sizes (sometimes we call the dish(es) the **collecting area**) can make you achieve the same noise level within a shorter on-source integration time. Ideally, to yield a specified overall collecting area, it is better to build many small dishes instead of a few big dishes. You will see the reason in the following. Also note that a telescope cannot be arbitrarily small. There needs a minimum space to host the other hardware devices including the receivers and the cryogenic systems for the receivers, etc, which will also be introduced later.
{: .fs-2 }

In astronomical observations, we also often express intensity or sensitivity in the unit call **Jy beam<sup>-1</sup>** (pronounced as Jansky per beam). [Jy](https://en.wikipedia.org/wiki/Jansky) is the unit for flux density, which has a dimension of  *energy per unit area per unit time per unit observing frequency*, i.e., flux density is integrated intensity over solid angle (e.g, the solid angle of your target source). *Jansky per beam* denotes the flux density in a *unit resolution element* in your image. If your resolution element is a Gaussian beam, you can convert between the brightness temperature and the Jy beam<sup>-1</sup> based on the formula given in [this page](https://science.nrao.edu/facilities/vla/proposing/TBconv).
{: .fs-2 }

So what is the *unit resolution element*? As a start, you may comprehend it as a shape (e.g., a circle) which occupies a certain solid angle in the image domain.
The full story is only slightly more complicated than that. Precisely speaking, the **resolution** describes the *angular response function* of your telescope. For a single-dish radio telescope that the dish diameter is *d*, at observing wavelength *L*, that response function may be approximated by a two-dimensional gaussian that has a [full-width-at-half-maximum](https://en.wikipedia.org/wiki/Full_width_at_half_maximum#:~:text=In%20a%20distribution%2C%20full%20width,half%20of%20its%20maximum%20value.) around 1.22 times *L/d*. The image you obtained from the observations is the intensity distribution of your astronomical source (for example, a nebula) **convolved** with this response function. Fundamentally, you cannot distinguish the following two cases: (1) two point-like sources that have a separation closer than 1-sigma Gaussian width of the response function, and (2) a relatively spatially extended source (e.g., the angular scale is comparably larger than your response function). To distinguish these two cases, we must improve the angular resolution, for example, by using the same single-dish telescope to observe at a higher frequency (i.e., shorter wavelength), or by performing the interferometric follow-up observations at higher angular resolution.
The solid angle of the response function can be obtained by integrating the response function over the whole angular range. If you are interested in the mathematical details, you can check Section 3.3.3 of [this page](https://www.cv.nrao.edu/~sransom/web/Ch3.html). Note that your *angular resolution* is not identical to your *position accuracy*. If your target source is a bright point-like source (e.g., a spatially unresolved high-redshift quasar), your interferometric observations may determine the coordinates of this quasar at a precision that is much finer than the angular resolution of the observations.
{: .fs-2 }

For an interferometer array, we call the response function provided by the dish, the function that the characteristic angular scale is given by *L/d* [in radian units], the **primary beam** of the observations. If a target source is observed outside of the primary beam, its intensity will be significantly attenuated. Sometimes, people also refer to the full-width-at-half-maximum (FWHM) of the Gaussian primary beam simply as *primary beam*. This FWHM is approximately the **simultaneous field-of-view** of the interferometric observations on a single pointing (i.e., observations that track a specific coordinates instead of scanning).  The longer wavelength you observe, the bigger simultaneous field-of-view (or primary beam) you have.
{: .fs-2 }

The resolution element of a modern interferometer array (e.g., ALMA) is also approximately a two-dimensional gaussian, although the major and minor axes of this Gaussian response function may not be equal. So you need to describe this two-dimensional gaussian resolution element with the major axis, minor axis, and position angle, e.g., it is often expressed as something like (0".5 x 0".5; P.A.=10 degree). We call this resolution element a **synthesized beam**. The major and minor axes of this resolution element is determined by the largest projected separations *B<sub>max</sub>* of the telescopes in the interferometer array. That is the major or minor axis of the resolution element is approximately *L/B<sub>max</sub>*. A very special aspect is that the smallest projected separations *B<sub>min</sub>* (e.g., 1000 meters) of the telescopes determins the **largest recoverable angular scale** of your interferometric observations. The observed intensity of any structure that is spatially more extended than *L/B<sub>min</sub>* will be very significant attenuated. That is, an interferometer is working like a spatial high-pass filter.
{: .fs-2 }

Note that if you express the sensitivity of an interferometer in units of Jy beam<sup>-1</sup>, the sensitivity will be independent of the solid angle of your synthesized beam. We say that the point-source sensitivity of an interferometer is independent of angular resolution. However, if you express it in units of Kelvin, it will be better (i.e., corresponds to a lower temperature) if you are using a coarser angular resolution (i.e., a synthesized beam with a bigger solid angle).
{: .fs-2 }

The values of *B<sub>max</sub>* and *B<sub>min</sub>* are determined by the **array configuration**, which describes how you locate the telescopes in an array. Many modern interferometers (e.g., ALMA, SMA, JVLA) can reconfigure the array, i.e., moving telescopes from certain pads to the others. SMA has four different array configurations, namely the subcompact, compact, extended, and very extended array configurations. The most extended array configuration offers the best achievable angular resolution, however, also filters out a lot of extended emission. To recover the extended emission, we can combine the observations taken with the observations taken in the compact array configuration, and the observations taken with the single-dish telescopes. Similarly, ALMA has the C-1, C-2, ..., C-10 array configuration (from the most compact to the most extended), and JVLA has the D, C, B, and A array configurations (from the most compact to the most extended). JVLA rotate throughs these four array configurations approximately every 1.5 years (see the [array configuration schedule](https://science.nrao.edu/facilities/vla/proposing/configpropdeadlines)). For a student, it is good to keep in mind when you should propose the observations you need, otherwise, you may miss the timeline for graduation!
{: .fs-2 }

In general, we want an array to have small *B<sub>min</sub>* such that we can recover the angularly extended astronomical emission sources. Mechanically, *B<sub>min</sub>* cannot be smaller than your dish diameter *d*. Otherwise, when you slew the telescopes, their dishes will collide with each other. That makes one motivation to build many small dishes instead of a few large dishes. In addition, small dishes also provide bigger simultaneous-field-view than big dishes, which is advantageous when performing mapping experiments or blind surveys of certain types of astronomical sources. However, the more (small) telescopes you build, the more receivers you need to build. This part is costly. And the hardware or software power to correlate the incoming signal scales as the square of the number of telescopes. Since we usually do not have unlimited budget, these also need to be taken into consideration when building an interferometry array.
{: .fs-2 }

###### Inside the receiver cabin

The dishes on the telescopes collect the incoming electromagnetic wave to feed the **receivers** (sometimes, through an additional sub-reflector).
{: .fs-2 }

In most cases, one receiver observes one polarization mode at a time. The **linear feed** receivers observe the X and Y linear polarizations that are perpendicular to each other (in the Euclidean space). The **circular feed** receivers observe the R and L (i.e., right- and left-handed) circular polarizations. A circular feed receiver can be realized by combining a linear feed receiver with a [**quarter-wave plate**](https://en.wikipedia.org/wiki/Waveplate). To perform full polarization interferometric observations, one either needs to simultaneously use two receivers to observe at the same frequency, or in the case of using single circular feed, cycling the quarter waveplates through the **Walsh cycle** (this is deprecated at SMA; but if you are interested in more details, see [SMA memo 156](https://lweb.cfa.harvard.edu/sma/memos/156.pdf)).
{: .fs-2 }

The characteristic size scales of (mechanical) structures on a receiver are comparable to the wavelength you are observing. When the wavelength of the incoming EM wave is much longer than the characteristic size scales of a receiver, this receiver will not be sensitive to the EM wave. To facilitate the observations over a wide range of wavelengths, there can be multiple receivers on a telescope. Each receiver has its optimal wavelength (or frequency) range to observe. We call such frequency range a **frequency band**. In many cases, they are designed to have optimal performance over various [atmospheric windows](https://en.wikipedia.org/wiki/Radio_window). For example, the 230 GHz receiver and 345 GHz receiver of the SMA are observing at two separated atmospheric windows. The most frequently used ALMA Band 3, 4, 6, and 7 receivers are observing at the ~90 GHz, 150 GHz, 230 GHz, and 345 GHz atmospheric windows, respectively. In between these windows, the atmospheric molecular line (in many cases, water) absorption is serious enough to prohibit the observations from the ground-based observatories. This is also why in the (sub)millimeter observations, we often characterize the weather condition with a quantity called the **precipitable water vapor (PWV)**, which is the amount of vertically integrated water (assuming that you can collect them and convert them to liquid phase). We often express it as PWV = 4 mm, PWV = 2 mm, and so on, where the *X* mm is the height of the converted, liquid phase water.
{: .fs-2 }

At (sub)millimeter wavelength (e.g., when we are observing with the SMA or ALMA), the incoming electromagnetic wave not only comes from the celestial sources. Our atmosphere and anything that is warmer than a few Kelvin is also prominent emitter, which is expected from the profile of black body emission (check the [wiki page](https://en.wikipedia.org/wiki/Black-body_radiation) if you are not familiar with it). The devices on your telescopes emit too. To suppress the non-celestial confusion, we need to isolate the receiver and some devices in the cryogenic systems (you may illustrate this as a combination of a refrigerator and a Dewar filled with liquid Nitrogen and/or liquid Helium). When you operate a telescope, you cool the receiver you are going to use down to its operational temperature. During the observations, you monitor the **receiver temperatures** which partly determine the noise level you can achieve.
{: .fs-2 }

The electronic signals you directly obtained from the receivers have ~100 GHz characteristic frequencies. Not all electronic devices (e.g., amplifiers) can respond to signals at such a high frequency. To enable further processing of the signals, we need to generate the artificial signal using a **local oscillator** ([**LO**](https://en.wikipedia.org/wiki/Local_oscillator)), and then mix the LO-signal with the signal obtained from the receiver with a [**mixer**](https://en.wikipedia.org/wiki/Frequency_mixer) to down-convert the signal to low frequency (usually, a few or up to 10~20 GHz). We call this technique (i.e., combining receiver, LO, mixer, and amplifier) the [**Heterodyne**](https://en.wikipedia.org/wiki/Heterodyne) system.
{: .fs-2 }

We call the low-frequency output of the mixer as the  **intermediate frequency (IF) signal**. For example, the SMA now records the 4-16 GHz IF signals ([check this page](http://sma1.sma.hawaii.edu/status.html) if you are not sure). Since a IF range can correspond to a higher frequency range and a lower frequency range of the ordinary signals, namely the **upper sideband (USB)** and the **lower sideband (LSB)**, with a single LO tuning, the modern observatories (e.g., SMA, ALMA) usually allow you to record signals from the upper or lower sidebands, if not both. Again, taking the capability of the SMA as an example, if you tune the LO-signal to 224 GHz, you can simultaneously observe the 208~220 GHz and the 228~240 GHz frequencies ranges. This is a very frequently adopted tuning in the studies of the interstellar medium, which cover multiple useful tracers such as the CO/<sup>13</sup>CO/C<sup>18</sup>O J=2-1 rotational transition, the shock tracer SiO J=5-4, the CH<sub>3</sub>CN J=12-11 line forest which is a very useful thermometer, the dense gas tracer <sup>13</sup>CS J=5-4, many CH<sub>3</sub>OH, SO, and SO<sub>2</sub> lines, and the hydrogen recombination line H30-alpha (which trace ionized gas), and so on. Of course, these observations also sense the continuum emission (e.g., from dust or free electrons). To build some familiarity with these lines, you can see [Liu et al. (2012)](https://ui.adsabs.harvard.edu/abs/2012ApJ...756...10L/abstract) which also include reviews of individual of some of these molecules. If you are not sure about the mathematical principle in the mixing, and if you are uncertain about why there should be the upper and lower sidebands, you can check the Sum-to-product formula in the [list of trigonometric_identities](https://en.wikipedia.org/wiki/List_of_trigonometric_identities).
{: .fs-2 }

The signal obtained from the heterodyne system is then transmitted to the **correlators**, which are typically located in a bigger building, for further processing. The concept of correlating the signal will become (just) a little more clearer in the next section.
{: .fs-2 }

### A little more about interferometry

If you are already getting comfortable with the idea that, a short/long **baseline** in the interferometry array is sampling the angularly more extended/compact emission from a celestial object, I am going to introduce a little more about the underlying mathematical principle. This may help you to get a better idea about our terminology. If you feel this part is hard when reading it for the first time, you can move on to the next section first. Later you can come back to check some concepts, when it is necessary/useful.
{: .fs-2 }

The full derivation of this principle is involving and should be introduced in a serious course. You may refer to the free textbooks [Synthesis Imaging in Radio Astronomy II](https://www.aspbooks.org/a/volumes/table_of_contents/?book_id=292) and  [Interferometry and Synthesis in Radio Astronomy](https://link.springer.com/book/10.1007/978-3-319-44431-4) which I recommend. If you are taking a course about radio interferometry and if you are reading into a textbook anyway, you may view this webpage as a tour guide. Also, I strongly recommend watching the videos at [2022 Submillimeter Array Interferometry School](https://lweb.cfa.harvard.edu/sma-school/program/). I am not sure whether or not this link will be permanent. If this link is broken, please let me know.
{: .fs-2 }

In the following, I assume that the three-dimensional coordinates of each telescope in our array are known exactly, to bypass some complicated technical details. This assumption is usually fair when you are using a modern interferometric observatory except the Very Long Baseline Interferometry (or the Event Horizon Telescope).
{: .fs-2 }

A little more assumption: the celestial objects of interest are far enough from us. In this case, our observations are only sensitive to the projected intensity distribution onto a plane that is perpendicular to our line-of-sight. We call this plane as the **plane of sky**. In other words, we assume that the celestial objects of interest are far enough for us to lose the sense of whether *a sub-structure of our target source is a little closer to us or is further* (with respect to the mean distance of the bulk of the target source). In the following, we will call the plane of sky (a small facet we are looking at) the *spatial domain* for simplicity. It should be understood that the *spatial domain* is defined by the coordinate systems on the sky instead of those on the ground. For simplicity, let's for this moment assume that the incoming light is monochromatic.
{: .fs-2 }

Now is the principle:
{: .fs-2 }

**An interferometer array incompletely samples the *spatially Fourier transformed intensity distribution* of a celestial object.**
{: .fs-2 }

What this means?
{: .fs-2 }

In our terminology, we refer to the domain that the *Fourier transformed intensity distribution* lives in the as the **uv domain**. The coordinates in the uv domain can be expressed by *(u, v)*. In the spatial domain, the intensity distribution at a frequency *f* is expressed as a scalar function *I<sub>f</sub>(x,y)* of the spatial coordinates *(x, y)*. Since we are discussing about the case of monochromatic incoming light, I will omit the subscript *f* to avoid cluttering. In the uv domain, the intensity distribution is described by a pair of scalar function, namely the amplitude *a(u, v)* and phase *p(u, v)*: *a(u, v)* describes how bright is the emission on the angular scale (and direction) that is represented by the uv coordinates *(u, v)*; *p(u, v)* the angular offset of that emission component from a **phase referencing center** you can choose. For a specific *(u, v)*, we call the *a(u, v)* and *p(u, v)* data together the ** complex visibility** (or simply, **visibility**) at *(u, v)*.
{: .fs-2 }

Roughly speaking, at each time, the observation of a baseline (i.e., the data taken from a pair of telescopes) lets you know the *a(u, v)* and *p(u, v)* at a specific (u, v) coordinates. The separation of *(u, v)* from the origin in uv domain, *(u<sup>2</sup>+v<sup>2</sup>)<sup>1/2</sup>*, which we call **uv distance**, is larger when the baseline is shorter. The position angle of *(u, v)* is determined by the relative orientation between the baseline and the spatial coordinate system in the sky. A baseline aligned in the north-south direction sample the intensity distribution in the north-south direction. You can see how the other directions are can be sampled with arguments based on symmetry.
{: .fs-2 }

Over a night of observations, the sky rotates with respect to your interferometry array. This helps populate more independent sampling points in the *(u, v)* domain. Therefore, it is always favorable to perform long tracking if you are conducting an imaging experiment.
{: .fs-2 }

If you feel it is difficult to illustrate a two-dimensional case with an arbitrary intensity distribution *I(x, y)*, let's first look at a simplified case: a one-dimensional sky with only one coordinate *x*.
{: .fs-2 }

Assuming that the intensity distribution is *I(x)=Acos(kx)* where *A* and *k* are constants. This intensity distribution is obviously peaking at *your chosen origin of coordinate* (i.e., *x*=0), which is your **phase referencing center** in this one-dimensional space.  After you Fourier transform the intensity distribution, you obtain a delta function in the Fourier transformed domain. Mapping to the terminology of interferometry we just introduced, the Fourier transformed one-dimensional intensity distribution is described by the scalar amplitude function *a(k)* that is infinity at the spatial frequency *k* (i.e., the fourier transformed coordinate system) and is zero elsewhere. The scalar phase function *p(k)=0* for all *k*. Note that this delta function should be normalized to *A* after you integrate over the Fourier transformed coordinate. Here, an important concept to remember is that, observing a zero-phase at a certain spatial frequency *k* means that the intensity distribution on the spatial scale corresponding to *k* is centered (in the spatial domain) at your chosen phase referencing center. If you slightly offset the intensity from the phase referencing center to be *Acos(kx + phi)*, you will obtain a non-zero phase a *k* while the normalization of amplitude is unchanged. If the intensity distribution is spatially more extended, that is, if *k* is smaller, then in the Fourier transformed domain you will see the spike (i.e., the delta function) located closer to the origin (in the Fourier transformed one-dimensional coordinate system).
{: .fs-2 }

Now you illustrate that you have a device to make measurements in the Fourier transformed one-dimensional domain. If this device cannot fully sample the spatial frequency *k*, for example, if this device only makes measurements at some discrete *k<sub>i</sub>* (here *i* is just an index) non of which are equal to the *k* defined in your intensity distribution is *I(x)=Acos(kx)*, then all of the *a(k<sub>i</sub>)* and *p(k<sub>i</sub>)* returned by this device are zeros. In this case, the observed intensity distribution is not distinguishable from *I(x)=0*. This device serves as a high- and low-pass filter which leaves you with nothing detectable.
{: .fs-2 }

Of course, no astronomical sources look like a simple cosine wave. Let's look at a more realistic example but still stay in the one-dimensional world: a one-dimensional Gaussian function that has a standard deviation *b*. What happens after you Fourier transform it? The answer is that it is still a Gaussian that has a standard deviation *w*. *w* is inversely proportional to *b* (in case you are really unfamiliar with Fourier transformation, see the [wiki page](https://en.wikipedia.org/wiki/Fourier_transform)). A spatially compact Gaussian function corresponds to a wide one in the Fourier domain. Now if your device only samples the small spatial frequencies *k<sub>i</sub>* around the plateau of the Fourier transformed Gaussian, you will obtain very similar amplitudes and phases at all of the sampled *k<sub>i</sub>* locations. The Gaussian function varies slowly around the plateau. In this case, if we still need to consider measurement errors, we may not be able to clearly distinguish the measurements from a Fourier transformed delta function (i.e., if the intensity distribution is a delta function in the spatial domain, the amplitude is a constant of *k* in the Fourier domain). Since small *k<sub>i</sub>* corresponds to a large spatial scale, in this case, we say that the device has a **too poor spatial resolution** (or say it has a too big beam) to resolve this Gaussian function. Conversely, if your device only sample very large *k<sub>i</sub>* such that the detected amplitudes are all close to zero, then you may not be able to clearly distinguish the measurement from a blank sky. In this case, we say the device has **resolved out** the Gaussian function.
{: .fs-2 }

You can illustrate the two-dimensional case similarly. For example, if your celestial object looks like a elongated strip that is centering at your phase referencing center and is aligning in the north-south direction,  then *p(u, v)* is everywhere zero in the uv domain, while *a(u, v)* is larger at the *(u, v)* coordinates in the Fourier transformed north-south direction and is smaller in the Fourier transformed east-west direction.
{: .fs-2 }

An interferometer is a device to sample *a(u, v)* and *p(u, v)* at some (discrete) *(u, v)* coordinates. A sampled *(u, v)* coordinate is referred to as a **uv sample**, and the overall uv samples taken from a track of interferometric observations are referred to as our **uv coverage**. The magic to extract *a(u, v)* and *p(u, v)* from the signal transmitted from a pair of telescopes is called **correlation**. The hardware or software device to make correlations is called the **correlator**.
 {: .fs-2 }

###### More about correlator and data storage

In the introduction above, we assumed that the incoming light is monochromatic. This is not the reality. Instead, the incoming light is a superposition of EM waves at various frequencies (or wavelengths).
 {: .fs-2 }

Remember, we still want to spectrally resolve some molecular or atomic line emission/absorption. We do not always want to approximately view the incoming light as monochromatic EM waves. In fact, in some applications of broad bandwidth observations of continuum emission (e.g., dust thermal emission, synchrotron emission, free-free emission, etc), we are still not supposed to view the incoming light as monochromatic EM waves in spite that there may not be any spectral line for us to resolve. This is because when you superimpose EM waves over a wide range of frequencies, they can cancel each other (e.g., imagining that you are adding many sine or cosine waves together). There is a similar effect when you are integrating the signal over time, if your *(u, v)* coverage changes significantly over time. These effects are namely the [bandwidth and time-averaging smearing](https://ui.adsabs.harvard.edu/abs/1999ASPC..180..371B/abstract).
 {: .fs-2 }

To mitigate the bandwidth and time-averaging smearing, a radio interferometer array cannot only store the data after making a very long integration. Instead, it needs to break the data stream (in the time domain) into short integrations and store individual of these short integrations. In our terminology, we call the duration of an **integration** the **integration time**. We call a series of consecutive (in the time domain) integrations on one target source (or calibrator source) a **scan**.
{: .fs-2 }

The better angular resolution you have, the easier it is for you to sense the variation of your *(u, v)* coverage over time. Therefore, you need to use a shorter integration time when your angular resolution is better (i.e., when the synthesized beam size is smaller). But the integration time should be just as short as is needed. If you make the integration time arbitrarily short, i.e., if you store data very frequently, the data filesize will become prohibitively large for any post-processing. Typically, SMA uses 15s or 30s integration time, except that some wide-field mosaics can adopt an integration time that is as short as 5~7 seconds (e.g., [Liu et al. 2012](https://ui.adsabs.harvard.edu/abs/2012ApJ...756..195L/abstract); [Battersby et al. 2020](https://ui.adsabs.harvard.edu/abs/2020ApJS..249...35B/abstract)). ALMA typically uses a 2s integration time. JVLA uses a 3s integration time in the B, C, and D array configuration, and uses a 2s integration time in the A array configuration. The JVLA data archive allows you to bin the data in the time domain to reduce the filesize, before downloading them. The raw data filesize of the JVLA, SMA, and ALMA can be as large as 100 GB.
{: .fs-2 }

What about the frequency domain? Similar to how we treat the data in the time domain, what we want to do is to divide the data into bins that have small frequency-widths. In our terminology, we call a bin a **spectral channel**. We call a series of consecutive spectral channels a **spectral window**.
{: .fs-2 }

The electronic signal transmitted from each telescope is a time series (of data). We obtain the information about the frequency domain by Fourier transforming this time series. Making such Fourier transforms demand hardware and/or software devices. In addition, the more spectral channels you have, the larger the data filesize.  Modern radio or (sub)millimeter interferometers such as ALMA or JVLA allow you to sample the IF signal with a few spectral windows. Each spectral window is characterized by a **central frequency**, an **overall frequency width** (i.e., coverage), and a **channel width** (in frequency units). There is some flexibility for you to configure the spectral windows to various overall frequency widths and channel widths. For example, when there is a broad line (e.g., the hydrogen recombination lines, which typically have ~10 km/s linewidths) and a narrow line (e.g., the N<sub>2</sub>D<sup>+</sup> line, which has multiple hyperfine line components each of which can be as narrow as <0.5 km/s), you can resolve them with spectral windows that have different overall frequency and channel widths. The configuration of the spectral windows is limited by the hardware/software capability and the overall data rate.
{: .fs-2 }

The **correlators** of some observatories make such time-Fourier transformation for the signal transmitted from each antenna, and then cross-correlate the signals of every pair of telescopes to obtain *a(u, v)* and *p(u, v)* as functions of frequency. Such correlator is called **FX** correlator, where *F* and *X* stand for *Fourier transformation* and *cross-correlation*, respectively. There are also correlators that make the cross-correlation first to obtain the time series of *a(u, v)* and *p(u, v)*, and then make the time-Fourier transformation to obtain the information about the frequency domain. Such correlators are called **XF** correlators.
{: .fs-2 }

Modern correlators look like supercomputers. For example, a picture of the ALMA correlator can be found [here](https://www.almaobservatory.org/en/about-alma/how-alma-works/technologies/the-alma-main-array-correlator/).
{: .fs-2 }

### Observational planning

The ground-based astronomical measurements are subject to both the *atmospheric effects* and the *errors in instrumental responses*. These effects can be seen in the time or frequency domain. As we mentioned before, we need to plan the observations in a way such that our data can be calibrated.
{: .fs-2 }


###### Target source loop

The atmosphere deflects the incoming light. When the atmosphere is perturbed, for example, by some turbulent motion in the atmosphere, it will look like the stars are wobbling around their mean locations. In the optical or infrared astronomy, this is described by a quantity called **[seeing](https://en.wikipedia.org/wiki/Astronomical_seeing)**.
{: .fs-2 }

When the seeing effect is serious, if you take a series of CCD images on a tracked star with very short integrations (i.e., snapshots), the star will locate at different pixels (relative to your tracking center) in different images. If you make a long CCD integration, the star will become a big blur instead of a sharp spot.
{: .fs-2 }

A similar effect also occurs in your radio or (sub)millimeter interferometric observations. Since the positions of the celestial source are constrained by phase *p(u, v)*, **turbulence in the atmosphere induces phase errors**. The longer is a baseline (i.e., roughly speaking, the better angular resolution you use), the more it is sensitive to a small perturbation in the atmosphere. If you try to analyze the phase-uncalibrated data, it will appear like the target source structures are spatially smeared. In most cases, if you try to produce images out of phase-uncalibrated interferometric data, the images will look so rough such that no analysis can be made.
{: .fs-2 }

 So we need to know *what are the phase errors for each baseline at each time* and then calibrate the phase errors out in the post-processing.
{: .fs-2 }

To know what are the phase errors at a certain time, we can observe a reference source, in which the location and structure (or say, phase) have been well constrained by the previous observations. We refer to such a reference source as the **gain-phase calibrator** (or simply, **gain calibrator**). Let's call such a previously constrained phase the *true phase*. We can then deduce the phase errors by measuring how much the observed phase deviates from the true phase. Usually, we then plan our observations in a sequence like
{: .fs-2 }

gain -> target -> gain -> target -> gain -> target -> gain
{: .fs-2 }

We refer to this sequence of observations as the **target source loop**. The valid target source observations need to be sandwiched by the scans on the gain calibrator(s), such that you can interpolate (in time) the *phase errors you derived from the gain calibrator(s)* to your *target source scans*. If you have multiple target sources that are close by, you can replace *gain -> target -> gain* with either  *gain -> target1 -> gain -> target2 -> gain -> target3 -> gain* or *gain -> target1 -> target2 -> target3 -> gain*, and so on.
{: .fs-2 }

You need to observe the gain calibrator(s) frequently enough. Otherwise, the phase errors will look like jumping around stochastically and the interpolation will not be possible. Exactly how frequently you need to observe the gain calibrator(s) depends on the weather condition and your angular resolution. Taking the SMA for example, usually the following three scans *gain -> target -> gain* (including slewing time) have to be observed within 15-20 minutes (I personally prefer 15 minutes). We call this duration the **calibration cycle time**. The ALMA observatory plans the calibration cycles for the users. So you do not need to worry about such details. The JVLA is providing a [table](https://science.nrao.edu/facilities/vla/docs/manuals/obsguide/calibration#section-15) (There is only one table in this webpage. Just scroll down to it.) for the recommended calibration cycle time at various wavelengths and array configurations. You can see that in the high-frequency (e.g., 30-50 GHz) operations of the JVLA and in the extended array configuration (e.g., A or B), we need to rapidly switch between the observations on the target source and the gain calibrator. The cycle time of such observations can be as short as ~2 minutes. We refer to such observing strategy as the **fast-switching** technique.
{: .fs-2 }

If we make an analogy to optical or infrared photometric imaging observations again, this **gain-phase calibration** strategy is like we use a very fast camera to monitor the wobbling motions of a very bright star. Then we *undone* these motions to all of the stars that are near this bright star, before integrating the signals in the time domain.
{: .fs-2 }

Is there a tip for choosing the gain calibrator?
{: .fs-2 }

We need to know its location and structure before making our *calibrated* radio or (sub)millimeter interferometric observations. In general, this is not possible. There is an exception. The high redshift quasars are very far from us, such that they can be approximated as point-sources (note that this assumption sometimes breaks down when we are performing very high angular resolution observations using the JVLA, VLBA, VLBI, or EHT). If we put the phase referencing center on the location of a quasar, then the true *p(u, v)* should be zero and the true *a(u, v)* should be a constant for all probed *(u, v)*. This simplified our derivations of phase errors. The hosts of quasars are supermassive black holes. The flux densities of the quasars can vary on the characteristic timescales that are comparable to the orbital timescales (*t<sub>q</sub>*) of the [innermost stable circular orbits](https://en.wikipedia.org/wiki/Innermost_stable_circular_orbit) around these black holes. The value of *t<sub>q</sub>* is determined by the masses of the host black holes: the more massive a black hole is, the longer is *t<sub>q</sub>*.  For the Galactic supermassive black hole, Sgr A\*, *t<sub>q</sub>* is on the order of some minutes. Most of the quasar hosts are around 100 times more massive than the Sgr A\*, such that their *t<sub>q</sub>* are a few days. Over a few hours' observations, the flux densities of these quasars may be approximated by constants. Therefore, we can also calibrate the time-varying instrumental response of the *a(u, v)* based on the observations of these **gain calibration quasars**. We call the derivation of the time-dependent amplitude calibration solution the **gain-amplitude calibration**. Gain-amplitude and gain-phase calibrators together are called **complex-gain calibration** or simply **gain calibration**.
{: .fs-2 }

The gain calibrator has to be bright enough such that each of your baselines can detect it at a high signal-to-noise ratio within a relatively short time. In addition, it has to have a small angular separation from your target source, such that (i) the atmospheric effects on your target source can be approximated by the atmospheric effects on this gain calibrator (i.e., they are more or less on the same part of the sky), and (ii) it does not take too much time to slew your telescopes back-and-forth.
{: .fs-2 }

If you need a very long integration time on the gain calibrator to detect it, for example, a whole night, then you cannot resolve the time dependence of the phase errors which is required in the data calibration. You actually want to spend your precious observing time integrating on your target source instead of the gain calibrator. So we should try to pick a bright gain calibrator unless there is nothing bright near our target source.
{: .fs-2 }

How bright the gain calibrator needs to be? It depends on the sensitivity of your telescopes. Many modern observatories provide online sensitivity estimators. You can use them to check: *given the total bandwidth of your observations, how bright a source needs to be such that you can achieve 5~10 sigma detection in ~2~5 minutes*. Ideally, if there is a very bright gain calibrator close to your target source, your gain calibration scans can have a shorter duration. However, in practice, some observatories take time for the hardware to stabilize after slewing to a new position. If you use a duration that is too short, in some cases there could be a high risk that some gain calibration scans fail. In such cases, the target source scans observed before and after the failed gain calibration scans cannot be gain calibrated. Therefore, sometimes, there can be a minimally allowable scan duration. For the JVLA, it is 20 seconds (i.e., all scans need to have >20 seconds durations). If you use an observatory for the first time and are not sure about what is the best to do, you should double check with the experienced users of the observatories, e.g., they may say, for the SMA, picking a >0.7 Jy source and observe 2~5 minutes would be OK.
{: .fs-2 }

There are occasions that the structures of our target sources have been constrained by previous observations (e.g., at other wavelengths), or the structures are relatively simple (e.g., it is dominated by a bright point-like maser source at a certain frequency). In such cases, we can also use the observations on the target source to derive phase errors. We call this technique **self-calibration**. Usually, it is an iterative procedure between reconstructing the structures of your target sources and refining the derivations of the phase errors. If you can self-calibrate the target sources, you may observe the gain calibrator less frequently. This is very important to enable some high-frequency projects of the JVLA. However, mathematically, there is no guarantee that the self-calibration iterations will converge (or converge correctly). Moreover, after performing self-calibration, you will lose the information of absolute astrometry (i.e., the precise location of your target source) in spite that the structures may be recovered. The astrometry problem may not always be serious if your observations are redundant (e.g., if you are using a big array such as ALMA). If you try to compare the observations at multiple frequencies, you should think carefully whether or not you want to self-calibrate your data, or whether or not you want to trust the scientific results derived based on self-calibrated data. Losing astrometry at some frequency bands sometimes can make your derivation of spectral indices wrong, for example.
{: .fs-2 }

###### Special consideration for wide-field mosaic observations (mega-mosaic)

**(under construction)**


###### Before or during the target source loop

We refer to the direction that the peak of the antenna response function is pointing to as the **pointing center**. Note that the *pointing center* and *phase referencing center* have a different concepts.
{: .fs-2 }

Ideally, when you are observing a target source or a calibrator, both the pointing center and phase referencing center have to co-locate with that target source or calibrator. Observing the source at the pointing center provides the best achievable sensitivity. We call such observations the **on-axis** observations, otherwise, **off-axis** observations.
{: .fs-2 }

In practice, it is easier to maintain the accurate location of the phase referencing center. The pointing center for each telescope can have a time-dependent offset. The offset can be caused by the deformation of the dish due to the (i) time varying thermal profile in the dish, (ii) strong wind, and (iii) gravity. When these effects are very serious, that is, when the point errors are very large (which can be different at different telescopes), it can happen that the target source or calibration is observed outside of the primary beams. This is particularly true when we are operating at high frequency (e.g., 20-50 GHz in the case of the JVLA).
{: .fs-2 }

Usually, the operator on-site will stow the telescopes when the wind speed is higher than certain limits.
{: .fs-2 }

To mitigate the thermal effect, we usually specify that we want to perform **reference pointing calibration** after sunrise and sunset. The calibration is done by observing a bright point-like source. The calibration solution is derived, validated, and applied on-the-fly. We do not need to worry about this part in the post-processing. When using the SMA, we also often break the target source loop after the transit of the target source and gain calibrator, to perform a reference pointing calibration.
{: .fs-2 }

With the high-frequency observations (>20 GHz) of the JVLA, you need a reference pointing calibration before the first scan on the absolute flux calibrator, passband calibrator, (and polarization calibrators if they are included), and the target source loop. The daytime JVLA operation at high-frequency will require you to break the target source loop approximately every ~30 minutes to make reference pointing calibrations. In the nighttime, making a reference pointing calibration every hour may be OK (roughly saying, when the accumulated AZ or EL change after the previous pointing calibration is more than 20 degrees).
{: .fs-2 }

When you are calibrating your observations in the postprocessing, you do not need to do anything with the pointing calibration data. You only need to make sure that you are not using such data since many of those scans were taken off-axis (due to the need of deriving pointing calibration solutions). Sometimes, the pointing calibration solutions may be poor. In that case, you may notice that the amplitudes of some telescopes show funky time variability. You need to flag those data as bad data and avoid using them in the calibrations or scientific analysis.
{: .fs-2 }

###### Before and/or after the target source loop

 The instrumental amplitude and phase responses not only vary in time but also in frequency. To comprehend the frequency-dependent amplitude response, you can make an analogy to the [*filter response*](https://en.wikipedia.org/wiki/Photometric_system) in the optical and infrared photometric observations. Our terminology is similar to that of the optical and infrared community. We refer to the frequency-dependent amplitude response as the **passband amplitude**. Similarly, we refer to the frequency-dependent phase response as the **passband phase**. The calibration of these effects is namely the **passband calibration**, and the calibrator observed for this purpose is called the **passband calibrator**.
{: .fs-2 }

In modern radio observatories, the passband amplitudes and phases usually have a dependence on antennae (i.e., telescope), i.e., the errors in all baselines can be factored to some terms, each of which only depend on the antennae. For example, if the signal-cable connecting a telescope-A with the correlator is stretched a little bit for any reason, on the scales comparable to a fraction of the observing wavelength, this stretch will induce a small **delay error**.  Such a delay, which can be expressed in length or time unit (e.g., 0.1 millimeter or 0.1 millimeter divided by light speed), corresponds to different wave numbers at different wavelengths. The net effect is a phase error that depends linearly on the observing frequency, which will be seen from all baselines that involve telescope-A. We call the errors that can be factored to the contribution by individual antennae the **antenna-based errors**. The errors that have a dependence on individual baselines are called **baseline-based errors**. When you are deriving the calibration solutions, the software usually allows you to choose whether you want to assume that the errors are antenna-based or baseline-based. In most cases, antenna-based errors are good assumption while you should double check the quality of the calibration solution. There are cases that you cannot find good antenna-based solutions such that switching to a baseline-based assumption becomes necessary.
{: .fs-2 }

The passband errors are usually stable over a night of observations. This is the case for the SMA, JVLA, and ALMA observatories. That is, we only need to measure the passband amplitudes and phases at a certain time. Then we can apply the **passband calibration solutions** to the rest of the observations taken on that night.
{: .fs-2 }

Similar to the case of complex gain calibration, using a high redshift quasar as a calibrator makes it easy to derive the passband phase. In addition, the radio and (sub)millimeter emission from a quasar is dominated by synchrotron emission that the flux density varies with frequency as a very smooth power-law. If you are observing over a relatively small frequency range, you can approximate its flux density as a constant of frequency over the frequency coverage of your observations. Then, in the frequency domain, the deviation of the observed amplitudes from a constant can be translated to your passband response straightforwardly.
{: .fs-2 }

What is different from the complex gain calibration is that,  *passband calibration requires a high signal-to-noise ratio in a small frequency range*, while complex gain calibration can use the aggregated signal from all available bandwidth. Therefore, the passband calibrator needs to be very bright, such that you can obtain good enough signal-to-noise ratios from the observations within a few tens of minutes.
{: .fs-2 }

A night is only 10~12 hours more or less. You do not want to spend too much of it on calibrations unless it is unavoidable, and you do not want to etch your target source loops with a long calibration scan. Usually, what we do is pick a very bright quasar that can be observed before or after your target source loop as our passband calibrator. There are not so many of them although bright is a relative sense. The more sensitive is your observatory, the fainter quasars you can use as passband calibrators. Presently (in 2022), for the SMA observations in the summer and winter semesters, quasars 3C279 and 3C84 are good passband calibrators. When you are conducting the continuum observations instead of spectral line observations, the bright blazar BL Lac can also be used as a passband calibrator. BL Lac is right behind a high-density Milky Way molecular cloud. In some narrow frequency ranges (e.g., around the CO J=2-1 central frequency 230.530 GHz), the passband amplitudes can confuse with the absorption line feature, making the calibration relatively complicated. 3C111 used to be an option of passband calibrators that share the same problem with BL Lac, although 3C111 is not so bright presently. The ALMA observatory will pick a passband calibrator for your project. When using the ALMA observatory, you only need to keep an eye that your calibrator is not known to be right behind a dense molecular cloud and is not your target source (e.g., when your science purpose is observing a bright quasar, it can happen that the selected calibrator is identical to your target source, which can induce problems in some cases).
{: .fs-2 }


Finally, the raw signal you obtain from the correlators may have voltage or electric current units, otherwise, arbitrary units. To convert them to the astrophysically meaningful units, you need to observe a target source that the absolute flux density is already known. This is analogous to the observations on the [*standard stars*](https://www.eso.org/sci/observing/tools/standards.html) in the optical or infrared observations. We call such calibration sources the **absolute flux calibrators**. For the (sub)millimeter observations, the best choices are planet (if your array is not too extended such that the planet is resolved out) or planet moon (e.g., Callisto, Ganymede, if they are reasonably well separated from the host planet in the night of your observations). At (sub)millimeter wavelengths, the frequency-dependent absolute flux densities of such Solar System objects are dominated by dust thermal emission which is stationary over a night. We can model them based on the following information: the distance from the Sun and from the Earth, the phase angle (e.g., are we looking at the day or night side), and the absorption and scattering opacity of its surface. The model evaluates the rate for the object to convert the Sunlight (dominated by optical bands) to (sub)millimeter thermal emission.
{: .fs-2 }

The SMA almost always uses the Solar System absolute flux calibrators, or sometimes a well-monitored young star [MWC 349A](https://en.wikipedia.org/wiki/MWC_349) which is a thermal emission source at (sub)millimeter wavelength. ALMA sometimes uses the Solar System objects as absolute flux calibrators, and sometimes uses quasars of which the absolute flux densities are constrained within a week of your observations by the **[ALMA Calibrator Grid Survey](https://almascience.eso.org/alma-data/calibrator-catalogue)**. The JVLA uses only [a handful of quasars) (https://science.nrao.edu/facilities/vla/docs/manuals/oss/performance/fdscale) of which the flux densities are relatively stationary (e.g., 3C286, 3C147, 3C48, 3C138). Unfortunately, the latter two have been flaring since 2018 so need to be used with caution.
{: .fs-2 }

The calibration for the full polarization observations is a relatively advanced topic. You need to calibrate the **absolute polarization position angle** and the **polarization leakage**. Sometimes, different observatories required a different strategy for polarization calibrations. I assume that polarimetry is not what you are doing. I am assuming that you are a beginner to use radio interferometry. If you are already an advanced user and if you are interested in polarimetry, please read the following two papers at least: [Hamaker et al. (1996)](https://ui.adsabs.harvard.edu/abs/1996A%26AS..117..137H/abstract) and [Sault et al. (1996)](https://ui.adsabs.harvard.edu/abs/1996A%26AS..117..149S/abstract). I learned polarimetry from these two references and I have not seen any introduction that is more transparent, although it would be good if someone can create a beginner-friendly version. This is not necessarily possible though.
{: .fs-2 }

**As a summary, here is a *check list* of what you need to do with the observational planning (if you are not doing polarimetry):**
1. **Is your frequency tuning (including the details of how you set up individual spectral windows if you are using the JVLA or ALMA; you do not need to worry about the spectral windows when using the SMA which takes the default).**
  - Are you using good enough spectral resolution for your spectral lines?
  - Are your spectral windows coverage big enough frequency width, and are you tracking the correct source velocity?
  - With JVLA, you need to make sure that you are not using too many spectral channels such that the data rate exceeds the maximally allowable data rate.
2. **Are the target source coordinates correct? If you are using the JVLA or ALMA, you need to double-check whether or not you are tracking the velocities of your track sources. If you do not pay attention to this, in some cases, the spectral lines can be redshifted/blueshifted to a frequency that is well outside of your spectral window. The SMA usually does not have this problem since the frequency coverage is very big.**
3. **Have you included an absolute flux calibrator? Is it resolved out?**
4. **Have you included a passband calibrator?**
5. **Have you picked suitable complex gain calibrators for the individual of your target sources?**
6. **Are gain calibrators observed at good enough signal-to-noise? Is the calibration cycle time fair? With the JVLA or SMA, you need to make sure that the slewing time does not give you surprises (e.g., spending all time in the slewing but no time on target sources, etc).**
7. **Is your integration time appropraite?**
8. **When using the SMA or JVLA, if you are using a relatively compact array configuration, you need to double check that the dishes on the telescopes do not seriously shadow each other. With the SMA, that is simply done by setting the correct elevation limit. With the JVLA, this is done by optimizing the starting Local Sidereal Time (LST) and the overall duration of your scheduling block**
9. **Have you specified the sufficient reference pointing calibrations**
{: .fs-3 }

### Data calibration
