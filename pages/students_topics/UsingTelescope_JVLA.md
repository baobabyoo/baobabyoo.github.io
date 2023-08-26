---
layout: default
title: JVLA
parent: Telescopes Tips
grand_parent: To my students
nav_order: 2
---

### If this is your first time

If you are my postdoc, and if you need me to revise English or double check the technical setup, forward me your first draft at least **2 weeks** ahead of the proposal deadline.
{: .fs-1 }

If you are my student, forward me your first draft at least **4 weeks** ahead of the proposal deadline. I will spend time iterating with you many times for education purposes.
{: .fs-1 }


### Chapter 1. Proposing

#### 1.1 Timeline and interface

**There are two proposal deadlines each year, usually on February 01 and August 01 except when these dates are in the weekends.**
{: .fs-2 }

Please register an **account** at the [NRAO graphical interface](https://my.nrao.edu/) well ahead of the proposal deadline (e.g., one month ahead or earlier). You need to log in and familiarize yourself with how to prepare for the cover-page online. In addition, all of your co-Is will need to register to this interface otherwise they cannot be included. You need to inform your co-Is early enough such that the have time to process this.
{: .fs-2 }

The JVLA capability has been evolving. Please read the [Call for Proposals](https://science.nrao.edu/observing/call-for-proposals) well ahead of the deadline to understand what capability has become available for your experiment(s). In each proposal deadline, the available array configuration(s) is also different. Please check the [Array Configuration Schedule](https://science.nrao.edu/facilities/vla/proposing/configpropdeadlines) well ahead of the deadline and check the [Angular resolution and Largest Angular Scale](https://science.nrao.edu/facilities/vla/docs/manuals/oss/performance/resolution) of the available array configuration(s). This is necessary information for planning your experiment(s).
{: .fs-2 }

Usually, you try to form a rough idea about what you are going to propose (target source(s), array configuration, frequency band(s) and correlator setup, and sensitivity). Let's say, this is at least 1~1.5 months ahead of the proposal deadline. If you are my student and postdoc, please come discuss with me about this rough idea.
{: .fs-2 }

Note that it is almost impossible to observe a target source that is at lower than -35 degree declination.
{: .fs-2 }

#### 1.2 Preparation-1: Feasibility, complementary data, and duplication

**After we agree that this idea is worth pursuing and is technically feasible
, you should use the [NRAO Data Archive](https://data.nrao.edu/portal/) to check whether or not you are duplicating historical or ongoing projects.** In the case that you are duplicating, you can (1) give up and try to come up with other proposal ideas, or (2) download the archival data can see if the calibrated data can achieve the quality that is needed for your science purpose. If the quality of the archival data is fair, then just continue to use that data to proceed with your research. If there is no archival data or if the quality of the archival data is poor, you can go ahead to complete the preparation of your proposal. **You need to explicitly and convincingly explain what was the problem with the archival data if it exists. So prepare your proposal well ahead of the deadline** in case you really need to look into some archival data or need other colleagues to check the archival for you. Close to the deadline, they (and I) have to prepare their own proposals thus may refuse to help you.
{: .fs-2 }

**Do not waster your (and my) time to prepare a proposal that has a problem with unnecessary duplication. Such proposals will be rejected for 100% sure.**
{: .fs-2 }

When making the duplication checks mentioned above, you may find that there are other observations on your target source(s) which can help your science case to some extent although they do not fully resolve the problem. For example, you may find that some short-spacing observations for your high-angular resolution experiment already exist. In this case, **explicitly mentioning how** you will make use of such complementary data in the proposal is a plus. Just mentioning you will use those data but without saying how usually does not help. If you have also checked the data archive of the observatories (e.g., ALMA, SMA, Herschel, Spitzer, etc) and found some useful complementary data, you can also mention how you will make use of them in a joint analysis. You might find some historical VLA images using the [NRAO image archive](http://www.aoc.nrao.edu/~vlbacald/ArchIndex.shtml). Sometimes this helps your proposal preparation.
{: .fs-2 }

#### 1.3 Preparation-2: Scientific justification and technical details

To complete the proposal submission, you need a **title**, an **Abstract**, a PDF scientific justifications with **2 pages of text and 2 pages of Figures/Tables**. If you are not sure about how to compose the Abstract or the 2+2 pages scientific justification, check [here](https://baobabyoo.github.io/pages/students_topics/proposal_obs.html).
{: .fs-2 }

Usually, we prepare the 2+2 pages justifications using LaTEX. If you are my student/postdoc, please use the [Overleaf](https://www.overleaf.com/) interface and share the link with me, *if you need my revision*. Use **fontsize 12** as far as you can. *Never make fontsize smaller than 11.* Do not use a very small margin. Try not to make your proposal over texty. No reviewer wants to spend more than **5 minutes** reading your proposal. Do not make it necessary for them to do so.
{: .fs-2 }

You will need to fill the technical details through the online interface. There are a lot of items to fill and many of them can be very complicated. Do prepare early unless you are already very experienced.
{: .fs-2 }

******************************************************************************

If you are proposing continuum experiment(s), you can simply use the standard 3-bit setup (or 8-bit if you are observing at L or S bands). If you want to change the correlator setup, you need to double check the maximum allowable data rate from [this page](https://science.nrao.edu/facilities/vla/docs/manuals/oss/proposing), and check the [VLA Frequency Bands and Tunability](https://science.nrao.edu/facilities/vla/docs/manuals/oss/performance/vla-frequency-bands-and-tunability). You can validate your **correlator setup** using the [GHOST tool](https://science.nrao.edu/facilities/vla/docs/manuals/propvla/gost). Download this java tool and use the linux command `javaws latestGOST.jnlp` to launch it. It is **necessary** to re-download the latest version after the call for proposals was issued. When you are proposing a spectral line experiment, it is mandatory to use it and attach a screenshot to your proposal.
{: .fs-2 }

You can check the **sensitivity** *at your observing frequency* using the online [Sensitivity Estimator](https://obs.vla.nrao.edu/ect/). You need to export the sensitivity estimates using this page and attach to your proposal.
{: .fs-2 }

******************************************************************************

#### 1.4 Preparation-3: Scopes (being sufficiently ambitious)

A regular JVLA proposal usually requests from a few hours to a few tens of hours of observing time **for each array configuration**. Usually we try to limit the Ka and Q band time to <15 hours but there is not a hard rule for this. When your scientific goal is important and concrete, you should request the observing time that is needed to achieve your goal. Since 2021, there is an extra-large proposal category (X-proposal) that allows you to request up to 1000 hours of observing time. If you want to submit a X-proposal, prepare early.
{: .fs-2 }

If you are a Ph.D. student who already know what is your thesis project, and if your thesis project requires JVLA observations, do prepare the proposal early and submit the extra [Dissertation Plans](https://science.nrao.edu/observing/call-for-proposals/2023a/alerts-tips-for-proposers). It helps *DRAMATICALLY*. In this case, you can also propose observations for the future semester without being limited by what is stated in the [Array Configuration Schedule](https://science.nrao.edu/facilities/vla/proposing/configpropdeadlines). The request for the future semester(s) may be rejected. Nevertheless, this allows you to revise your proposal based on the Time Allocation Committee comments and then resubmit. It helps.
{: .fs-2 }

**Pick a problem that can be solved by such an investment resource.** You can think bigger once you have enough reputation to convince the reviewers that you can manage a larger-scale project.
{: .fs-2 }



### Chapter 2. Organizing observing scripts

You may find [this PDF document](https://events.asiaa.sinica.edu.tw/workshop/20120903/talk/EmmanuelMomjian1.pdf) useful.

You need to do it on the [NRAO online interface](https://my.nrao.edu/). It is recommended to use Firefox, although I sometimes also use Google Chrome. Other web browsers are not necessarily well supported. After you login, click the `Obs Prep` tab. Then click into `Login to the Observation Preparation Tool (OPT)` to launch the **OPT** interface.
{: .fs-2 }

You will see a complicated web-based interface. Before you do anything with it, you need to learn the following two things:
{: .fs-2 }

1. **The interface itself.** If this is your first time organizing a JVLA observing script, please carefully read this [tutorial](https://science.nrao.edu/facilities/vla/docs/manuals/opt-manual/opt-tutorial-1). For a full reference manual, you can click into [this page](https://science.nrao.edu/facilities/vla/docs/manuals/opt-manual).
2. **The concept of data calibration.** Please read through this [webpage](https://science.nrao.edu/facilities/vla/docs/manuals/obsguide/calibration).
{: .fs-2 }

After you have an idea, please open the proposal you submitted and the disposition letter. You will need to reference them when you are preparing the observing scripts.
{: .fs-2 }

#### 2.1 Receiver and correlator resources

The first thing you need to do is to configure the receiver and correlator resources. If you are performing standard continuum-mode observations, you can simply use the NRAO defaults. In that case, to prepare the resources, click the `Instrument Configurations` tab in the OPT interface. You will see the *NRAO Defaults* and *your project code* on the left. Click into the *NRAO Defaults* and then click into the relevant category. A list of receiver and correlator setups will appear on the right. You should be able to understand what they mean after reading the aforementioned  [tutorial](https://science.nrao.edu/facilities/vla/docs/manuals/opt-manual/opt-tutorial-1). Check the boxes for the ones that you are going to use, and then click `Edit`->`Copy`->`Instrument Cfgs`. Then click *your project code* on the left, and then click `Edit`->`Paste`->`Instrument Cfgs` to paste it into your project.
{: .fs-2 }

This task is a lot more complicated when you are performing spectral line observations. Please read into the details of
[this page](https://science.nrao.edu/facilities/vla/docs/manuals/oss/widar#section-7).
{: .fs-2 }

#### 2.2 Selecting calibrators

You need to understand the JVLA calibrator list from [this page](https://science.nrao.edu/facilities/vla/observing/callist). In particular, you need to pay attention to the meanings of the **calibrator quality code**. To prepare the calibrators for your project, in the **OPT** interface, click the `Sources` tab in the OPT interface. You will see *VLA* and *your project code* on the left. You can click the plus sign on the left of the *VLA catalogue* on the left to unfold this catalog. Then you can look you the calibrators you will use (more below) in certain RA Groups. After you click into a specific *RA Group*, you will see a list of calibration quasar on the right. Check the box of your calibrator and then click `Edit`->`Copy`->`Sources`, and then click *your project code* on the left and click `Edit`->`Paste`->`Source` to copy it into your own project.
{: .fs-2 }

##### 2.2.1 Absolute Flux Calibrator

There are only a few options for the JVLA, which can be looked up on [this page](https://science.nrao.edu/facilities/vla/docs/manuals/oss/performance/fdscale). Pick the one that is close to your target source and avoid the one that is flaring.
{: .fs-2 }

##### 2.2.2 Gain Calibrator

In the **OPT** interface, click the `Sources` tab and then click the plus sign on the left of *your project code* to unfold it. You will see the list of your source groups. If you click into a specific source group, you will see the list of target sources in that group on the right. To find the gain calibrator that is close to a target source, click the `Sky Map` symbol in the right-most column. From the pop-up tab in your web browser, you can pick the suitable Gain calibrator that is bright, spatially compact enough for your observations, and is not too far from your target source.
{: .fs-2 }

There might be multiple options. When you are observing a large number of target sources in one scheduling block, you can try to make a combination that is minimizing the slewing time. If you have any question about slewing time, you are more than welcome to contact my Master's student [Chia-Ying Chung and Yuka Terada](https://baobabyoo.github.io/pages/members.html). She can help you with this as part of a collaboration.
{: .fs-2 }

##### 2.2.3 Passband Calibrator

This calibrator needs to be bright. It is also better that this calibrator is not extremely far from your target source, to avoid the long slewing time. For continuum observations, your absolute flux calibrator may also be used for this purpose. Otherwise, some sources I used before include 3C84, 3C273, 3C279, bllac, J1924-292, 3C454.3, and so on.
{: .fs-2 }

##### 2.2.4 Polarization Calibrator

If this is what you are doing, you should be a relatively advanced user already. You can find all the information you need on [this page](https://science.nrao.edu/facilities/vla/docs/manuals/obsguide/modes/pol). You can contact and ask me if there is something that you are not so sure about, otherwise, contact the NRAO helpdesk.
{: .fs-2 }


#### 2.3 Organizing scans

Usually, for the dynamically scheduled observations (which is most cases), the overall duration for a scheduling block is between **1~2 hours**. The scheduling block that is shorter than 30 mins will be dominated by overhead (hardware setup, calibration, slewing, etc); the scheduling block that is longer than 2 hours will have a very low chance to be dynamically scheduled.
{: .fs-2 }

In all cases, you will need the scans on **your target sources**, **gain calibrator(s)**, **passband calibrator**, **absolute flux calibrator**, and in the case of polarimetry, the **polarization position angle and cross-hand phase/delay calibrator*** and the **leakage calibrator**. In high frequency (Q, Ka, K, and sometimes, Ku bands) observations, you will also need to include **reference pointing calibration scans**. The target sources and gain calibrators are usually organized *loops* in which the target source scans are sandwiched by the scans on the identical gain calibrator. We simply call such loops the **target source loops**. Finally, you also need some dummy **setup scans** to reserve time for hardware tuning.
{: .fs-2 }

To create a scheduling block, in the **OPT** interface, find your project code on the left and click the plus sign to unfold it. You will see a *Program block* with a character (A,B,C,D) that is the array configuration in the upcoming semester; click the plus sign to unfold it. Then on the top, click `File`->`Create New`->`Scheduling Block` to create a new empty observing script under that program block. Click into the **Scheduling block** you just created and give it a proper name (e.g., something easy for you and for the NRAO internal staff to know what that scheduling block is doing). Change the weather requirement of that scheduling block to the one that is suitable for your frequency band, and then in the case of dynamically scheduled observations, change the `latest UT start date/time:` to an arbitrarily late time (e.g., 2099 year). You can tentatively use an arbitrary `LST start range` and come back to edit it later.
{: .fs-2 }

You can continue to build the scans by clicking `File`->`Create New`->`Scan`, or can include a new target source loop by clicking `File`->`Create New`->`Scan Loop`.
{: .fs-2 }

##### 2.3.1 Setup scans

Strictly follow the rules documented in [this page](https://science.nrao.edu/facilities/vla/docs/manuals/obsguide/set-up). Otherwise, your observations will fail (the NRAO internal staff will spot if you do not follow the rule well). Note that although the document suggests a minimum 12 minutes' overall start time, you may need it to be longer than 12 minutes when your *first non-setup scan* is reference pointing to ensure that the on-source time for that scan is longer than **2m30s** (see also **Section 2.3.3**). More instruction regarding this point is given in **Section 2.3.4.1**.
{: .fs-2 }

##### 2.3.2 Target source loops

You need to look up the recommended **calibrator cycle time** for your target source in Table 3.1 of [this page](https://science.nrao.edu/facilities/vla/docs/manuals/obsguide/calibration). The actual cycle time for your observations can be shorter than that but not longer. You can also check the guideline for the *scan length* in the same webpage. Note that it does not matter how bright is your target source or calibrator, the minimum allowable on-source time for a scan is **20 seconds**.
{: .fs-2 }

##### 2.3.3 Reference pointing

Without calibration, the naiive pointing accuracy of the JVLA is ~2 arcmin. When your field of view is considerably bigger than that ([check here](https://science.nrao.edu/facilities/vla/docs/manuals/oss/performance/fov)), such pointing error does not lead to a big amplitude error. When the field of view is large, pointing calibration only matters when you are carrying out high dynamic-range imaging or mosaic observations, or polarization observations.
{: .fs-2 }

When the field of view is comparably smaller than the typical pointing errors, for example, in high-frequency observations, we need to include a reference pointing scan every time we slew to a new field, e.g., before your first calibration scan (of any purpose), when you slew from passband to absolute flux calibrator (and vice versa), when you slew from any of these calibrators to the gain calibrator, etc. Here, a *new field* can be defined by an AZ-EL direction that is offset from the current pointing direction by over **20 degrees**. Note that even if you are approximately staying around the same field, we still need to do reference pointing calibration approximately every 40 minutes when carrying out nighttime observations. In the daytime observations, we may want to do it every 20~30 minutes. We should use the standard X-point resource configuration if possible.
{: .fs-2 }

In most cases, you can use the calibrator that you are going to integrate on to calibrator reference pointing, e.g., you can perform the standard X-band pointing observations on your passband calibrator before you integrate on your passband calibrator at any other frequency bands. The minimum allowable on-source time for reference pointing calibration is **2m30s**. If the on-source time is less than that, your pointing calibration will likely fail. You can perform reference pointing calibration with an arbitrarily longer duration but that will reduce the time for you to integrate on your target source.
{: .fs-2 }

##### 2.3.4 Overall

###### 2.3.4.1 Simulating observations and optimizing scan duration, LST start range and antenna wrapping

Once (you think) you have all the scans you need, click the name of the scheduling block on the left. You will find five tabs on the right, which are `Information`, `Reports`, `Validation and Submission`, `Bulk Scan Edit`, and `Executions`.
{: .fs-2 }

Click into `Reports`. Then you will find the item `Assumed LST Start` and the two boxes on the right for you to insert the abbreviated `Julian date` and `LST time`. The former one is not so important unless your are doing *target-of-opportunity* observations or fixeed date observations for any other purposes (e.g., coordinated with optical or X-ray observations). You need to simulate the observations, iterating starting from your earliest possible LST start time of that specific scheduling block, with 20 minutes' interval. For example, if your LST range is 2~4 hr, then you have to simulate the observations at 2:00, 2:20: 2:40, 3:00, 3:20: 3:40, and 4:00. During the simulations, you have to make sure **(1) the on-source time for any calibration or target source scans is longer than 20 seconds**, **(2) all non-setup scans are observed at 8~80 degrees elevation**,  **(3) the on-source time for any reference pointing scans is longer than 2m30s**, **(4) for high-frequency observations, reference points are carried out every time you are slewing to a field that is more than 20 degrees offset from the present field**.
{: .fs-2 }

When your first non-setup scan is a reference pointing scan, you need to simulate with a LST start time that the reference pointing calibrator begins at its highest possible elevation. You then see to set the `Assumed Antenna Starting Direction` to a direction that is exactly opposite to that reference pointing calibrator. This is to ensure the success of the first reference pointing scan. Note that this may make your overall start-up time longer than the **12 minutes'** general recommendatation.
{: .fs-2 }

In general, I do not recommend observing your target source at lower than 20 degree
 elevation. But sometimes you do not have a choice, e.g., when your target source is at low delication.
 {: .fs-2 }

 Also, if your proposal rating is high (e.g., A ranked), you can try to limit the LST range for your scheduling blocks, such that the observations are carried out at >40 degree elevation in the case of D configuration observations, and at >25 degree elevation in the case of C array configuration. This is to avoid the mutual shadowing of antennae. However, the more limited LST range you use, the less chance for your observations to be dynamically scheduled. So there is this trade-off. If you are not sure about what is an optimal choice, please ask experienced observers.
{: .fs-2 }

###### 2.3.4.1 Validation, submission, and linking scheduling blocks

After changing the scans such that there is no errors, click into `Validation and Submission` to validate your scheduling block and submit it. Then an internal staff will review your scheduling blocks and give some feedback if necessary. **Remember to logout the OPT to allow the staff to login to your project.** In many cases, you have to un-submit your scheduling blocks and make edits accordingly. **Prepare and submit your scheduling block early. It takes time to iterate through these. The earlier the scheduling blocks are queued, the higher relative priority they will have (i.e., they will be more likely to be executed). This is particularly important when you are carrying out C-rated high-frequency observations (e.g., >20 GHz).**
{: .fs-2 }

Sometimes you may have to create various versions of scheduling blocks for the observations of the same target source groups. For example, sometimes you may need to observe different absolute flux and/or passband calibrators when using different LST ranges. Sometimes you also need to use different scan lengths. In such cases, you can submit various versions of scheduling blocks and then **link** them following this [instruction](https://science.nrao.edu/facilities/vla/docs/manuals/opt-manual/observation-preparation-tool/linking-sbs). Do not make a mistake with this. Otherwise, you may bill too much time for the observations on certain target sources groups while leaving no time for the rest.
{: .fs-2 }


### Chapter 3. Data calibration

#### 3.1 Pipeline calibration

Please find the pipeline [here](https://science.nrao.edu/facilities/vla/data-processing/pipeline). It may work OK when you are working at low-frequency standard continuum observations. This is rarely what I do. So I have not used it myself. Good luck.
{: .fs-2 }

#### 3.2 Manual CASA calibration

If you have not done this before, be ready to spend several weeks of full-time working in order to pick this up. Below is a *ALMA script generator style script* that I organized. It is compatible with CASA6 but not with any earlier version of CASA. You need to edit the section *##### Setting the basic information of the script ###########*. This script is not automatic, in particular, there is no automatic flagging. It is recommended to run it step-by-step. If this is the first time you use it, it may be necessary for you to visually check the options/parameters used for the tasks in each step and make sure those are what you really want. You should pay extra care if you would like to perform polarization calibration (you may need to manually update the polarization of the calibrators). And unfortunately, you have to manually created a file `pola_flux.txt` which should be an ASCII file with 2 columns: the first is the index of the spectral window, the second is the flux density of your polarization position angle calibrator. This information can be obtained during step 15 and is loaded in step 16 (i.e., to evaluate Stokes I, Q, U, and V of the calibrator based on the Stokes I flux density, polarization percentage, and polarization position angle).
{: .fs-2 }

If you use this script for your journal publication, it would be very much appreciated if you could include the following acknowledgement:
{: .fs-2 }

```
The manual JVLA data calibrations were performed using the procedure shared on the personal webpage of Hauyu Baobab Liu (https://baobabyoo.github.io/pages/students_topics/UsingTelescope_JVLA.html).
```
{: .fs-2 }

The script can be executed by
{: .fs-2 }

```
# for example, to execute step 0 only:
CASA> mysteps = [0]
CASA> execfile('script.py')
```
{: .fs-2 }


```
import os
import re
import numpy as np

##### Script Info ###########################################
#
# CASA version: CASA 6.5.2.26
# Contact: Hauyu Baobab Liu
#
#############################################################

##### Setting the basic information of the script ###########

### Calibration options
if_importasdm       = True
PolCalibration      = True
plot_interactive    = False
angle_calibrator = '3C286'
post2019            = True

### Data related parameters
filename     = '19A-262.sb36833530.eb37361201.58770.40095413194'
vis          = filename + '.ms'
Band         = 'Q'
config       = 'A'
EBid         = 'eb37361201'
num_antenna  = 26
refant       = 'ea10'

# name the calibrator field
BP   = '0'      # J0319+4130 (3C84)
GN   = '2'      # J0431+1731
TG   = '3'      # DMtau
POLD = '0'      # J0319+4130
POLA = '1'      # 3C138
FL   = '1'      # 3C138

# name scans:
GNscan = '14, 16, 18, 20, 22, 24, 26, 28, 30, 32, 34, 36, 38, 40, 42, 44, 46, 48, 50, 52, 54, 56, 58,  62, 64, 66, 68, 70, 72, 74, 76, 78, 80, 82, 84, 86, 88, 90, 92, 94, 96, 98, 100, 102, 104, 106'
BPscan = '6'
FLscan = '10'
POLDscan = '6'
POLAscan = '10'
TGscan   = '15, 17, 19, 21, 23, 25, 27, 29, 31, 33, 35, 37, 39, 41, 43, 45, 47, 49, 51, 53, 55, 57,  63, 65, 67, 69, 71, 73, 75, 77, 79, 81, 83, 85, 87, 89, 91, 93, 95, 97, 99, 101, 103, 105'

# name the spectral window ranges:
allspw     = '0~64'
sciencespw = '2~64'
bandcenters = '2~64:0~63'
beginspw   = '2'
endspw     = '64'
num_spw    = 63

### CASA related parameters
# fluxmodelpth = '/home/hyliu/softwares/CASA/casa-release-5.7.0-134.el7/data/nrao/VLA/CalModels/'
fluxmodelim  = '3C138_Q.im'
fluxstandard = 'Perley-Butler 2017'

### Important:
# Using CASA 5.3.0-143 and after, using Perley+17 flux standard

### Naming calibration tables (Do not edit this section)
antenna_table     = filename + '.antpos'
gaincurve_table   = filename + '.gaincurve'
opacity_table     = filename + '.opacity'
requantizer_table = filename + '.requantizer'
passband_gPtable  = filename + '.G0'
delay_table       = filename + '.K0'
BP_table          = filename + '.B0'
bootstrapgP_table = filename + '.G1'
BPflux_table      = filename + '.F1'
passband_gPtable2 = filename + '.G0.b'
delay_table2      = filename + '.K0.b'
BP_table2         = filename + '.B0.b'
gPint_table       = filename + '.G1.int'
gPinf_table       = filename + '.G1.inf'
gAint_table       = filename + '.G2'
flux_table        = filename + '.F2'
CrossHand_table   = filename + '.Kcross'
leakage_table     = filename + '.D1'
leakage_table2    = filename + '.D2'
POLPA_table       = filename + '.X1'
#############################################################


thesteps = []
step_title = {
              0: 'Listobs and plot antennas',
              1: 'Initial flagging and Data inspects',
              2: 'Manual flaggings',
              3: 'Save initial flags',
              4: 'Set flux density scale',
              5: 'Generate antenna position, gain curve, Tropospheric opacity, Requantizer gain table',
              6: 'First iteration of delay calibration',
              7: 'First iteration of passband calibration',
              8: 'Derive flux model for the passband calibrator',
              9: 'Second iteration of delay and passband calibration',
              10: 'Final manual flaggings',
              11: 'Save flags before final gain calibration',
              12: 'Per integration gain phase calibration',
              13: 'Per scan gain phase calibration',
              14: 'Gain amplitude calibration',
              15: 'Absolute flux scaling',
              16: 'Set polarizatoin flux standard',
              17: 'Solve crosshand delay',
              18: 'Set leakage calibrator flux standard',
              19: 'Solving for leakage terms',
              20: 'Solving for the R-L polarization angle',
              21: 'Applying calibration table',
              22: 'Splitting calibrated data',
             }

try:
  print ('List of steps to be executed ...', mysteps)
  thesteps = mysteps
except:
  print ('global variable mysteps not set.')
if (thesteps==[]):
  thesteps = range(0,len(step_title))
  print ('Executing all steps: ', thesteps)



mystep = 0
if(mystep in thesteps):
  casalog.post('Step '+str(mystep)+' '+step_title[mystep],'INFO')
  print ('Step ', mystep, step_title[mystep])

  if if_importasdm == True:
      importasdm(
                 asdm = filename, vis = vis,
                 createmms = False,
                 ocorr_mode = 'co', with_pointing_correction = True,
                 process_flags = True, applyflags = True,
                 savecmds = True, overwrite = True
                )

  listfile = filename + '.listobs'
  os.system('rm -rf ' + listfile)
  listobs(vis=vis, listfile=listfile)

  figfile  = filename + '.plotants.png'
  os.system('rm -rf ' + figfile)
  plotants(vis=vis, figfile=figfile)

  clearstat()




mystep = 1
if(mystep in thesteps):
  casalog.post('Step '+str(mystep)+' '+step_title[mystep],'INFO')
  print ('Step ', mystep, step_title[mystep])

  # apply online flaggs (required when imported ASDM instead of downloading MS)
  flagcmd(vis=vis, inpmode='table', action='apply',
          flagbackup=False)

  # listing online flaggs
  plotfile = filename + '.onlineflags.png'
  os.system('rm -rf ' + plotfile)
  flagcmd(vis=vis, inpmode='table', action='plot', \
          useapplied=True, plotfile=plotfile)

  mode = 'shadow'
  spw = ''
  flagbackup=False
  flagdata(vis=vis, mode=mode, spw=spw, flagbackup=flagbackup)




mystep = 2
if(mystep in thesteps):
  casalog.post('Step '+str(mystep)+' '+step_title[mystep],'INFO')
  print ('Step ', mystep, step_title[mystep])

  # flag dummy scans and pointings
  mode = 'manual'
  antenna = ''
  spw = ''
  flagbackup=False
  scan = '1~5, 7~9, 11~13, 59~61'
  timerange = ''
  flagdata(vis=vis, mode=mode, antenna=antenna, spw=spw, flagbackup=flagbackup, scan=scan, timerange=timerange)

  # flag dummy spw
  mode = 'manual'
  antenna = ''
  spw = '0,1'
  flagbackup=False
  scan = ''
  timerange = ''
  flagdata(vis=vis, mode=mode, antenna=antenna, spw=spw, flagbackup=flagbackup, scan=scan, timerange=timerange)

  # flag edge channls
  mode = 'manual'
  antenna = ''
  spw = '2~64:0~3;60~63'
  flagbackup=False
  scan = ''
  timerange = ''
  flagdata(vis=vis, mode=mode, antenna=antenna, spw=spw, flagbackup=flagbackup, scan=scan)

  # flag initial integration
  mode = 'quack'
  flagdata(vis=vis, mode=mode, quackinterval=6.0, quackmode = 'beg', flagbackup=False)


  # Initial data flagging
    # low amplitude
  mode = 'manual'
  antenna = 'ea01'
  spw = '2~64'
  flagbackup=False
  scan = ''
  timerange = ''
  flagdata(vis=vis, mode=mode, antenna=antenna, spw=spw, flagbackup=flagbackup, scan=scan)

  mode = 'manual'
  antenna = 'ea23'
  spw = '14'
  flagbackup=False
  scan = ''
  timerange = ''
  flagdata(vis=vis, mode=mode, antenna=antenna, spw=spw, flagbackup=flagbackup, scan=scan)

  mode = 'manual'
  antenna = 'ea07'
  spw = ''
  flagbackup=False
  scan = ''
  timerange = ''
  flagdata(vis=vis, mode=mode, antenna=antenna, spw=spw, flagbackup=flagbackup, scan=scan)

  mode = 'manual'
  antenna = 'ea08,ea12'
  spw = '2~33'
  flagbackup=False
  scan = ''
  timerange = ''
  flagdata(vis=vis, mode=mode, antenna=antenna, spw=spw, flagbackup=flagbackup, scan=scan)

  mode = 'manual'
  antenna = 'ea24'
  spw = '54~56'
  flagbackup=False
  scan = ''
  timerange = ''
  flagdata(vis=vis, mode=mode, antenna=antenna, spw=spw, flagbackup=flagbackup, scan=scan)

  mode = 'manual'
  antenna = 'ea10&ea11'
  spw = ''
  flagbackup=False
  scan = ''
  timerange = ''
  flagdata(vis=vis, mode=mode, antenna=antenna, spw=spw, flagbackup=flagbackup, scan=scan)

  mode = 'manual'
  antenna = 'ea19'
  spw = '10~33'
  flagbackup=False
  scan = ''
  timerange = ''
  flagdata(vis=vis, mode=mode, antenna=antenna, spw=spw, flagbackup=flagbackup, scan=scan)

  # zeros
  mode = 'manual'
  antenna = 'ea19&ea24'
  spw = '39'
  flagbackup=False
  scan = ''
  timerange = ''
  flagdata(vis=vis, mode=mode, antenna=antenna, spw=spw, flagbackup=flagbackup, scan=scan)

  mode = 'manual'
  antenna = 'ea19&ea23'
  spw = '39'
  flagbackup=False
  scan = ''
  timerange = ''
  flagdata(vis=vis, mode=mode, antenna=antenna, spw=spw, flagbackup=flagbackup, scan=scan)

  mode = 'manual'
  antenna = 'ea19&ea25'
  spw = '39'
  flagbackup=False
  scan = ''
  timerange = ''
  flagdata(vis=vis, mode=mode, antenna=antenna, spw=spw, flagbackup=flagbackup, scan=scan)

  mode = 'manual'
  antenna = 'ea19&ea26'
  spw = '39'
  flagbackup=False
  scan = ''
  timerange = ''
  flagdata(vis=vis, mode=mode, antenna=antenna, spw=spw, flagbackup=flagbackup, scan=scan)

  mode = 'manual'
  antenna = 'ea04'
  spw = '50'
  flagbackup=False
  scan = ''
  timerange = ''
  flagdata(vis=vis, mode=mode, antenna=antenna, spw=spw, flagbackup=flagbackup, scan=scan)


  # large number of missing scans
  mode = 'manual'
  antenna = 'ea22'
  spw = ''
  flagbackup=False
  scan = ''
  timerange = ''
  flagdata(vis=vis, mode=mode, antenna=antenna, spw=spw, flagbackup=flagbackup, scan=scan)


   # RFI
  mode = 'manual'
  antenna = ''
  spw = '10:28;29,11:20;21;54;55,12:0~6;21~23;51~55,13:9;49~50,15:19,17:36~39,27:47;48;56;57,28:46;47,29:46;47,36:40;41,37:11;23;25;26;59,38:17~19;27;39;40;44;45;50;51,39:14;18;34;43;44,52:50,54:21;22;50;55;56,55:33~35;58;59'
  flagbackup=False
  scan = ''
  timerange = ''
  flagdata(vis=vis, mode=mode, antenna=antenna, spw=spw, flagbackup=flagbackup, scan=scan)


  # clip zeros
  flagdata(vis=vis, mode='clip', clipzeros=True, flagbackup=False)

  # phase error
  mode = 'manual'
  antenna = 'ea02'
  spw = ''
  flagbackup=False
  scan = '45,51~53,85'
  timerange = ''
  flagdata(vis=vis, mode=mode, antenna=antenna, spw=spw, flagbackup=flagbackup, scan=scan)

  mode = 'manual'
  antenna = 'ea04,ea15'
  spw = ''
  flagbackup=False
  scan = '49~51'
  timerange = ''
  flagdata(vis=vis, mode=mode, antenna=antenna, spw=spw, flagbackup=flagbackup, scan=scan)

  # high amplitude
  mode = 'manual'
  antenna = ''
  spw = '33'
  flagbackup=False
  scan = ''
  timerange = ''
  flagdata(vis=vis, mode=mode, antenna=antenna, spw=spw, flagbackup=flagbackup, scan=scan)



mystep = 3
if(mystep in thesteps):
  casalog.post('Step '+str(mystep)+' '+step_title[mystep],'INFO')
  print ('Step ', mystep, step_title[mystep])

  mode = 'save'
  versionname = 'initial'
  flagmanager(vis=vis, mode=mode, versionname=versionname)




mystep = 4
if(mystep in thesteps):
  casalog.post('Step '+str(mystep)+' '+step_title[mystep],'INFO')
  print ('Step ', mystep, step_title[mystep])

  delmod(vis)
  field = FL
  scalebychan = True
  standard    = fluxstandard
  model = fluxmodelim
  setjy(vis=vis, field=field, spw=sciencespw,
        scalebychan=scalebychan, standard=standard, model=model)

  plotfile = vis + '.fluxmodel.png'
  os.system('rm -rf ' + plotfile)
  plotms(vis=vis, field=FL, antenna=refant, xaxis='freq', yaxis='amp', ydatacolumn='model',
        plotfile=plotfile)



mystep = 5
if(mystep in thesteps):
  casalog.post('Step '+str(mystep)+' '+step_title[mystep],'INFO')
  print ('Step ', mystep, step_title[mystep])

  antenna_table = filename + '.antpos'
  caltype       = 'antpos'
  antenna       = ''
  os.system('rm -rf ' + antenna_table)
  gencal(vis=vis, caltable=antenna_table, caltype=caltype, antenna=antenna)

  gaincurve_table = filename + '.gaincurve'
  caltype         = 'gc'
  os.system('rm -rf ' + gaincurve_table)
  gencal(vis=vis, caltable=gaincurve_table, caltype=caltype)

  doPlot = True
  myTau = plotweather(vis=vis, doPlot=doPlot)

  opacity_table = filename + '.opacity'
  caltype       = 'opac'
  spw = allspw
  os.system('rm -rf ' + opacity_table)
  gencal(vis=vis, caltable=opacity_table, caltype=caltype, spw=spw, parameter=myTau)

  requantizer_table = filename + '.requantizer'
  caltype = 'rq'
  os.system('rm -rf ' +  requantizer_table)
  gencal(vis=vis, caltable=requantizer_table, caltype=caltype)




mystep = 6
if(mystep in thesteps):
  casalog.post('Step '+str(mystep)+' '+step_title[mystep],'INFO')
  print ('Step ', mystep, step_title[mystep])

  # phase-vs.-time only calibration
  passband_gPtable = filename + '.G0'
  field            = BP
  spw              = bandcenters
  if os.path.exists(antenna_table) == True:
    gaintable = [antenna_table, gaincurve_table, requantizer_table, opacity_table]
  else:
    gaintable = [gaincurve_table, requantizer_table, opacity_table]

  gaintype  = 'G'
  calmode   = 'p'
  solint    = 'int'
  minsnr    = 3
  selectdata = True
  scan       = BPscan
  os.system('rm -rf ' + filename + '.G0.plotCal' )
  os.system('rm -rf ' + passband_gPtable)
  gaincal(vis=vis, caltable=passband_gPtable, field=field, spw='',
        gaintable=gaintable,
        gaintype=gaintype, refant=refant,
        calmode=calmode, solint=solint, minsnr=minsnr,
        # corrdepflags=False, # this line only works in older casa
        selectdata=selectdata, scan=scan)

  os.system('rm -rf ' + filename + '.G0.plots' )
  es.checkCalTable(passband_gPtable, msName=vis, interactive=False)


  delay_table = filename + '.K0'
  spw         = sciencespw
  antenna     = ''
  gaintype    = 'K'
  solint      = 'inf'
  minsnr      = 3
  if os.path.exists(antenna_table) == True:
    gaintable   = [antenna_table, gaincurve_table, requantizer_table, opacity_table, passband_gPtable]
  else:
    gaintable   = [gaincurve_table, requantizer_table, opacity_table, passband_gPtable]

  os.system( 'rm -rf ' + delay_table )
  gaincal(vis=vis, caltable=delay_table,
          gaintable=gaintable,
          field=field,
          scan=scan, selectdata=selectdata, spw=spw, antenna=antenna,
          gaintype=gaintype, refant=refant, solint=solint, minsnr=minsnr)

  xaxis = 'spw'
  yaxis = 'delay'
  figfile = filename + '.K0.png'
  os.system( 'rm -rf ' + figfile)
  plotms(vis=delay_table, xaxis=xaxis, yaxis=yaxis, plotfile=figfile, coloraxis='antenna1')




mystep = 7
if(mystep in thesteps):
  casalog.post('Step '+str(mystep)+' '+step_title[mystep],'INFO')
  print ('Step ', mystep, step_title[mystep])

  field        = BP
  selectdata   = True
  scan         = BPscan
  BP_table = filename + '.B0'
  solnorm  = False
  bandtype = 'B'
  if os.path.exists(antenna_table) == True:
    gaintable   = [antenna_table, gaincurve_table, requantizer_table, opacity_table, passband_gPtable, delay_table]
  else:
    gaintable   = [gaincurve_table, requantizer_table, opacity_table, passband_gPtable, delay_table]

  solint   = 'inf'
  os.system('rm -rf ' + '.B0.plotCal' )
  os.system('rm -rf ' + BP_table)
  bandpass(vis=vis, caltable=BP_table, gaintable=gaintable,
           field=field, selectdata=selectdata, scan=scan,
           refant=refant, solnorm=solnorm, bandtype=bandtype,
           solint=solint
           # spw = '0,1,3~5, 7~11, 13~14, 16~17', append=False
           )

  os.system('rm -rf ' + filename + '.B0.plots' )
  es.checkCalTable(BP_table, msName=vis, interactive=False)




mystep = 8
if(mystep in thesteps):
  casalog.post('Step '+str(mystep)+' '+step_title[mystep],'INFO')
  print ('Step ', mystep, step_title[mystep])


  if (BP != FL):


      field             = BP + ',' + FL
      bootstrapgP_table = filename + '.G1'
      gaintype          = 'G'
      calmode           = 'ap'
      solint            = 'int'
      minsnr            = 3
      selectdata        = True
      scan              = BPscan + ',' + FLscan
      if os.path.exists(antenna_table) == True:
        gaintable   = [antenna_table, gaincurve_table, requantizer_table, opacity_table, delay_table, BP_table]
      else:
        gaintable   = [gaincurve_table, requantizer_table, opacity_table, delay_table, BP_table]

      os.system('rm -rf ' + bootstrapgP_table+'.p')
      gaincal(vis=vis, caltable=bootstrapgP_table+'.p', field=field,
            gaintable=gaintable,
            gaintype='G', refant=refant, calmode='p', solint=solint, minsnr=3)

      if os.path.exists(antenna_table) == True:
        gaintable   = [antenna_table, gaincurve_table, requantizer_table, opacity_table, delay_table, BP_table, bootstrapgP_table+'.p']
      else:
        gaintable   = [gaincurve_table, requantizer_table, opacity_table, delay_table, BP_table, bootstrapgP_table+'.p']

      os.system('rm -rf ' + bootstrapgP_table)
      gaincal(vis=vis, field=field, caltable=bootstrapgP_table, gaintype=gaintype,
              ###### flux calibrator spatially resolved out; limit uv range to improve solution #####
              # uvrange='0~400klambda',
              #######################################################################################
              gaintable=gaintable, refant=refant, calmode=calmode, solint='inf', minsnr=minsnr,
              selectdata=selectdata, scan=scan)

      BPflux_table = filename + '.F1'
      reference    = FL
      transfer     = BP
      listfile     = 'BP.fluxinfo'
      fitorder     = 1
      os.system('rm -rf ' + 'BP.fluxinfo')
      os.system('rm -rf ' + BPflux_table)
      flux1 = fluxscale(vis=vis, caltable=bootstrapgP_table, fluxtable=BPflux_table,
                      reference=reference, transfer=transfer, listfile=listfile, fitorder=fitorder)

      freq = flux1['freq'] / 1e9
      spw_list = range(0, num_spw)
      spw_str = []
      for i in spw_list:
        thisspw = str(i)
        spw_str.append(thisspw)

      bootstrapped_fluxes = []
      bootstrapped_freq   = []
      for j in spw_str:
        thisflux = flux1[BP][j]['fluxd'][0]
        thisfreq = flux1['freq'][int(j)]
        if (thisflux ==None) or (thisflux < 0.0) or ( thisfreq < 0.0 ):
            continue
        else:
            bootstrapped_freq.append(thisfreq)
            bootstrapped_fluxes.append(thisflux)

      z = np.polyfit( np.log10(bootstrapped_freq) , np.log10(bootstrapped_fluxes), 1)
      print ( "spectral index: ", z[0] )

      p = np.poly1d(z)

      setjy(vis=vis, field=BP, scalebychan=True, standard = 'fluxscale', fluxdict=flux1)

      plotfile = vis + '.fluxmodel.BP.png'
      os.system('rm -rf ' + plotfile)
      plotms(vis=vis, field=BP, antenna=refant, xaxis='freq', yaxis='amp', ydatacolumn='model',
             plotfile=plotfile)



mystep = 9
if(mystep in thesteps):
  casalog.post('Step '+str(mystep)+' '+step_title[mystep],'INFO')
  print ('Step ', mystep, step_title[mystep])


  if (BP != FL):
      passband_gPtable2  = filename + '.G0.b'
      field              = BP
      spw                = bandcenters
      selectdata         = True
      scan               = BPscan
      gaintype           = 'G'
      calmode            = 'p'
      solint             = 'int'
      minsnr             = 3
      if os.path.exists(antenna_table) == True:
        gaintable   = [antenna_table, gaincurve_table, requantizer_table, opacity_table]
      else:
        gaintable   = [gaincurve_table, requantizer_table, opacity_table]

      os.system('rm -rf ' + passband_gPtable2)
      os.system('rm -rf ' + filename + '.G0.b.plotCal' )
      gaincal(vis=vis, field=field, spw=spw, selectdata=selectdata, scan=scan,
            caltable=passband_gPtable2, gaintable=gaintable, gaintype=gaintype,
            refant=refant, calmode=calmode, solint=solint, minsnr=minsnr)

      os.system('rm -rf ' + filename + '.G0.b.plots' )
      es.checkCalTable(passband_gPtable2, msName=vis, interactive=False)


      delay_table2      = filename + '.K0.b'
      spw               = sciencespw
      gaintype          = 'K'
      solint            = 'inf'
      if os.path.exists(antenna_table) == True:
        gaintable         = [antenna_table, gaincurve_table, requantizer_table, opacity_table, passband_gPtable2]
      else:
        gaintable         = [gaincurve_table, requantizer_table, opacity_table, passband_gPtable2]

      os.system('rm -rf ' + delay_table2)
      gaincal(vis=vis, caltable=delay_table2, gaintable=gaintable, field=field,
              selectdata=selectdata, scan=scan, spw=spw, gaintype=gaintype,
              refant=refant, solint=solint, minsnr=minsnr)

      BP_table2 = filename + '.B0.b'
      solnorm   = False
      bandtype  = 'B'
      solint    = 'inf,1000kHz'
      if os.path.exists(antenna_table) == True:
        gaintable         = [antenna_table, gaincurve_table, requantizer_table, opacity_table, passband_gPtable2, delay_table2]
      else:
        gaintable         = [gaincurve_table, requantizer_table, opacity_table, passband_gPtable2, delay_table2]

      os.system('rm -rf ' + BP_table2)
      os.system('rm -rf ' + filename + '.B0.b.plotCal' )
      solint   = 'inf'
      bandpass(vis=vis, caltable=BP_table2, gaintable=gaintable,
               field=field, selectdata=selectdata, scan=scan,
               refant=refant, solnorm=solnorm, bandtype=bandtype,
               solint=solint,
               # spw = '0,1,3~5, 7~11, 13~14, 16~17', append=False
               )

      os.system('rm -rf ' + filename + '.B0.b.plots' )
      es.checkCalTable(BP_table2, msName=vis, interactive=False)

  else:

    os.system('rm -rf ' + delay_table2)
    os.system('cp -r ' + delay_table + ' ' + delay_table2)
    os.system('rm -rf ' + BP_table2)
    os.system('cp -r ' + BP_table + ' ' + BP_table2)




mystep = 10
if(mystep in thesteps):
  casalog.post('Step '+str(mystep)+' '+step_title[mystep],'INFO')
  print ('Step ', mystep, step_title[mystep])




mystep = 11
if(mystep in thesteps):
  casalog.post('Step '+str(mystep)+' '+step_title[mystep],'INFO')
  print ('Step ', mystep, step_title[mystep])

  mode = 'save'
  versionname = 'BeforeGain'
  flagmanager(vis=vis, mode=mode, versionname=versionname)




mystep = 12
if(mystep in thesteps):
  casalog.post('Step '+str(mystep)+' '+step_title[mystep],'INFO')
  print ('Step ', mystep, step_title[mystep])

  if os.path.exists(antenna_table) == True:
    gaintable   = [antenna_table, gaincurve_table, requantizer_table, opacity_table, delay_table2, BP_table2]
  else:
    gaintable   = [gaincurve_table, requantizer_table, opacity_table, delay_table2, BP_table2]

  os.system('rm -rf ' + gPint_table)
  os.system('rm -rf ' + filename + '.G1.int.plotCal' )
  gaincal(
          vis=vis, caltable=gPint_table, gaintable=gaintable,
          field       = FL,
          scan        = FLscan,
          solint      = 'int',
          gaintype    = 'G',
          calmode     = 'p',
          refantmode  = 'strict',
          refant=refant, solnorm=False, selectdata=True,
          append=False
         )

  if (BP != FL):
    gaincal(
          vis=vis, caltable=gPint_table, gaintable=gaintable,
          field       = BP,
          scan        = BPscan,
          solint      = 'int',
          gaintype    = 'G',
          calmode     = 'p',
          refantmode  = 'strict',
          refant=refant, solnorm=False, selectdata=True,
          append=True
         )

  if (GN != BP):
    gaincal(
            vis=vis, caltable=gPint_table, gaintable=gaintable,
            field       = GN,
            scan        = GNscan,
            solint      = 'int',
            gaintype    = 'G',
            calmode     = 'p',
            refantmode  = 'strict',
            refant=refant, solnorm=False, selectdata=True,
            append=True
           )

  if PolCalibration == True:
    if (POLD != BP):
      gaincal(
              vis=vis, caltable=gPint_table, gaintable=gaintable,
              field       = POLD,
              scan        = POLDscan,
              solint      = 'int',
              gaintype    = 'G',
              calmode     = 'p',
              refantmode  = 'strict',
              refant=refant, solnorm=False, selectdata=True,
              append=True
           )

  os.system('rm -rf ' + filename + '.G1.int.plots' )
  es.checkCalTable(gPint_table, msName=vis, interactive=False)




mystep = 13
if(mystep in thesteps):
  casalog.post('Step '+str(mystep)+' '+step_title[mystep],'INFO')
  print ('Step ', mystep, step_title[mystep])

  if os.path.exists(antenna_table) == True:
    gaintable   = [antenna_table, gaincurve_table, requantizer_table, opacity_table, delay_table2, BP_table2]
  else:
    gaintable   = [gaincurve_table, requantizer_table, opacity_table, delay_table2, BP_table2]

  os.system('rm -rf ' + gPinf_table)
  os.system('rm -rf ' + filename + '.G1.inf.plotCal' )
  gaincal(vis=vis, caltable=gPinf_table, gaintable=gaintable,
          field       = GN,
          scan        = GNscan,
          solint      = 'inf',
          gaintype    = 'G',
          calmode     = 'p',
          refant=refant,
          solnorm=False
         )

  os.system('rm -rf ' + filename + '.G1.inf.plots' )
  es.checkCalTable(gPinf_table, msName=vis, interactive=False)




mystep = 14
if(mystep in thesteps):
  casalog.post('Step '+str(mystep)+' '+step_title[mystep],'INFO')
  print ('Step ', mystep, step_title[mystep])

  delmod(vis)

  table_created = False
  append        = False

  field = FL
  scalebychan = True
  standard    = fluxstandard
  model = fluxmodelim
  setjy(vis=vis, spw=sciencespw,
        field=field, scalebychan=scalebychan, standard=standard, model=model)

  os.system('rm -rf ' + gAint_table)
  os.system('rm -rf ' + filename + '.G2.plotCal' )


  field = BP
  if os.path.exists(antenna_table) == True:
    gaintable   = [antenna_table, gaincurve_table, requantizer_table, opacity_table, delay_table2, BP_table2, gPint_table]
    gainfield   = ['','','','',BP,BP,field]
    interp      = ['','','','','nearest','nearest','nearest']
  else:
    gaintable   = [gaincurve_table, requantizer_table, opacity_table, delay_table2, BP_table2, gPint_table]
    gainfield   = ['','','',BP,BP,field]
    interp      = ['','','','nearest','nearest','nearest']

  if (BP != FL):
     gaincal(vis=vis, caltable=gAint_table, gaintable=gaintable, gainfield=gainfield, interp=interp,
          field=field, refant=refant, solnorm=False,
          scan          = BPscan,
          solint        = 'inf',
          gaintype      = 'G',
          calmode       = 'a',
          append        = append,
          spw           = sciencespw,
          selectdata=True)
     table_created = True


  if PolCalibration == True:
    if (POLD != BP):

      field = POLD
      if os.path.exists(antenna_table) == True:
        gaintable   = [antenna_table, gaincurve_table, requantizer_table, opacity_table, delay_table2, BP_table2, gPint_table]
        gainfield   = ['','','','',BP,BP,field]
        interp      = ['','','','','nearest','nearest','nearest']
      else:
        gaintable   = [gaincurve_table, requantizer_table, opacity_table, delay_table2, BP_table2, gPint_table]
        gainfield   = ['','','',BP,BP,field]
        interp      = ['','','','nearest','nearest','nearest']

      if ( table_created == True ):
        append = True


      gaincal(vis=vis, caltable=gAint_table, gaintable=gaintable, gainfield=gainfield, interp=interp,
          field=field, refant=refant, solnorm=False,
          scan          = POLDscan,
          solint        = 'inf',
          gaintype      = 'G',
          calmode       = 'a',
          append        = append,
          spw           = sciencespw,
          selectdata=True)
      table_created = True



  field = GN
  if os.path.exists(antenna_table) == True:
    gainfield   = ['','','','',BP,BP,field]
  else:
    gainfield   = ['','','',BP,BP,field]

  if ( table_created == True ):
    append = True

  if (GN != BP):
    gaincal(vis=vis, caltable=gAint_table, gaintable=gaintable, gainfield=gainfield, interp=interp,
            field=field, refant=refant, solnorm=False,
            scan          = GNscan,
            solint        = 'inf',
            gaintype      = 'G',
            calmode       = 'a',
            append        = append,
            spw           = sciencespw,
            selectdata=True)

    table_created = True


  field = FL
  if os.path.exists(antenna_table) == True:
    gainfield   = ['','','','',BP,BP,field]
  else:
    gainfield   = ['','','',BP,BP,field]

  if ( table_created == True ):
    append = True

  gaincal(vis=vis, caltable=gAint_table, gaintable=gaintable, gainfield=gainfield, interp=interp,
          field=field, refant=refant, solnorm=False,
          scan          = FLscan,
          solint        = 'inf',
          gaintype      = 'G',
          calmode       = 'a',
          append        = append,
          spw           = sciencespw,
          selectdata=True)

  os.system('rm -rf ' + filename + '.G2.plots' )
  es.checkCalTable(gAint_table, msName=vis, interactive=False)




mystep = 15
if(mystep in thesteps):
  casalog.post('Step '+str(mystep)+' '+step_title[mystep],'INFO')
  print ('Step ', mystep, step_title[mystep])

  reference   = FL
  listfile    = vis + '.fluxscale'
  os.system('rm -rf ' + flux_table)
  os.system('rm -rf ' + filename + '.F2.plotCal')
  os.system('rm -rf ' + listfile)
  flux2 = fluxscale(vis=vis, caltable=gAint_table,
                    listfile     = listfile,
                    fluxtable=flux_table, reference=reference)

  os.system('rm -rf ' + filename + '.F2.plots' )
  es.checkCalTable(flux_table, msName=vis, interactive=False)




mystep = 16
if(mystep in thesteps):
  casalog.post('Step '+str(mystep)+' '+step_title[mystep],'INFO')
  print ('Step ', mystep, step_title[mystep])

  if PolCalibration == True:
    delmod(vis)

    ### REMEMBER TO EDIT THIS ###
    freq_min = 4.0104e+10
    freq_max = 4.7896e+10
    flux_freqmin = 0.82535
    flux_freqmax = 0.7295
    ### #########################
    spix = np.log( flux_freqmin / flux_freqmax ) / np.log( freq_min / freq_max )
    print( 'spectral index', spix )

    # using value after 2019
    if angle_calibrator == '3C286':
      if post2019 == True:
        polfreq_Hz = np.array([
                               1.02,
                               1.47,
                               1.87,
                               2.57,
                               3.57,
                               4.89,
                               6.68,
                               8.43,
                               11.3,
                               14.1,
                               16.6,
                               19.1,
                               25.6,
                               32.1,
                               37.1,
                               42.1,
                               48.1
                             ]) * 1e9
        polper_percent = np.array([
                               8.6,
                               9.8,
                               10.1,
                               10.6,
                               11.2,
                               11.5,
                               11.9,
                               12.1,
                               12.3,
                               12.3,
                               12.5,
                               12.6,
                               12.7,
                               13.1,
                               13.5,
                               13.4,
                               14.6
                             ])
        polang_degree = np.array([
                               33,
                               33,
                               33,
                               33,
                               33,
                               33,
                               33,
                               33,
                               34,
                               34,
                               35,
                               35,
                               36,
                               36,
                               36,
                               37,
                               36
                             ])

      else:

        polfreq_Hz = np.array([
                               1.05,
                               1.45,
                               1.64,
                               1.95,
                               2.45,
                               2.95,
                               3.25,
                               3.75,
                               4.50,
                               5.00,
                               6.50,
                               7.25,
                               8.10,
                               8.80,
                               12.8,
                               13.7,
                               14.6,
                               15.5,
                               18.1,
                               19.0,
                               22.4,
                               23.3,
                               36.5,
                               43.5
                           ]) * 1e9
        polper_percent = np.array([
                               8.6,
                               9.5,
                               9.9,
                               10.1,
                               10.5,
                               10.8,
                               10.9,
                               11.1,
                               11.3,
                               11.4,
                               11.6,
                               11.7,
                               11.9,
                               11.9,
                               11.9,
                               11.9,
                               12.1,
                               12.2,
                               12.5,
                               12.5,
                               12.6,
                               12.6,
                               13.1,
                               13.2
                           ])
        polang_degree = np.array([
                               33,
                               33,
                               33,
                               33,
                               33,
                               33,
                               33,
                               33,
                               33,
                               33,
                               33,
                               33,
                               34,
                               34,
                               34,
                               34,
                               34,
                               34,
                               34,
                               35,
                               35,
                               35,
                               36,
                               36
                          ])


    if angle_calibrator == '3C147':
      if post2019 == True:
        polfreq_Hz = np.array([
                               1.02,
                               1.47,
                               1.87,
                               2.57,
                               3.57,
                               4.89,
                               6.68,
                               8.43,
                               11.3,
                               14.1,
                               16.6,
                               19.1,
                               25.6,
                               32.1,
                               37.1,
                               42.1,
                               48.1
                             ]) * 1e9
        polper_percent = np.array([
                               0.0,
                               0.0,
                               0.0,
                               0.0,
                               0.0,
                               0.16,
                               0.51,
                               0.48,
                               0.85,
                               1.8,
                               2.4,
                               2.9,
                               3.4,
                               4.0,
                               4.5,
                               4.9,
                               6.0
                             ])
        polang_degree = np.array([
                               0,
                               0,
                               0,
                               0,
                               0,
                               -13,
                               -57,
                               -19,
                               27,
                               53,
                               60,
                               66,
                               79,
                               83,
                               87,
                               87,
                               85
                             ])

      else:

        polfreq_Hz = np.array([
                              1.05,
                              1.45,
                              1.64,
                              1.95,
                              2.45,
                              2.95,
                              3.25,
                              3.75,
                              4.50,
                              5.00,
                              6.50,
                              7.25,
                              8.10,
                              8.80,
                              12.8,
                              13.7,
                              14.6,
                              15.5,
                              18.1,
                              19.0,
                              22.4,
                              23.3,
                              36.5,
                              43.5
                           ]) * 1e9
        polper_percent = np.array([
                              0.0,
                              0.0,
                              0.0,
                              0.0,
                              0.0,
                              0.0,
                              0.0,
                              0.0,
                              0.1,
                              0.3,
                              0.3,
                              0.6,
                              0.7,
                              0.8,
                              2.2,
                              2.4,
                              2.7,
                              2.9,
                              3.4,
                              3.5,
                              3.8,
                              3.8,
                              4.4,
                              5.2
                           ])
        polang_degree = np.array([
                              0,
                              0,
                              0,
                              0,
                              0,
                              0,
                              0,
                              0,
                              -100,
                              0,
                              -65,
                              -39,
                              -24,
                              -11,
                              43,
                              48,
                              53,
                              59,
                              67,
                              68,
                              75,
                              76,
                              85,
                              86
                          ])

    if angle_calibrator == '3C48':
      if post2019 == True:
        polfreq_Hz = np.array([
                              1.02,
                              1.47,
                              1.87,
                              2.57,
                              3.57,
                              4.89,
                              6.68,
                              8.43,
                              11.3,
                              14.1,
                              16.6,
                              19.1,
                              25.6,
                              32.1,
                              37.1,
                              42.1,
                              48.1
                             ]) * 1e9
        polper_percent = np.array([
                              0.3,
                              0.5,
                              0.9,
                              1.6,
                              2.9,
                              4.3,
                              5.4,
                              5.4,
                              5.7,
                              6.1,
                              6.3,
                              6.5,
                              7.2,
                              6.4,
                              6.7,
                              5.6,
                              6.8
                             ])
        polang_degree = np.array([
                              4.3,
                              -34,
                              23,
                              67.1,
                              -84,
                              -72,
                              -66,
                              -63,
                              -62,
                              -63,
                              -64,
                              -68,
                              -72,
                              -76,
                              -77,
                              -84,
                              -84
                             ])

      else:

        polfreq_Hz = np.array([
                            1.05,
                            1.45,
                            1.64,
                            1.95,
                            2.45,
                            2.95,
                            3.25,
                            3.75,
                            4.50,
                            5.00,
                            6.50,
                            7.25,
                            8.10,
                            8.80,
                            12.8,
                            13.7,
                            14.6,
                            15.5,
                            18.1,
                            19.0,
                            22.4,
                            23.3,
                            36.5,
                            43.5
                           ]) * 1e9
        polper_percent = np.array([
                            0.3,
                            0.5,
                            0.7,
                            0.9,
                            1.4,
                            2.0,
                            2.5,
                            3.2,
                            3.8,
                            4.2,
                            5.2,
                            5.2,
                            5.3,
                            5.4,
                            6.0,
                            6.1,
                            6.4,
                            6.4,
                            6.9,
                            7.1,
                            7.7,
                            7.8,
                            7.4,
                            7.5
                           ])
        polang_degree = np.array([
                            25,
                            140,
                            -5,
                            -150,
                            -120,
                            -100,
                            -92,
                            -84,
                            -75,
                            -72,
                            -68,
                            -67,
                            -64,
                            -62,
                            -62,
                            -62,
                            -63,
                            -64,
                            -66,
                            -67,
                            -70,
                            -70,
                            -77,
                            -85    
                          ])

    if angle_calibrator == '3C138':
      if post2019 == True:
        polfreq_Hz = np.array([
                             1.02,
                             1.47,
                             1.87,
                             2.57,
                             3.57,
                             4.89,
                             6.68,
                             8.43,
                             11.3,
                             14.1,
                             16.6,
                             19.1,
                             25.6,
                             32.1,
                             37.1,
                             42.1,
                             48.1
                             ]) * 1e9
        polper_percent = np.array([
                             5.5,
                             7.8,
                             9.0,
                             9.9,
                             10.3,
                             10.5,
                             10.2,
                             10.9,
                             9.1,
                             8.2,
                             8.2,
                             8.4,
                             8.4,
                             8.5,
                             8.7,
                             8.8,
                             9.2
                             ])
        polang_degree = np.array([
                             -13,
                             -9.6,
                             -9.3,
                             -10,
                             -9.5,
                             -10.5,
                             -11.5,
                             -9.4,
                             -7.9,
                             -11,
                             -13,
                             -16,
                             -18,
                             -19,
                             -20,
                             -23,
                             -24
                             ])
      else:

        polfreq_Hz = np.array([
                            1.05,
                            1.45,
                            1.64,
                            1.95,
                            2.45,
                            2.95,
                            3.25,
                            4.50,
                            5.00,
                            6.50,
                            7.25,
                            8.10,
                            8.80,
                            12.8,
                            13.7,
                            14.6,
                            15.5,
                            18.1,
                            19.0,
                            22.4,
                            23.3,
                            36.5,
                            43.5    
                           ]) * 1e9
        polper_percent = np.array([
                            5.6,
                            7.5,
                            8.4,
                            9.0,
                            10.4,
                            10.7,
                            10.0,
                            10.0,
                            10.4,
                            9.8,
                            10.0,
                            10.4,
                            10.1,
                            8.4,
                            7.9,
                            7.7,
                            7.4,
                            6.7,
                            6.5,
                            6.7,
                            6.6,
                            6.6,
                            6.5
                           ])
        polang_degree = np.array([
                            -14,
                            -11,
                            -10,
                            -10,
                            -9,
                            -10,
                            -10,
                            -11,
                            -11,
                            -12,
                            -12,
                            -10,
                            -8,
                            -7,
                            -7,
                            -8,
                            -9,
                            -12,
                            -13,
                            -16,
                            -17,
                            -24,
                            -27
                          ])

    windowfreq_dict = {}
    ms.open(vis)
    spwInfo = ms.getspectralwindowinfo()
    for window in spwInfo:
       if ( spwInfo[window]['ChanWidth'] > 0.0 ):
         bandlow = spwInfo[window]['Chan1Freq']
         bandup  = spwInfo[window]['Chan1Freq'] + spwInfo[window]['TotalWidth']
       else:
         bandlow = spwInfo[window]['Chan1Freq'] - spwInfo[window]['TotalWidth']
         bandup  = spwInfo[window]['Chan1Freq']
       bandmean = (bandlow + bandup) / 2.0
       windowfreq_dict[window] = bandmean

    # print( windowfreq_dict )
    ms.close()

    fluxfilename  =  'pola_flux.txt'
    window_ids   =  np.loadtxt(
                        fluxfilename,
                        comments = '#',
                        usecols  = [0]
                        )
    window_fluxJys =  np.loadtxt(
                        fluxfilename,
                        comments = '#',
                        usecols  = [1]
                        )


    spw_list = range( int(beginspw) , int(endspw) + 1)
    for j in spw_list:
      thisspw = str(j)

      windowfreq = windowfreq_dict[ thisspw ]
      index = np.where( window_ids == j )
      id0   =index[0][0]

      for i in range( np.size( polfreq_Hz ) -1 ):
        if (
            ( polfreq_Hz[i] <= windowfreq )
            and
            ( polfreq_Hz[i+1] >= windowfreq )
           ):
          freq_id_l = i
          freq_id_h = i+1

          freq_l = polfreq_Hz[i]
          freq_h = polfreq_Hz[i+1]
          polper_percent_l = polper_percent[i]
          polper_percent_h = polper_percent[i+1]
          polang_degree_l = polang_degree[i]
          polang_degree_h = polang_degree[i+1]

          freq_interp = np.array( [freq_l, freq_h] )
          polper_percent_interp = np.array( [polper_percent_l, polper_percent_h] )
          polang_degree_interp  = np.array( [polang_degree_l,polang_degree_h] )

          polper = np.interp(windowfreq, freq_interp, polper_percent_interp)
          polang = np.interp(windowfreq, freq_interp, polang_degree_interp)

      # print( window_ids[id0], windowfreq, window_fluxJys[id0], polper, polang )

      thisflux = window_fluxJys[id0]
      thisfreq = str(windowfreq) + 'Hz'

      i0 = thisflux
      percentage = polper * 0.01
      polposang  = polang
      p0 = percentage * i0
      q0 = p0 * np.cos((2.0*polposang*np.pi)/180.0)
      u0 = p0 * np.sin((2.0*polposang*np.pi)/180.0)

      standard = 'manual'
      field    = POLA
      fluxdensity = [i0,q0,u0,0]
      thisspix        = [spix, 0]
      reffreq     = thisfreq
      # print( thisfreq, fluxdensity )
      setjy(
            vis=vis,
            field=POLA,
            standard='manual',
            spw=thisspw,
            fluxdensity=fluxdensity,
            reffreq=thisfreq,
            spix=thisspix,
            scalebychan=True,
            usescratch=False
           )

    plotfile = vis + '.Polfluxmodel_RRamp.png'
    os.system('rm -rf ' + plotfile)
    plotms(vis=vis, field=POLA, antenna=refant, xaxis='freq', yaxis='amp', ydatacolumn='model',
           correlation = 'RR',
           plotfile=plotfile)

    plotfile = vis + '.Polfluxmodel_RLamp.png'
    os.system('rm -rf ' + plotfile)
    plotms(vis=vis, field=POLA, antenna=refant, xaxis='freq', yaxis='amp', ydatacolumn='model',
           correlation = 'RL',
           plotfile=plotfile)

    plotfile = vis + '.Polfluxmodel_RLphase.png'
    os.system('rm -rf ' + plotfile)
    plotms(vis=vis, field=POLA, antenna=refant, xaxis='freq', yaxis='phase', ydatacolumn='model',
           correlation = 'RL',
           plotrange   = [-1,-1,-180,180],
           plotfile=plotfile)




mystep = 17
if(mystep in thesteps):
  casalog.post('Step '+str(mystep)+' '+step_title[mystep],'INFO')
  print ('Step ', mystep, step_title[mystep])

  if PolCalibration == True:

    if os.path.exists(antenna_table) == True:
      gaintable = [antenna_table, gaincurve_table, requantizer_table, opacity_table, delay_table2, BP_table2, gPint_table, gAint_table]
      gainfield = ['','','','','','',POLA,POLA]
      interp    = ['','','','','nearest','nearest','linear','linear']
    else:
      gaintable = [gaincurve_table, requantizer_table, opacity_table, delay_table2, BP_table2, gPint_table, gAint_table]
      gainfield = ['','','','','',POLA, POLA]
      interp    = ['','','','nearest','nearest','linear','linear']

    os.system('rm -rf ' + CrossHand_table)
    gaincal(vis=vis, caltable=CrossHand_table,
            field           = POLA,
            scan            = POLAscan,
            spw             = sciencespw,
            solint          = 'inf',
            ###### flux calibrator spatially resolved out; limit uv range to improve solution #####
            # uvrange='0~400klambda',
            #######################################################################################
            combine         = 'scan',
            parang          = True,
            gaintype='KCROSS', refant=refant, selectdata=True,
            gaintable=gaintable, gainfield=gainfield, interp=interp)

    # Inspect the solution. Should have a similar order of magnitude
    # with the parallel-hand delays (?)
    xaxis = 'spw'
    yaxis = 'delay'
    figfile = filename + '.Kcross-delay.png'
    os.system( 'rm -rf ' + figfile)
    plotms(vis=CrossHand_table, xaxis=xaxis, yaxis=yaxis, plotfile=figfile, coloraxis='antenna1')




mystep = 18
if(mystep in thesteps):
  casalog.post('Step '+str(mystep)+' '+step_title[mystep],'INFO')
  print ('Step ', mystep, step_title[mystep])

  if PolCalibration == True:

    reference   = FL
    os.system('rm -rf ' + 'POLDflux_table_temp')
    flux2 = fluxscale(vis=vis, caltable=gAint_table,
                      fluxtable='POLDflux_table_temp',
                      reference=reference)
    os.system('rm -rf ' + 'POLDflux_table_temp')

    freq = flux2['freq'] / 1e9
    spw_list = range( int(beginspw) , int(endspw) + 1)
    spw_str = []
    for i in spw_list:
      thisspw = str(i)
      spw_str.append(thisspw)

    bootstrapped_fluxes = []
    bootstrapped_freq   = []
    # print(flux2)
    for j in spw_str:
      thisflux = flux2[POLD][j]['fluxd'][0]
      thisfreq = flux2['freq'][int(j)]
      if (thisflux ==None) or ( thisfreq < 0.0 ):
        continue
      else:
        bootstrapped_freq.append(thisfreq)
        bootstrapped_fluxes.append(thisflux)

    z = np.polyfit( np.log10(bootstrapped_freq) , np.log10(bootstrapped_fluxes), 1)
    print ( "spectral index: ", z[0] )

    for j in spw_str:
      standard    = 'manual'
      thisflux = flux2[POLD][j]['fluxd'][0]
      thisfreq = str( flux2['freq'][int(j)] ) + 'Hz'
      thisspix = [ z[0], 0]

      # print( thisfreq, thisflux, thisspix )
      setjy(vis=vis,
            field = POLD,
            spw   = j,
            scalebychan=True,
            standard='manual',
            fluxdensity=[thisflux, 0, 0, 0],
            reffreq=thisfreq,
            spix=thisspix
           )




mystep = 19
if(mystep in thesteps):
  casalog.post('Step '+str(mystep)+' '+step_title[mystep],'INFO')
  print ('Step ', mystep, step_title[mystep])

  if PolCalibration == True:

    plot_interactive = True

    if os.path.exists(antenna_table) == True:
      gaintable = [antenna_table, gaincurve_table, requantizer_table, opacity_table, delay_table2, BP_table2, gPint_table, gAint_table, CrossHand_table]
      gainfield = ['','','','','','',BP, BP, '']
      interp    = ['','','','','nearest','nearest','linear','linear','nearest']
    else:
      gaintable = [gaincurve_table, requantizer_table, opacity_table, delay_table2, BP_table2, gPint_table, gAint_table, CrossHand_table]
      gainfield = ['','','','','',BP, BP, '']
      interp    = ['','','','nearest','nearest','linear','linear','nearest']

    os.system('rm -rf ' + leakage_table)
    polcal(vis=vis, caltable=leakage_table,
          field         = POLD,
          scan          = POLDscan,
          spw           = sciencespw,
          solint        = 'inf',
          poltype       = 'D',
          refant=refant, combine='',
          selectdata=True,
          gaintable=gaintable,interp=interp, gainfield=gainfield)




mystep = 20
if(mystep in thesteps):
  casalog.post('Step '+str(mystep)+' '+step_title[mystep],'INFO')
  print ('Step ', mystep, step_title[mystep])

  if PolCalibration == True:

    if os.path.exists(antenna_table) == True:
      gaintable = [antenna_table, gaincurve_table, requantizer_table, opacity_table, delay_table2, BP_table2, gPint_table, gAint_table, CrossHand_table, leakage_table]
      gainfield = ['','','','','','',POLA, POLA, '','']
      interp    = ['','','','','nearest','nearest','linear', 'linear','nearest','nearest']
    else:
      gaintable = [gaincurve_table, requantizer_table, opacity_table, delay_table2, BP_table2, gPint_table, gAint_table, CrossHand_table, leakage_table]
      gainfield = ['','','','','',POLA, POLA, '','']
      interp    = ['','','','nearest','nearest','linear','linear','nearest','nearest']

    os.system('rm -rf ' + POLPA_table)
    polcal(vis=vis, caltable=POLPA_table,
           field             =  POLA,
           combine           =  'scan',
           poltype           =  'Xf',
           solint            =  'inf',
           scan              =  POLAscan,
           ###### flux calibrator spatially resolved out; limit uv range to improve solution #####
           # uvrange='0~500klambda',
           #######################################################################################
       gaintable=gaintable, gainfield=gainfield, interp=interp,
       selectdata=True)




mystep = 21
if(mystep in thesteps):
  casalog.post('Step '+str(mystep)+' '+step_title[mystep],'INFO')
  print ('Step ', mystep, step_title[mystep])

  other_calibrators = [GN]
  targets           = [TG]

  if PolCalibration == True:

    # Flux calibrator  
    if os.path.exists(antenna_table) == True:
      gaintable   = [antenna_table, gaincurve_table, requantizer_table, opacity_table, delay_table2, BP_table2, gPint_table, gAint_table, CrossHand_table, leakage_table, POLPA_table]
      gainfield   = ['','','','','','',FL,FL,'','','']
      interp      = ['','','','','nearest','nearest','linear','nearest','','','']
    else:
      gaintable   = [gaincurve_table, requantizer_table, opacity_table, delay_table2, BP_table2, gPint_table, gAint_table, CrossHand_table, leakage_table, POLPA_table]
      gainfield   = ['','','','','',FL,FL,'','','']
      interp      = ['','','','nearest','nearest','linear','nearest','','','']

    applycal(vis=vis,
         field     = FL,
         scan      = FLscan,
         parang    = True,
         gaintable=gaintable, gainfield=gainfield, interp=interp,
         calwt=False, selectdata=True
        )

    # Other calibrators
    for field in other_calibrators:
      if os.path.exists(antenna_table) == True:
        gaintable   = [antenna_table, gaincurve_table, requantizer_table, opacity_table, delay_table2, BP_table2, gPint_table, flux_table, CrossHand_table, leakage_table, POLPA_table]
        gainfield   = ['','','','','','',field,field,'','','']
        interp      = ['','','','','nearest','nearest','linear','nearest','','','']
      else:
        gaintable   = [gaincurve_table, requantizer_table, opacity_table, delay_table2, BP_table2, gPint_table, flux_table, CrossHand_table, leakage_table, POLPA_table]
        gainfield   = ['','','','','',field,field,'','','']
        interp      = ['','','','nearest','nearest','linear','nearest','','','']

      applycal(vis=vis,
               field     = field,
               parang    = True,
               gaintable=gaintable, gainfield=gainfield, interp=interp,
               calwt=False, selectdata=True
        )

    # Target source and check sources
    for field in targets:
      print('Applying calibration Tables to source: ' + field )

      if os.path.exists(antenna_table) == True:
        gaintable   = [antenna_table, gaincurve_table, requantizer_table, opacity_table, delay_table2, BP_table2, gPinf_table, flux_table, CrossHand_table, leakage_table, POLPA_table]
        gainfield   = ['','','','','','',GN,GN,'','','']
        interp      = ['','','','','nearest','nearest','linear','linear','','','']
      else:
        gaintable   = [gaincurve_table, requantizer_table, opacity_table, delay_table2, BP_table2, gPinf_table, flux_table, CrossHand_table, leakage_table, POLPA_table]
        gainfield   = ['','','','','',GN,GN,'','','']
        interp      = ['','','','nearest','nearest','linear','linear','','','']

      applycal(vis=vis,
               field     = field,
               parang    = True,
               gaintable=gaintable, gainfield=gainfield, interp=interp,
               calwt=False, selectdata=True
        )


  else:

    # Flux calibrator  
    if os.path.exists(antenna_table) == True:
      gaintable   = [antenna_table, gaincurve_table, requantizer_table, opacity_table, delay_table2, BP_table2, gPint_table, gAint_table]
      gainfield   = ['','','','','','',FL,FL]
      interp      = ['','','','','nearest','nearest','linear','nearest']
    else:
      gaintable   = [gaincurve_table, requantizer_table, opacity_table, delay_table2, BP_table2, gPint_table, gAint_table]
      gainfield   = ['','','','','',FL,FL]
      interp      = ['','','','nearest','nearest','linear','nearest']

    applycal(vis=vis,
         field     = FL,
         scan      = FLscan,
         parang    = True,
         gaintable=gaintable, gainfield=gainfield, interp=interp,
         calwt=False, selectdata=True
        )

    # Other calibrators
    for field in other_calibrators:
      if os.path.exists(antenna_table) == True:
        gaintable   = [antenna_table, gaincurve_table, requantizer_table, opacity_table, delay_table2, BP_table2, gPint_table, flux_table]
        gainfield   = ['','','','','','',field,field]
        interp      = ['','','','','nearest','nearest','linear','nearest']
      else:
        gaintable   = [gaincurve_table, requantizer_table, opacity_table, delay_table2, BP_table2, gPint_table, flux_table]
        gainfield   = ['','','','','',field,field]
        interp      = ['','','','nearest','nearest','linear','nearest']

      applycal(vis=vis,
               field     = field,
               parang    = True,
               gaintable=gaintable, gainfield=gainfield, interp=interp,
               calwt=False, selectdata=True
        )

    # Target source and check sources
    for field in targets:
      print('##### Applying calibration Tables to source: ' + field )

      if os.path.exists(antenna_table) == True:
        gaintable   = [antenna_table, gaincurve_table, requantizer_table, opacity_table, delay_table2, BP_table2, gPinf_table, flux_table]
        gainfield   = ['','','','','','',GN,GN]
        interp      = ['','','','','nearest','nearest','linear','linear']
      else:
        gaintable   = [gaincurve_table, requantizer_table, opacity_table, delay_table2, BP_table2, gPinf_table, flux_table]
        gainfield   = ['','','','','',GN,GN]
        interp      = ['','','','nearest','nearest','linear','linear']

      applycal(vis=vis,
               field     = field,
               parang    = True,
               gaintable=gaintable, gainfield=gainfield, interp=interp,
               calwt=False, selectdata=True
        )




mystep = 22
if(mystep in thesteps):
  casalog.post('Step '+str(mystep)+' '+step_title[mystep],'INFO')
  print ('Step ', mystep, step_title[mystep])

  targets           = [
                       'DMtau',
                      ]
  for field in targets:

    print( '##### Splitting calibrated data for :' + field )

    avgspw      = sciencespw
    keepflags   = False
    chanavgvis  = field + '_' + Band + 'band_' + config + '_' + EBid + '.19A262.polcal.uvaver.ms'
    width       = 64
    datacolumn  = 'corrected'
    os.system('rm -rf ' + chanavgvis)
    mstransform(
                vis=vis,
                outputvis=chanavgvis,
                field=field,
                spw=avgspw,
                datacolumn=datacolumn,
                keepflags=keepflags,
                chanaverage=True,
                chanbin=width
               )
```
{: .fs-2 }
