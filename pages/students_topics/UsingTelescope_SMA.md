---
layout: default
title: SMA
parent: Telescopes Tips
grand_parent: To my students
nav_order: 1
---

#### If this is your first time

If you are my postdoc, and if you need me to revise English or double check the technical setup, forward me your first draft at least **2 weeks** ahead of the proposal deadline.
{: .fs-1 }

If you are my student, forward me your first draft at least **4 weeks** ahead of the proposal deadline. I will spend time iterating with you many times for education purposes.
{: .fs-1 }

#### Proposing

**There are two proposal deadlines each year. They are normally in mid-March and mid-September but please pay attention to the call for proposals.**
{: .fs-2 }

Please register an **account** at the [SMA Observer Center](http://sma1.sma.hawaii.edu/) well ahead of the proposal deadline (e.g., one month ahead or earlier). You need to log in and familiarize yourself with how to prepare for the cover-page online.
{: .fs-2 }

Usually, you try to form a rough idea about what you are going to propose (target source(s), resolution, spectral setup, and sensitivity). Let's say, this is at least 1~1.5 months ahead of the proposal deadline. If you are my student and postdoc, please come discuss with me about this rough idea.
{: .fs-2 }

**After we agree that this idea is worth pursuing and is technically feasible
, you should use the [SMA Data Archive](https://lweb.cfa.harvard.edu/cgi-bin/sma/smaarch.pl) to check whether or not you are duplicating historical or ongoing projects.** In the case that you are duplicating, you can (1) give up and try to come up with other proposal ideas, or (2) download the archival data can see if the calibrated data can achieve the quality that is needed for your science purpose. If the quality of the archival data is fair, then just continue to use that data to proceed with your research. If there is no archival data or if the quality of the archival data is poor, you can go ahead to complete the preparation of your proposal. **You need to explicitly and convincingly explain what was the problem with the archival data if it exists. So prepare your proposal well ahead of the deadline** in case you really need to look into some archival data or need other colleagues to check the archival for you. Close to the deadline, they (and I) have to prepare their own proposals thus may refuse to help you. **Do not waster your (and my) time to prepare a proposal that has a problem with unnecessary duplication. Such proposals will be rejected for 100% sure.**
{: .fs-2 }

To complete the proposal submission, you need a **title**, an **Abstract**, a PDF scientific justifications with **2 pages of text and 2 pages of Figures/Tables**. If you are not sure about how to compose the Abstract or the 2+2 pages scientific justification, check [here](https://baobabyoo.github.io/pages/students_topics/proposal_obs.html).
{: .fs-2 }

Usually, we prepare the 2+2 pages justifications using LaTEX. If you are my student/postdoc, please use the [Overleaf](https://www.overleaf.com/) interface and share the link with me, *if you need my revision*. Use **fontsize 12** as far as you can. *Never make fontsize smaller than 11.* Do not use a very small margin. Try not to make your proposal over texty. No reviewer wants to spend more than **5 minutes** reading your proposal. Do not make it necessary for them to do so.
{: .fs-2 }

You will need to include your **observing time requests** through the online interface at the [SMA Observer Center](http://sma1.sma.hawaii.edu/). The observation for **each target source** at **each array configuration** with **each receiver tuning** need an independent observing time request that states how many hours you need for that target source at that setup. Based on the record(s) of your observing time request, the reviewers will check whether or not you are duplicating historical or ongoing projects unnecessarily.
{: .fs-2 }

******************************************************************************

You can check your **spectral setup (i.e., receiver tuning)** at [this page](http://sma1.sma.hawaii.edu/smaPassbandViewer/smaPassbandVis2020A.html). Usually, SMA does not re-tune the receiver for a PI in a night (e.g., it will not consider a project that requests to make short observations on one single target with >2 different receiver tunings; using two different tunings in one project in a night is already very rare since that costs a lot of overhead time in the (re-)tuning and in the passband calibration). If you are not sure about what tuning is feasible or not feasible, come discuss with me.
{: .fs-2 }

You can check the **angular resolution** and **sensitivity** *at your observing frequency* at [this page](http://sma1.sma.hawaii.edu/beamcalc.html).
{: .fs-2 }

Use [this page](http://sma1.sma.hawaii.edu/callist/callist.html) to check which **gain and passband calibrators** are ideal for your project. Usually, I try to pick a >0.7 Jy quasar as gain calibrator. It is the best if the angular separation between this quasar and your target source is less than 10 degrees. When the separation is in the range of 10~20 degrees, the phase errors can be noticible. A quasar that is >20 degrees separated from your target source should not be considered as you gain calibrator unless you are sure that your target source can be self-calibrated. Passband calibrator can be 3C84 or 3C279; bllac may be OK if you are not observing CO J=2-1 or CO J=3-2.
{: .fs-2 }

You can use [this page](http://sma1.sma.hawaii.edu/planetvis.html) to check which Solar System object can be your **absolute flux calibrator**. But don't worry too much about this. The SMA scheduler always double-checks which is the best one on the date of your observations.
{: .fs-2 }

******************************************************************************

A regular SMA proposal can request up to 100 hours of observing time. If you need 100~1000 hours, there is a Large Project category which is relatively hard. If you want to submit a Large Project proposal, prepare early. If you are student or postdoc in Taiwan, I would consider that it is fair to request **2~4 nights** of observing time in each proposal. If you are a Master's student and if your thesis is going to base on this SMA proposal, I would encourage you to think big and consider a project with **5~10 nights** of overall observing time. A night corresponds to 8~10 hours.
{: .fs-2 }

#### Organizing observing scripts

Here is a step-by-step guide:
{: .fs-2 }

Check the previous section if you are not sure how to pick calibrators (the relevant parts are in between the two horizontal gray lines); check [this page](https://baobabyoo.github.io/pages/students_topics/AstroBasic_RadioInterferometer.html) if you are confused about any thing (or everything).
{: .fs-1 }

1. Log in to the [SMA Observer Center](http://sma1.sma.hawaii.edu/).
2. Click the **My Projects** tab on the left.
3. From the list of your project, click into the relevant one. You will see the allocated observing tracks in the **Summary of tracks** section in the bottom. If there is not yet an observing script, there will be red text saying *(needs script)*.
4. Click **Track overview & script** next to the *(needs script)* text.
5. Scroll down to the **Observing Script** section. If you have never prepared an SMA script, then click **create new script using script generator**. If you are experienced, or if you are modifying a previously created script, you can click **manage script directory** will allows you to edit the ASCII script file.
6. The online **script generator** has self-contained explanation. You can follow through what it asks you to fill.
7. After a preliminary script is prepared using the script generator, and after you save the script, the online interface will allow you to enter the prospective UTC time of this observation and then **simulate** how the script works. After the start of a semester, a rough array configuration schedule will be provided [here](http://sma1.sma.hawaii.edu/array_config_sched.html). From there you can check in which month your project may be executed, and then use the simulator to see if all the calibrators can be observed above the elevation limit, and if the cycle time(s) of the target source loop(s) is indeed what you expect. You should definitely run this simulator and make sure there is no error message (e.g., any syntax error in your script that cause failure, or if your target source or calibrator goes above/below the elevation limit).
8. Sometimes you may need to control the LST start/end time of your target source loops (e.g., when you have multiple groups of target sources that need different gain calibrator, or when you want to control the duration of each target source loop). You can then click **manage script directory** can use the command like the following example:
{: .fs-2 }

```
print "----- main science target observe loop (vytau, xztau) -----\n";
$LST_start=20; $LST_end=2;
  &ObsLoop(cal1,targ3,targ4);

print "----- main science target observe loop (v1143ori, v1183ori, nyori)-----\n";
$LST_start=1.5; $LST_end=12;
  &ObsLoop(cal0,targ1,targ2,targ3);
```

The `print` commands does not do anything to the telescopes; it just prints some text to let the operator see what the array is going to do. Do simulate the script after making such edits in case of any surprise.
{: .fs-2 }

#### Operation

A SMA operator will execute your observing script and will watch over the observations. So usually, there is nothing you need to do. But if you would like to participate in the operation or would like to monitor the operation, let me know.
{: .fs-2 }

#### Data calibration and imaging

You will need some software. An overview of them is provided [here](https://lweb.cfa.harvard.edu/rtdc/SMAdata/process/overview/).
{: .fs-2 }

The official software package to calibrated the SMA data is [MIR IDL](https://lweb.cfa.harvard.edu/~cqi/mircook.html). You can find examples of MIR IDL calibration procedures in that MIR IDL webpage (or click [here](https://lweb.cfa.harvard.edu/~cqi/mir/mirscript_2016jan22.txt) for the 2016 version and [here](https://lweb.cfa.harvard.edu/~cqi/mir/mir2018.txt) for the 2018 version). To use MIR IDL, you will need to install [IDL](https://www.l3harrisgeospatial.com/Software-Technology/IDL). It is not free (it is ultra expensive). If you do not have an access to an IDL license, come ask me.
{: .fs-2 }

Note that MIR IDL will load all raw data in a file to the memory of your computer. The loaded data will in fact occupy twice the raw data filesize in the memory due to using double precision variables (e.g., if the raw filesize is 100 GB, then it will occupy 200 GB in your memory). If the raw filesize is too large for your computer, you can use the [SMA Data Rechunker code](https://lweb.cfa.harvard.edu/rtdc/SMAdata/process/rechunk/) to bin the spectral channels to reduce the filesize, before loading into MIR IDL.
{: .fs-2 }

You can also use the [CASA software package](https://lweb.cfa.harvard.edu/rtdc/SMAdata/process/casa/) to calibrate the SMA data, which is less subject to memory issue (by design, CASA can handle large raw data with a computer with relatively small memory, although it can be very slow if the memory is way too small). By the time of early 2022, the CASA data reduction path remained somewhat experimental.
{: .fs-2 }

I usually use the [Miriad](https://lweb.cfa.harvard.edu/rtdc/SMAdata/process/miriad/) software package to image the SMA data. You can also use it to calibrate the SMA data. You can also use CASA to image your SMA data although it is a lot slower than Miriad.
{: .fs-2 }

#### Publishing

You are required to include the following statement in the Acknowledgement:
{: .fs-2 }

*
The Submillimeter Array is a joint project between the Smithsonian Astrophysical Observatory and the Academia Sinica Institute of Astronomy and Astrophysics, and is funded by the Smithsonian Institution and the Academia Sinica (Ho et al. 2004).
*
{: .fs-2 }

You are required to cite [Ho et al. (2004)](https://ui.adsabs.harvard.edu/abs/2004ApJ...616L...1H/abstract).
{: .fs-2 }

Your are required to cite [Sault et al. (1995)](https://ui.adsabs.harvard.edu/abs/1995ASPC...77..433S/abstract), [Qi et al. (2003)](https://ui.adsabs.harvard.edu/abs/2003cdsf.conf..393Q/abstract), or [McMullin et al. (2007)](https://ui.adsabs.harvard.edu/abs/2007ASPC..376..127M/abstract) if you use Miriad, MIR IDL, or CASA to process your data.
{: .fs-2 }


#### When you get stuck

If you are located in Taiwan, you can either ask me or my present Master's student, [Chia-Ying Chung](http://www.asiaa.sinica.edu.tw/people/cv.php?i=cychung).
{: .fs-2 }

Note that she is not obligated to work for you or answer your questions regardless of your career stage. If you are making a very big request to her, for example, if you need her to teach you or walk you through data calibrations, or even calibrate data for you, then you should regard this as a formal collaboration and should include her as a co-I when you are making a journal publication. Please appreciate that it takes a very significant effort for her to pick up this skill. She still has the right to say no to you (so be nice to her). I also have the right to say no to you for her, to ensure that she can be sufficiently focused on her thesis project.
{: .fs-1 }
