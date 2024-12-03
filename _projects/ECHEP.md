---
layout: distill
permalink: /ECHEP/
title: Ecuadorian High Energy Physics Group
description: A set of quick instructions to get started
date: December 2022
bibliography: portfolio.bib
nav: false
img: assets/img/ECHEP/CMSecuador.png
importance: 1
category: work
toc:
  - name: Introduction to the basics
    # if a section has subsections, you can add them as follows:
    # subsections:
    #   - name: Example Child Subsection 1
    #   - name: Example Child Subsection 2
  - name: Introduction to CMS Physics
  - name: Machine Learning (ML) for High Energy Physics
  - name: Useful literature
---

## Introduction to the basics

If you need a few tutorials/material to start with some basic languages/programs, here there is a (non-complete and ongoing) list of suggested tutorials:

 * [Git](https://swcarpentry.github.io/git-novice/index.html): Carpentry tutorials for the basics of how to use github/gitlab. This is useful to keep your code in a online repository.
 * [Python](https://swcarpentry.github.io/python-novice-inflammation/): Carpentry tutorial for `python` and how to create plots using python tools.
 * [Root](https://root.cern/doc/master/group__Tutorials.html): THE software used in collider experiments. There are some examples in `C++` and `python`.
 * [Jupyter Notebook](https://docs.jupyter.org/en/latest/): Jupyter notebooks are the way of creating code from your browser. This is the current standard in industry and it is growing quickly in research.
 * [Kaggle](https://www.kaggle.com/): the "social network" for data analysts. It is a set of public datasets and jupyter notebooks. Highly recommended.
 * [Kaggle learn](https://www.kaggle.com/learn): a set of tutorials in many tools used in data analysis in general. These tutorials are not focused in physics, but for data analyst's.
 * [Google colab](https://colab.research.google.com): your jupyter notebooks in your google account.

## Introduction to CMS Physics

CMS has a series of schools with introductory topics for newcomers. A list of the latest schools:

 * [CMS Induction Course](https://indico.cern.ch/event/1093833/timetable/#20220620): A set of talks introducing all the main aspects of CMS. From physics, management, detector, etc.
 * [CMSDAS](https://indico.cern.ch/event/1088671/timetable/): CMS Data Analysis School is a set of talks (with videos) focused on the main aspects of data analysis in CMS. **Highly recommended**. Here one can find examples, with working code, of analysis made at CMS.

## Introduction to CERN/CMS Computing basics

### Lxplus machine

### Certificate

### VOMS


## Machine Learning (ML) for High Energy Physics

As a first introduction to what CMS is doing with ML, it is strongly recommended to follow the CMSDAS tutorial. [Link](https://indico.cern.ch/event/1088671/timetable/#90-period-5-short-exercise-mac).

_I suggest you to watch the [lecture](https://indico.cern.ch/event/1088671/contributions/4577023/attachments/2330165/4045725/GMT20220104-211221_Recording_1920x1120.mp4) and follow the [slides](https://indico.cern.ch/event/1088671/contributions/4577023/attachments/2330165/4045705/CMSDAS2021_ML_04Jan2022.pdf)._

As a **first step** towards getting used to ML tools, I suggest you to use the CMSDAS material in the [CERN SWAN](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwi1z8vfuMn7AhWSm2oFHShpDL4QFnoECA0QAQ&url=https%3A%2F%2Fswan.cern.ch%2F&usg=AOvVaw3NDWvDkT5W57BkQ8-V3xGq). SWAN is a hub created at CERN with many tools needed for CERN data analysis. For more information about SWAN follow [this link](https://swan.docs.cern.ch/intro/what_is/). Contact me if you dont have access to SWAN.

In SWAN you will be asked about the environment you need to create, at this moment you can use the default settings and click on ```Start my Session```.

<img src="https://codimd.web.cern.ch/uploads/upload_734ab2206b1d5c9222fd4faf5282260d.png" alt="drawing" width="400"/>


Once you access your SWAN projects, you can include directly github repositories by click on the button next to the plus button.

<img src="https://codimd.web.cern.ch/uploads/upload_094a01da472ebfa750df5aa0411369ac.png" alt="drawing" width="400"/>

There you can add the github link `https://github.com/FNALLPC/machine-learning-das.git` from the [repository](https://github.com/FNALLPC/machine-learning-das). After this, you will have all the jupiter notebooks in SWAN ready to run. You must start with the `0-setup-libraries.ipynb` notebook, which it will create the environment you need for the rest of the notebooks.

Jupyter notebooks are a wonderful tool to teach and to learn coding. However, since you have working code there, it is easy just to run it once and do not understand what the code is doing. I strongly suggest you to take your time to see what the example is doing. Literally play as much as you can with it.

### Some known issues

#### 3.1-dense-pytorch.ipynb

This notebook is *optional*, you can continue to notebook 4 without loosing any major information.
If you have a problem with `import torch`, you need to modify the first cell. From:
```
!{sys.executable} -m pip install torch torchvision root_pandas --user
```
to
```
!{sys.executable} -m pip install torch --user
```
Then you can run it without problems.

#### 3.2-dense-bayesian-optimization.ipynb

This notebook relies on the `skopt` package, which is recommended to use with `python3`. The current environment has `python2.7`. We can fix this issue, but for now it is not necessary.

#### 4-preprocessing.ipynb

##### Notebook restarts after running

This only means that you might need to change your environment. Go back to your main SWAN folder and in the top right, click on the three dots. There, find the option `change configuration`, which it will bring you back to the settings. In my test, it work perfectly with 16 Gb.

##### Downloading files
In this notebook, you need to access some files that exist only in the CERN storage area. For that you need to set your certificate in lxplus. If you have never installed your certificate in lxplus, please follow [this instructions](https://ca.cern.ch/ca/Help/?kbid=024010).

Then, in lxplus, run:
```
voms-proxy-init -rfc -voms cms --valid 168:00
```
it will print a message containing some information and a line that looks like this:
```
Created proxy in /tmp/x509up_u99999.
```
These file contains a certificate that you need to copy to your cernbox. To do that, run:
```
cp -p /tmp/x509up_u99999 /eos/user/X/USER/tmp/x509up_u15148
```
where `X` and `USER` depends on *YOUR* user. For instance if your cern user is agomez then `X=a` and `USER=agomez`.

Then in the notebook `4-preprocessing.ipynb`, in the first cell right after `import numpy as np`, copy:

```
##### REMEMBER TO MANUALLY COPY THE PROXY TO YOUR CERNBOX FOLDER AND TO MODIFY THE NEXT LINE
import os
os.environ['X509_USER_PROXY'] = '/eos/home-X/USER/tmp/x509up_u99999'
if os.path.isfile(os.environ['X509_USER_PROXY']): pass
else: print("os.environ['X509_USER_PROXY'] ",os.environ['X509_USER_PROXY'])
os.environ['X509_CERT_DIR'] = '/cvmfs/cms.cern.ch/grid/etc/grid-security/certificates'
os.environ['X509_VOMS_DIR'] = '/cvmfs/cms.cern.ch/grid/etc/grid-security/vomsdir'
```
where `X` and `USER` follows the same notation as before.

Once you properly modify this line, you can run it once because it will download many files needed and it will take a lot of time.

If you have any technical problem, dont hesitate on contacting me on mattermost.

**More to come**


## Useful literature

 * [Machine Learning Lectures](https://indico.cern.ch/event/619370/) Set of ML lectures with videos at CERN by Michael Kagan (SLAC)
 * [A high-bias, low-variance introduction to Machine Learning for physicists](https://arxiv.org/abs/1803.08823) A good introduction to ML for physicists (with code!).
 * [CMS ML Group](https://cms-ml.github.io/documentation/): Website of the ML group at CMS.
 * [A Living Review of Machine Learning for Particle Physics](https://iml-wg.github.io/HEPML-LivingReview/): **THE** compilation of papers on ML for High Energy Physics.
