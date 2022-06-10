---
layout: default
title: Radio Interferometry
parent: Basic Astrophysics
grand_parent: To my students
nav_order: 9
---

### Radio Interferometry (or, aperture synthesis technique)

#### Why interferometry?

Analyzing interferometric data can be hard. It has been a nightmare to many astronomy/astrophysics students. This technique worths 0.5 Nobel Prize ([to Sir Martin Ryle, in 1974](https://www.nobelprize.org/prizes/physics/1974/summary/)).
In my experience, it takes a full-time student 2-6 months to master this technique, to the level that they can process data and troubleshoot independently. During this time period, both the trainer and trainee need to devote considerable amount time. So, in fact, most of our colleagues do not pick it up. People who have mastered radio interferometry are relatively unique.
{: .fs-2 }

So why use interferometry at all? How does it pay off?
{: .fs-2 }

**This is all about the need for resolution.**
{: .fs-2 }

For a telescope, with a lens or reflector that has a diameter *D*, at a wavelength *L*, the angular resolution is approximately **L/D [in units of radian]** (i.e., to convert it to arcsecond unit, you multiple *L/D* by (180/pi)\*3600 ). At a certain wavelength, if you want to achieve better and better angular resolution, then you need to build bigger and bigger telescopes. This is particularly bad when you are observing at (sub)millimeter or radio (i.e., centimeter or decimeter) wavelength bands. In such cases, the *L* is much longer than the that in the optical or near-infrared observations.
{: .fs-2 }

For example, presently, the biggest movable *single-dish* radio telescopes are the [Green Bank 100-meter telescope](https://greenbankobservatory.org/science/telescopes/gbt/) and [Effelsberg 100-meter telescope](https://www.mpifr-bonn.mpg.de/en/effelsberg).  Beyond this size, it becomes unrealistic to find material that is hard enough to make the mechanical structures. The surface of such big single-dish telescopes may considerably deform when you slew the telescope, due to gravity. It also deforms when the wind is blowing. To alleviate mechanical problems, the bigger radio telescopes are not movable, for example, the [Arecibo](https://en.wikipedia.org/wiki/Arecibo_Observatory) telescope and the [FAST](https://en.wikipedia.org/wiki/Five-hundred-meter_Aperture_Spherical_Telescope) observatory. The observations with such static dishes are subject to some limitations, as expected.
{: .fs-2 }

The radio interferometry technique sheds light on this problem. Based on physics/mathematical principles, we can build an **array** of telescopes that have small dishes. The interferometry technique allows us to to-some-extent take this array as an equivalent, big single-dish telescope, of which the diameter is comparable with the **largest projected separation** of the smaller telescopes in our array. Here, projection means we project the spatial distribution of the array to a plane that is perpendicular to the line-of-sight toward the astronomical source being observed.
{: .fs-2 }

Fortunately, we are coming to the era that the big interferometric radio or (sub)millimeter observatories (e.g., [ALMA](https://www.almaobservatory.org/en/about-alma/)) are offering good support. Nowadays, one can choose to use some of them in a way that most of the complicated mathematical principles are hidden from the user. To enable you to use [ALMA](https://www.almaobservatory.org/en/about-alma/) this way, or make query to the [archival observations of ALMA](https://almascience.nao.ac.jp/aq/), in the following, I will introduce some of the basic terminologies. Then I will introduce how we normally use these interferometric observatories. It will mostly stay at a qualitative level, which intends to be a minimal set of knowledge that you need to know before using ALMA like taking a picture with a point-and-shoot camera. If I have time, I may host the mathematical details at other places for the advanced users (when I find time). The details about the ALMA hardwares can be referenced from the official ALMA [Technical Handbook](https://almascience.nao.ac.jp/proposing/technical-handbook). If you want to be a black belt ALMA user, at some point, it may become inevitable to read through this very thick technical handbook.
{: .fs-2 }

#### How a radio interferometer look like?

###### Looking from outside

You can find the pictures of the modern radio or (sub)millimeter interferometers such as the [SMA](http://sma1.sma.hawaii.edu/smaoc.html) (200-400 GHz), [ALMA](https://www.almaobservatory.org/en/about-alma/) (90-1000 GHz), [JVLA](https://www.almaobservatory.org/en/about-alma/) (0.05-50 GHz), [GMRT](http://www.gmrt.ncra.tifr.res.in/) (0.1-1.5 GHz), [ASKAP](https://www.atnf.csiro.au/projects/askap/index.html) (0.7-1.8 GHz), [MeerKat](https://www.sarao.ac.za/gallery/meerkat/) (0.6-15 GHz), [VLBA](https://science.nrao.edu/facilities/vlba) (0.3-90 GHz), [EHT](https://eventhorizontelescope.org/array) (230 GHz), and so on. These are the *dish arrays* (i.e., each element in the array is a single-dish telescope). I will focus more on the dish arrays in the following.
{: .fs-2 }

Besides dish array, there are also radio interferometers that are composed of dipole antennae without dishes, such as [LOFAR](https://www.astron.nl/telescopes/lofar/), [LWA](https://leo.phys.unm.edu/~lwa/index.html), [OVRO-LWA](http://www.tauceti.caltech.edu/LWA/). They are operating at low frequency bands (<1 GHz, typically). The interferometric principles they are based on are the same as that for the dish arrays. However, the response functions of  is these diple antennae are very different. Usually, these dipole arrays can simultaneously observe the whole sky. OVRO-LWA performing all sky monitoring routinely. Otherwise, they can use the *[beamforming](https://en.wikipedia.org/wiki/Beamforming)* technique to observe some selected patches on the sky with high angular-resolution.
{: .fs-2 }

The dish collects the incoming light. The bigger the dish size, the more light it can collect in a unit of time, meaning that the **sensitivity** is better. For both single-dish telescope or interferometry, **sensitivity** is usually expressed in intensity units, which has dimension of *energy per unit area per unit solid angle per unit time per unit observing-frequency*. For instance, we can express the sensitivity as the intensity of an equivalent black body, e.g., we say our brightness sensitivity is 1 Kelvin. This means that, after we produce an image, which includes both the *emission of the target source* and the *thermal white noise*, the root-mean-square of the intensity fluctuation contributed by the thermal white noise corresponds to the intensity of the black body emission at 1 K temperature. We call the temperature of such equivalent black body the **[brightness temperature](https://en.wikipedia.org/wiki/Brightness_temperature)**. For most of the present-date radio or (sub)millimeter interferometry, the noise statistics are indeed approximately Gaussian (i.e., white). Then for example, if your target source is a 6000 K black body emitter, for example, our Sun, and if you want to resolve it at 10-sigma significance, then you need to achieve an rms noise level of 600 K. An ALMA image on the Sun can be found [here](https://www.almaobservatory.org/en/announcements/alma-starts-observing-the-sun/).
{: .fs-2 }

The longer you integrate on the target source with the observations, the better sensitivity (i.e., the lower rms noise level) you can achieve. Since the noise follows the Gaussian statistics, the noise level is inversely proportional to the square-root of the on-source integration time. Having a bigger dish, you can achieve the same noise level with a shorter on-source integration time.
{: .fs-2 }

In astronomical observations, we also often express intensity or sensitivity in the unit call **Jy beam<sup>-1</sup>** (pronounced as Jansky per beam). [Jy](https://en.wikipedia.org/wiki/Jansky) is the unit for flux density, which has a dimension of  *energy per unit area per unit time per unit observing frequency*, i.e., flux density is integrated intensity over solid angle (e.g, the solid angle of your target source). *Jansky per beam* denotes the flux density in a *unit resolution element* in your image. If your resolution element is a Gaussian beam, you can convert between the brightness temperature and the Jy beam<sup>-1</sup> based on the formula given in [this page](https://science.nrao.edu/facilities/vla/proposing/TBconv).
{: .fs-2 }

So what is the *unit resolution element*? As a start, you comprehend it as a shape (e.g., a circle) which occupies a certain solid angle in the image domain.
It is only slightly more complicated than that. Precisely speaking, the **resolution** describes the *angular response function* of your telescope. For a single-dish radio telescope that the dish diameter is *d*, at observing wavelength *L*, that response function may be approximated by a two-dimensional gaussian that has a [full-width-at-half-maximum](https://en.wikipedia.org/wiki/Full_width_at_half_maximum#:~:text=In%20a%20distribution%2C%20full%20width,half%20of%20its%20maximum%20value.) around 1.22 times *L/d*. The solid angle of that response function can be obtained by integrating over the whole angular range. If you are interested in the mathematical details, you can check Section 3.3.3 of [this page](https://www.cv.nrao.edu/~sransom/web/Ch3.html).
{: .fs-2 }

For an interferometer array, the response function provided by the dish, *L/d*, is your **simultaneous field-of-view**. We call this simultaneous field-of-view the **primary beam** of the observations. The longer wavelength you observe, the bigger simultaneous field-of-view (or primary beam) you have. The emission from target sources that are located outside of the primary beam is significantly attenuated.
{: .fs-2 }

The resolution element of a modern interferometer array (e.g., ALMA) is also approximately a two-dimensional gaussian, although the major and minor axes may not be equal. So you need to describe this two-dimensional gaussian resolution element with the major axis, minor axis, and position angle, e.g., it is often expressed as something like (0".5 x 0".5; P.A.=10 degree). We call this resolution element a **synthesized beam**. The major and minor axes of this resolution element is determined by the largest projected separations *B<sub>max</sub>* of the telescopes in the interferometer array. That is the major or minor axis of the resolution element is approximately *L/B<sub>max</sub>*. A very special aspect is that the smallest projected separations *B<sub>min</sub>* (e.g., 1000 meters) of the telescopes determins the **largest recoverable angular scale** of your interferometric observations. The observed intensity of any structure that is spatially more extended than *L/B<sub>min</sub>* will be very significant attenuated. That is, an interferometer is working like a spatial high-pass filter.
{: .fs-2 }

Note that if you express the sensitivity of an interferometer in units of Jy beam<sup>-1</sup>, the sensitivity will be independent of the solid angle of your synthesized beam. We say that the point-source sensitivity of an interferometer is independent of angular resolution. However, if you express it in units of Kelvin, it will be better (i.e., corresponds to a lower temperature) if you are using a coarser angular resolution (i.e., a synthesized beam with a bigger solid angle).
{: .fs-2 }

The values of *B<sub>max</sub>* and *B<sub>min</sub>* are determined by the **array configuration**, which describes how you locate the telescopes in an array. Many modern interferometers (e.g., ALMA, SMA, JVLA) can reconfigure the array, i.e., moving telescopes from certain pads to the others. SMA has four different array configurations, namely the subcompact, compact, extended, and very extended array configurations. The most extended array configuration offers the best achievable angular resolution, however, also filters out a lot of extended emission. To recover the extended emission, we can combine the observations taken with the observations taken in the compact array configuration, and the observations taken with the single-dish telescopes. Similarly, ALMA has the C-1, C-2, ..., C-10 array configuration (from the most compact to the most extended), and JVLA has the D, C, B, and A array configurations (from the most compact to the most extended). JVLA rotate throughs these four array configurations approximately every 1.5 years (see the [array configuration schedule](https://science.nrao.edu/facilities/vla/proposing/configpropdeadlines)). For a student, it is good to keep in mind when you should propose the observations you need, otherwise, you may miss the timeline for graduation!
{: .fs-2 }

There are also optical and infrared interferometers, for example, the [Very Large Telescope Interferometer (VLTI)](https://www.eso.org/sci/facilities/paranal/telescopes/vlti.html) and the [CHARA](https://www.chara.gsu.edu/). They can achieve extremely high angular resolution thanks to the short operational wavelengths. Looking from outside, they appear very similar to the radio or (sub)millimeter interferometer arrays. But the receiver techniques and the way to correlate signals from individual telescopes are very different from those of the radio or (sub)millimeter interferometer arrays. For the radio or (sub)millimeter interferometer arrays, these aspects are introduced in the following.
{: .fs-2 }

###### Inside the receiver cabin

#### Observational planning and data calibration

**This part is under construction** For this moment, please go to watch the videos at [2022 Submillimeter Array Interferometry School](https://lweb.cfa.harvard.edu/sma-school/program/)
{: .fs-2 }
