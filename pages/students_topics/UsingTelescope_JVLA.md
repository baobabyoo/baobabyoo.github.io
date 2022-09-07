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

You need to do it on the [NRAO online interface](my.nrao.edu). It is recommended to use Firefox, although I sometimes also use Google Chrome. Other web browsers are not necessarily well supported. After you login, click the `Obs Prep` tab. Then click into `Login to the Observation Preparation Tool (OPT)` to launch the **OPT** interface.
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

There might be multiple options. When you are observing a large number of target sources in one scheduling block, you can try to make a combination that is minimizing the slewing time. If you have any question about slewing time, you are more than welcome to contact my Master's student [Chia-Ying Chung](https://baobabyoo.github.io/pages/members.html). She can help you with this as part of a collaboration.
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

For high-frequency observations, we need to include a reference pointing scan every time we slew to a new field, e.g., before your first calibration scan (of any purpose), when you slew from passband to absolute flux calibrator (and vice versa), when you slew from any of these calibrators to the gain calibrator, etc. Here, a *new field* can be defined by an AZ-EL direction that is offset from the current pointing direction by over 20 degrees. Note that even if you are approximately staying around the same field, we still need to do reference pointing calibration approximately every 40 minutes when carrying out nighttime observations. In the daytime observations, we may want to do it every 20~30 minutes. We should use the standard X-point resource configuration if possible.
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
