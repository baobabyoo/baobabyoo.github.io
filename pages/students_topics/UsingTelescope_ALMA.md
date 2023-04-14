---
layout: default
title: ALMA
parent: Telescopes Tips
grand_parent: To my students
nav_order: 3
---

### If this is your first time

If you are my postdoc, and if you need me to revise English or double check the technical setup, forward me your first draft at least **2 weeks** ahead of the proposal deadline.
{: .fs-1 }

If you are my student, forward me your first draft at least **4 weeks** ahead of the proposal deadline. I will spend time iterating with you many times for education purposes.
{: .fs-1 }

If you are my student/postdoc and if you are not a native English speaker, use [Grammarly](https://www.grammarly.com/) and/or [chatGPT](https://openai.com/blog/chatgpt) to at least remove the typos and basic grammatical errors.
{: .fs-1 }

### 1. Proposing

#### 1.1 Timeline and interface

##### 1.1.1 Proposal deadline
**There is only one proposal deadline every year. It is normally in late April or early May but please pay attention to the call for proposals.** The observing cycle starts in the same October/November of the year and last for a year.
{: .fs-2 }

##### 1.1.2 Capability

The ALMA array is routinely being upgraded. Therefore, the array capability varies from cycle to cycle.
{: .fs-2 }

In addition, in a cycle (i.e., a year's observations), ALMA may optimize its array configuration schedule either for high angular resolution observations (e.g., mostly in the spatially compact array configurations) or for high-frequency or sensitive line observations (e.g., mostly in the spatially extended array configurations). It will likely focus on the extended array configuration in Cycle-10 (late 2023 to late 2024), focus on the compact array configurations in Cycle-11, focus on the extended array configurations in Cycle-12, and so on. Therefore, you need to plan ahead your experiment and make sure you do not miss the deadline (otherwise, you can only come back to propose the same experiment after 2 years). *For a student, it is good to discuss your proposal plan with your supervisor routinely.*
{: .fs-2 }

The exact capability of a cycle and the array configuration schedule is announced a month ahead of the proposal deadline. You can check them through the [Proposer's Guide](https://almascience.nao.ac.jp/proposing/proposers-guide) and [Technical Handbook](https://almascience.nao.ac.jp/proposing/technical-handbook) (Please change to the edition that is relevant to your proposal. The guides for the previous cycle is not totally usable.)
{: .fs-2 }

If you are an advanced user, you may find that the information in the Proposer's Guide or Technical Handbook imprecise, incorrect, or incomprehensive (e.g., prior to Cycle-9, the technical handbook stated that the absolute flux errors are X% without specifying that the X% refers to 2-sigma error, which is unconventional; before 2016, the alignments of the XX and YY receivers had been incorrectly documented.) This sometimes leads to incorrect proposal-preparation, proposal-review, and seriously incorrect journal publications. If you spot such issues, or if you are confused, please do reflect to the [Helpdesk](https://almascience.nao.ac.jp/help) ASAP with **no hesitation and no excuse for any delay. It can really make your proposal reviewed incorrectly and rejected unnecessarily.**
{: .fs-2 }

##### 1.1.2 Interfaces

To submit a proposal, you need an account on the [ALMA User Portal](https://almascience.nao.ac.jp/) (there are mirror sites at NA, EA, and EU. Please choose according to your present affiliation or al). Then you need to download the GUI tool,
[ALMA-OT](https://almascience.nao.ac.jp/proposing/observing-tool/installer-page). ALMA-OT allows you to prepare your proposal offline, while you can also link to your ALMA-OT account which is required when you are submitting and updating a proposal. **Register the account and download the latest version of ALMA-OT if you have not. You should do this before reading into the remaining sections.**
{: .fs-2 }

 **Try to be familiarize with all the GUI tools/interface as early as possible. There are lots of technical details. You do not want to be confused just ahead of your submission.**
{: .fs-2 }


#### 1.2 Preparation

##### 1.2.1 Feasibility, complementary data, and duplication

**Check array configuration schedule in the [Proposer's Guide]( https://almascience.nao.ac.jp/proposing/proposers-guide#autotoc-item-autotoc-51) early and make sure that your target source can be covered with the desired angular resolution.** In the case that your first choice of target sources are not available, you should consider redesigning your experiment (e.g., swapping target source, changing frequency band, or compromise your science goal, etc.)
{: .fs-2 }

**After we agree that this idea is worth pursuing and is technically feasible
, you should use the [ALMA Data Archive](https://almascience.nao.ac.jp/aq/) to check whether or not you are duplicating historical or ongoing projects.** In the case that you are duplicating, you can (1) give up and try to come up with other proposal ideas, or (2) download the archival data can see if the calibrated data can achieve the quality that is needed for your science purpose. If the quality of the archival data is fair, then just continue to use that data to proceed with your research. If there is no archival data or if the quality of the archival data is poor, you can go ahead to complete the preparation of your proposal. **You need to explicitly and convincingly explain what was the problem with the archival data if it exists. So prepare your proposal well ahead of the deadline** in case you really need to look into some archival data or need other colleagues to check the archival for you. Close to the deadline, they (and I) have to prepare their own proposals thus may refuse to help you.
{: .fs-2 }

**Do not waster your (and my) time to prepare a proposal that has a problem with unnecessary duplication. Such proposals will be rejected for 100% sure.**
{: .fs-2 }

When making the duplication checks mentioned above, you may find that there are other observations on your target source(s) which can help your science case to some extent although they do not fully resolve the problem. For example, you may find that some short-spacing observations for your high-angular resolution experiment already exist. In this case, **explicitly mentioning how** you will make use of such complementary data in the proposal is a plus. Just mentioning you will use those data but without saying how usually does not help. If you have also checked the data archive of the observatories (e.g., ALMA, JVLA, Herschel, Spitzer, etc) and found some useful complementary data, you can also mention how you will make use of them in a joint analysis.
{: .fs-2 }

##### 1.2.2 Dual anonymity

Officially, the proposers for the regular proposal queue (e.g., instead of Large Project) are required to maintain the (dual) anonymity. The proposal is not permitted to reveal the identity of the PI or co-Is in any way.
{: .fs-2 }

However, there are situations that we cannot avoid revealing the identity to a certain extent, e.g., when you are based on the data that are still in the proprietary period to justify your follow-up project. Below I explicitly quoted from the [ALMA Dual-Anonymous Guide](https://almascience.nao.ac.jp/proposing/alma-proposal-review/dual-anonymous):
{: .fs-2 }

-Instead of
{: .fs-2 }

1. "Our Cycle 5 program showed…"
2. "The data from our pilot program…"
3. "Our previous disk survey…"
{: .fs-2 }

proposers can write
{: .fs-2 }

4. "*The data from a Cycle 5 program (private communication) …*"
5. "*The data from program 2017.1.00105.S …*"
6. "*The survey from Smith et al. (2018) ...*"
{: .fs-2 }

-Instead of
{: .fs-2 }

1. "*This is a resubmission of our ongoing grade B program 2021.1.02045.S (PI: Smith). Half of our targets have been observed and we are resubmitting the proposal to obtain the remaining half.*"
{: .fs-2 }

proposers can write
{: .fs-2 }

2. "*This is a resubmission of our ongoing program. Half of the targets have been observed and we are resubmitting the proposal to observe the remaining half.*"
{: .fs-2 }

##### 1.2.3 Proposal types (scopes)

- Regular proposal:
  1. **<50 hours** on the *12-m Array*,
  2. or **<150 hours** on the *7-m Array* in stand-alone mode.
  3. Regular proposals may involve time-critical, multiple-epoch observations, and the monitoring of a target over a fixed time interval.
  4. Most Cycle-9 regular projects requested **2~20 hours of 12m-Array observing time**. The acceptance rate depends weakly on the requested observing time unless it exceeds 30 hours.
- Target of Opportunity (ToO)
  1. The target source is not known by the time of proposing.
- Large Projects
  1. Cannot use the newest capability (Band1, full polarization, solar observations, VLBI, Phased Array mode, Astrometric observations)
  2. Cannot do ToO observations.
  3. The team needs to deliver value-added data products and a documentation to it.
- Joint Proposal (Proposers can submit a Joint Proposal to ALMA that also requests time on any or all of the partner facilities or submit a proposal to one of **JWST**, **VLA**, or **VLT** that requests ALMA time.) **PIs must submit their Joint Proposals to the observatory that requires the most observing time. Duplication is not permitted.** Proposers need to provide technical details for all involved observatories. Joint Proposals accepted by ALMA will be assigned Grade A; they will have high observing priority and will remain in the queue for a period of up to two years.
  1. JWST (can allocate 115 hours to each of ALMA, ACA, and TP)
  2. JVLA (can allocate 50 hours to each of ALMA, ACA, and TP)
  3. VLT (can allocate 115 hours to each of ALMA, ACA, and TP)
{: .fs-2 }

##### 1.2.4 Scientific justification and how your proposals will be reviewed

To complete the proposal submission, you need a **title**, an **Abstract**, a PDF scientific justifications with **4 pages of text and Figures/Tables for regular projects** (up to 6 pages for Large Projects). If you are not sure about how to compose the Abstract or the 4 or 6 pages scientific justification, check [here](https://baobabyoo.github.io/pages/students_topics/proposal_obs.html).
{: .fs-2 }

Usually, we prepare the 4 pages justifications using LaTEX. Download the latest version of the [ALMA proposal template](https://almascience.nao.ac.jp/proposing/proposal-template) and use it without changing anything about page setup or format. If you are my student/postdoc, please use the [Overleaf](https://www.overleaf.com/) interface to edit the proposal and share the link with me, *if you need my revision*. Use **fontsize 12pt which is strictly required by ALMA.** *Do not use smaller fontsize for your figure captions.* Do not use a very small margin. Try not to make your proposal over-texty. No reviewer wants to spend more than **5 minutes** reading your proposal. Do not make it necessary for them to do so.
{: .fs-2 }

Although you are not required to justify the technical details of your experimental setups (e.g., angular resolution, sensitivity, mosaic field of view, spectral setup, etc) in the Scientific Justification, I still strongly recommend you to do so. This is because not everybody read into the technical justification pages carefully.
{: .fs-2 }

After exporting the PDF file of your scientific justification, you need to attach it to the project you created with [ALMA-OT](https://almascience.nao.ac.jp/proposing/observing-tool/installer-page).
{: .fs-2 }

The team of every submitted regular proposal needs to share the duty of reviewing 10 regular proposals. The PI of every regular proposal must designate themselves or a Co-I as a reviewer at the time of submission. **In addition, starting from Cycle-10 (proposal deadline in 2023 May), no one is permitted to review more than 5 proposals.** *(e.g., if you write 6 proposals as PI, you have to designate at least one of your co-I as a reviewer for at least one of those 6 projects)*.
{: .fs-2 }

This means that you have to plan ahead in case you do not find a suitable person to designate the reviewing duty. **And you can see that the 10 reviewers of every one of your regular proposal are just like you and me: some are real experts but most are inexperienced with the analyses that you propose to do. The goal of the proposal writing is to make all 10 of them happy: your proposal can be rejected just because of receiving bad grade from one or two of them, in particular, when you are attempting non-standard capability or high frequency observations.**
{: .fs-2 }

**Therefore, the proposal cannot be over-basic that upset the experts, while it also cannot be over-advanced such that it loses the general reviewers at hello. I do not find a general strategy to tackle this problem yet (e.g., every time there are reviewers complaining that position-velocity diagrams are too difficult to understand; at the same time, there are also reviewers who questioned why I did not prepare a position-velocity diagram which is the best way of revealing the kinematics features). After ALMA started using such distributed peer review, my best proposals have always been rejected at bottom rating........** I am certainly not the only person making such complaints. After all, the proposing process may become a lottery to a large extent, Urrrrr.......
{: .fs-2 }

##### 1.2.5 Technical justification

You need to include your target sources and set the spectral step(s), angular resolution(s), largest recoverable angular scale(s), and sensitivity on the [ALMA-OT](https://almascience.nao.ac.jp/proposing/observing-tool/installer-page) file. If you do not know the rest frequency of the spectral line(s) you want to observe, you can check the [Splatalogue](https://splatalogue.online//), otherwise, consult [chatGPT](https://openai.com/blog/chatgpt).
{: .fs-2 }

If there is any term on ALMA-OT that you do not know the exact meaning, consult [chatGPT](https://openai.com/blog/chatgpt) and then make your you do understand it. Try not making low-level mistakes and/or leaving it as a duty for your collaborators to go through all technical details again. Close to the ALMA proposal deadline, everybody is very busy. It would be a big favor if anyone help you with the technical details. Request help only when it is really necessary (e.g., when you need to carry out a circular polarization experiment, which is something that most of the users have not been educated with the technical background.)
{: .fs-2 }

The selected spectral setups, angular resolution(s), and sensitivity also need to be explicitly explained on the ALMA-OT file. The quantitative needs to be quantitative and comprehensive. Do not leave any open question in the technical justifications, e.g., if you say you need to detect your target source at 10-sigma significance, then it would be good to explain why you need it to be 10-sigma instead of 5-sigma: the former requires 4 times longer on-source integration time than the latter!
{: .fs-2 }

*Finally, when you design a project, you should keep in mind that the minimum length of a scheduling block (the unit of observation) is 0.5 hours (for polarization project it is 3 hours). Historically, not many observations were executed with longer than 2 hours' scheduling blocks.*
{: .fs-2 }

### 2. Organizing observing scripts

Your observing script is usually automatically generated. You will be contacted by staff in the ALMA Regional Center to proofread your observing script. Please make sure the coordinates and the spectral setups are indeed what you intend to use (in most cases, the problems were due to users' mistakes). In some cases you also need to make sure that the calibration will be carried out in the way you need (or say, not be carried out in the way that you cannot use. For example, in the earlier cycles, the algorithm would choose Sgr A\* as your calibrator even when your target source is also Sgr A\*. There needs extra work for the staff to avoid such issues.)
{: .fs-2 }

### 3. Operation

ALMA staff will execute your observing script and will watch over the observations. So usually, there is nothing you need to do.
{: .fs-2 }

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

#### 4.2 Simple imaging scripts

##### 4.2.1 Continuum imaging (with flow control)

This procedure first list the details of the observations using the CASA **listobs()** task. Then it plots the visibility amplitudes versus spectral channels using the CASA **plotms()** task to allow visually inspecting whether or not there are strong emission/absorption lines in our passband (note that the visibility amplitudes are positively definite and therefore the absorption lines will also appear as positive peaks). Then it runs the inverse Fourier transform and deconvolution using the CASA **tclean()** task, and then corrects the [primary beam response function](https://baobabyoo.github.io/pages/students_topics/AstroBasic_RadioInterferometer.html#how-a-radio-interferometer-look-like) using the **impbcor** task. Here you have to carefully understand the parameters/keywords in the tclean task to be able to use it properly; they need to be optimized case-by-case. For example, in tclean(), we use the keyword `specmode   =  'mfs'` to produce a continuum image using the aggregated bandwidth provided by all (selected) spectral channels. For imaging the observations on a single field, we can use `gridder  =  'standard'`; to image the Stokes I mosaic observations (i.e., an image made with multiple antennae pointings), we have to use `gridder  =  'mosaicft'`; to image the full polarization mosaic observations, we have to use `gridder  =  'awprojectft'`.
{: .fs-2 }

Finally, this procedure uses the CASA **exportfits()** task to export the results of imaging to the FITS format binary files.
{: .fs-2 }

You can copy the content of this script to an ASCII file, e.g., imaging.py. To run the script from begin to end, in the CASA ipython interface, enter
{: .fs-2 }

```
CASA> execfile('imaging.py')
```
{: .fs-2 }

To execute one or a few steps at a time, try something like the following:
{: .fs-2 }

```
CASA> mysteps = [1,2]
CASA> execfile('imaging.py')
```
{: .fs-2 }
```
CASA> mysteps = [3]
CASA> execfile('imaging.py')
```
{: .fs-2 }

Below is the procedure:
{: .fs-2 }

```
import os
# using the data taken from https://casaguides.nrao.edu/index.php/First_Look_at_Imaging
# To uncompress .tgz file, e.g.,
#    tar -zxvf file.tgz
# To uncompress .tar file
#    tar -xvf file.tar
#
# To load a CASA task, e.g.,
#   CASA> tget task_name
# To check helpfile
#   CASA> help task_name
#
# To execute a script in CASA ipython interface
#   CASA> execfile('script.py')

##### flow control #######################################
thesteps = []
step_title = {
                0: 'List observational details',
                1: 'Inspecting spectrum',
                2: 'Perform imaging',
                3: 'Primary beam correction',
                4: 'exporting FITS image'
             }

try:
  print ('List of steps to be executed ...', mysteps)
  thesteps = mysteps
except:
  print ('global variable mysteps not set.')
if (thesteps==[]):
  thesteps = range(0,len(step_title))
  print ('Executing all steps: ', thesteps)
##########################################################

##### Setup parameters ###################################
filename = 'sis14_twhya_selfcal'
fields    = ['3c279']
stokes    = ['I']
interactive = True
dropdeg     = True
##########################################################

mystep = 0
if(mystep in thesteps):
    print ('Step ', mystep, step_title[mystep])

    os.system('rm -rf ' + filename + '.listobs')
    listobs(vis = filename + '.ms',
            listfile = filename + '.listobs'
           )


mystep = 1
if(mystep in thesteps):
    print ('Step ', mystep, step_title[mystep])

    for field in fields:
        outfig = filename + '_' + field + '.spectrum.png'
        os.system('rm -rf ' + outfig)
        plotms( vis   = filename + '.ms',
                xaxis = 'channel', yaxis = 'amplitude',
                field = field,
                coloraxis = 'antenna1',
                plotfile  = outfig
              )


mystep = 2
if(mystep in thesteps):
    print ('Step ', mystep, step_title[mystep])

    for stoke in stokes:
        for field in fields:

            imagename = field + '_' + stoke
            os.system('rm -rf ' + imagename + '.*')
            tclean( vis   = filename + '.ms',
                    selectdata = True,
                        field = field,
                        spw   = '0',
                    datacolumn = 'corrected',
                    imagename  = imagename,
                    cell       = ['0.1arcsec'], imsize = [300,300],
                    stokes     = stoke,
                    specmode   = 'mfs',  # multi-freqency synthesis continuum imaging
                    gridder    = 'standard',
                    pblimit    = 0.2,
                    deconvolver = 'hogbom',
                    weighting   = 'briggs',
                        robust  = 2.0,
                    niter      = 10000,
                    interactive = interactive,
                    restart     = True,
                    threshold = '0.1Jy'
              )


mystep = 3
if(mystep in thesteps):
    print ('Step ', mystep, step_title[mystep])


    for stoke in stokes:
        for field in fields:

            imagename = field + '_' + stoke
            outfile   = field + '_' + stoke + '.pbcor.image'
            os.system('rm -rf ' + outfile)
            impbcor(imagename = imagename + '.image',
                    pbimage   = imagename + '.pb',
                    outfile   = outfile
                   )

mystep = 3
if(mystep in thesteps):
    print ('Step ', mystep, step_title[mystep])


    for stoke in stokes:
        for field in fields:

            imagename = field + '_' + stoke
            suffixes  = ['.image', '.pbcor.image']
            for suffix in suffixes:
                exportfits(
                            imagename = imagename + suffix,
                            fitsimage = imagename + suffix + '.fits',
                            overwrite = True,
                            dropdeg   = dropdeg
                          )
```
{: .fs-2 }


##### 4.2.2 Spectral line imaging (with flow control)

The procedure to perform spectral line imaging is not too different from that of the continuum imaging. A major difference is that we need to use other `specmode` options in the CASA **tclean()** task. In addition, you may want to reset the **rest-frequency** to conveniently make the velocity gridding. You can look up the rest frequency of most of the molecular transitions that you might be interested in on the [Splatologue](https://splatalogue.online//) webpage. In addition, before running CASA **tclean()**, we usually (which is not always necessary, depending on your science case) visually inspect the visibility spectra using the CASA **plotms()** task, and separate the continuum and line emission using the CASA **uvcontsub()** task.
{: .fs-2 }

```
import os

##### flow control #######################################
thesteps = []
step_title = {
                0: 'List observational details',
                1: 'Inspecting spectrum',
                2: 'Separating continuum and line',
                3: 'Perform imaging',
                4: 'Primary beam correction',
                5: 'exporting FITS image'
             }

try:
  print ('List of steps to be executed ...', mysteps)
  thesteps = mysteps
except:
  print ('global variable mysteps not set.')
if (thesteps==[]):
  thesteps = range(0,len(step_title))
  print ('Executing all steps: ', thesteps)
##########################################################

##### Setup parameters ###################################
filename = 'nh3'
fields    = ['l429']
stokes    = ['I']
interactive = True
dropdeg     = True
##########################################################

mystep = 0
if(mystep in thesteps):
    print ('Step ', mystep, step_title[mystep])

    os.system('rm -rf ' + filename + '.listobs')
    listobs(vis = filename + '.ms',
            listfile = filename + '.listobs'
           )


mystep = 1
if(mystep in thesteps):
    print ('Step ', mystep, step_title[mystep])

    for field in fields:
        outfig = filename + '_' + field + '.spectrum.png'
        os.system('rm -rf ' + outfig)
        plotms( vis   = filename + '.ms',
                xaxis = 'channel', yaxis = 'amplitude',
                field = field,
                coloraxis = 'antenna1',
                plotfile  = outfig
              )



mystep = 2
if(mystep in thesteps):
    print ('Step ', mystep, step_title[mystep])

    fitspec = {
               '0': {'0': {'chan': '111~283;356~444;512~591;662~851', 'fitorder': 0} }
              }

    linems = filename + '_contsub.ms'
    os.system('rm -rf ' + linems)
    uvcontsub(
              vis        = filename + '.ms',
              outputvis  = linems,
              fitspec    = fitspec, # check the help file with 'CASA> help uvcontsub' to see how to set this
              datacolumn = 'data',
              writemodel = False
             )


mystep = 3
if(mystep in thesteps):
    print ('Step ', mystep, step_title[mystep])

    linems = filename + '_contsub.ms'
    for stoke in stokes:
        for field in fields:

            imagename = field + '_' + stoke
            os.system('rm -rf ' + imagename + '.*')
            tclean( vis   = linems,
                    selectdata = True,
                        field = field,
                        spw   = '0',
                    datacolumn = 'data',
                    imagename  = imagename,
                    cell       = ['0.5arcsec'], imsize = [300,300],
                    stokes     = stoke,
                    specmode   = 'cube',  # Spectral line imaging with one or more channels
                        nchan = 200,
                        start = 400,
                        width = 1,
                        outframe = 'LSRK', # reference system of velocity (LSRK: local standard of rest system)
                        veltype  = 'radio',
                        restfreq = ['23.69449550GHz'],   # rest frequency of the NH3 hyperfine inversion line
                        interpolation = 'linear',
                    gridder    = 'standard',
                    pblimit    = 0.2,
                    deconvolver = 'hogbom',
                    weighting   = 'briggs',
                        robust  = 2.0,
                    restoringbeam =    'common',
                    niter      = 0,
                    interactive = interactive,
                    restart     = True,
                    threshold = '5e-3Jy'
              )


mystep = 4
if(mystep in thesteps):
    print ('Step ', mystep, step_title[mystep])


    for stoke in stokes:
        for field in fields:

            imagename = field + '_' + stoke
            outfile   = field + '_' + stoke + '.pbcor.image'
            os.system('rm -rf ' + outfile)
            impbcor(imagename = imagename + '.image',
                    pbimage   = imagename + '.pb',
                    outfile   = outfile
                   )

mystep = 5
if(mystep in thesteps):
    print ('Step ', mystep, step_title[mystep])


    for stoke in stokes:
        for field in fields:

            imagename = field + '_' + stoke
            suffixes  = ['.image', '.pbcor.image']
            for suffix in suffixes:
                exportfits(
                            imagename = imagename + suffix,
                            fitsimage = imagename + suffix + '.fits',
                            overwrite = True,
                            dropdeg   = dropdeg
                          )
```
{: .fs-2 }
