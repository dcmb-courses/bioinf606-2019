---
layout: page
title: Setup 
permalink: /setup/
---

# Software Requirements & Setup Instructions
To fully participate in this boot camp, you will need access to the software described below on **your own laptop** (N.B. You will likely need _Administer privileges/permissions_ to install some of these). 

**Access to the FLUX computer cluster:**
In addition to the software listed further below, you will require access to the University of Michigan FLUX computer cluster. To obtain access to FLUX you will need to first fill out this [online form](https://arc-ts.umich.edu/fluxform/) with your UMICH unique name, the advisor name of "Michael Boehnke" (email: boehnke@umich.edu) and list "Participant in Introduction to Biocomputing course (BIOS/BIOI/HG 606)" in the project description field.

You must use **Duo authentication** to log on to Flux. Most people find using the Duo Mobile app on a smartphone to be most convenient method. This entials installing the app and then confirming a notification on your phone at the time of login. For more details see: [http://its.umich.edu/two-factor-authentication](http://its.umich.edu/two-factor-authentication). We will cover FLUX login and usage on [Day 4]({{ site.baseurl }}/day4/) of this course.


<br>

### The Bash Shell
Bash is a commonly-used shell that gives you the power to do simple tasks more quickly.

**Windows:** Install [MobaXterm](http://mobaxterm.mobatek.net), an enhanced terminal with bash for Windows. Note that the default 'Personal Edition install' typically places the MobaXterm executable in `C:\Program Files (x86)\Mobatek\MobaXterm Personal Edition`.  

Please also install the [**Plugin CygUtils**](http://mobaxterm.mobatek.net/CygUtils.plugin). Once downloaded please move the `CygUtils.plugin` file to the folder `C:\Program Files (x86)\Mobatek\MobaXterm Personal Edition`. Launching mobaxterm will complete the install.  

**Mac OS X:** You do not need to install anything. You can access bash from the **Terminal** (found in **/Applications/Utilities**). You may want to keep Terminal in your dock for this class.

**Linux:** There is no need to install anything.

<br>

### Git
Git is a version control system that lets you track who made changes to what and when. To work with GitHub and BitBucket you will need a [supported web browser](https://help.github.com/articles/supported-browsers/) (current versions of Chrome, Firefox or Safari, or Internet Explorer version 9 or above).

**Windows:** Git should be installed as a plugin to mobaxterm. Download the plugin for [**Git**](http://mobaxterm.mobatek.net/plugins/Git.mxt3). Once downloaded please move the `Git.mxt3` file to the folder `C:\Program Files (x86)\Mobatek\MobaXterm Personal Edition`. Launching mobaxterm will complete the install.  


**Linux:** If Git is not already available on your machine you can install it via your distro's package manager. For Debian/Ubuntu run 

    sudo apt-get install git 

and for Fedora run 

    sudo yum install git.

<br>

### Text Editor
When you're writing code, it's nice to have a text editor that is optimized for writing code, with features like automatic color-coding of key words. The default text editor on Mac OS X and Linux is usually set to Vim, which is not famous for being intuitive. if you accidentally find yourself stuck in it, try typing the **escape key**, followed by **:q!** (colon, lower-case 'q', exclamation mark), then hitting Return to return to the shell.

**Windows:** nano is a basic editor and the default that instructors use in the workshop. Nano should be installed as a plugin to mobaxterm (see above **Git** instructions for windows).

**Mac OS X:** nano should be pre-installed.

**Linux:** nano should be pre-installed.


<br>

### Python
Python is a popular language for scientific computing. Installing all of its scientific packages individually can be a bit difficult, so we recommend an all-in-one installer.

Regardless of how you choose to install it, please make sure you install Python version 2.x and not version 3.x (e.g., 2.7 is fine but not 3.4). Python 3 introduced changes that will break some of the code we teach during the workshop.

We will teach Python using the IPython notebook, a programming environment that runs in a web browser. For this to work you will need a reasonably up-to-date browser. The current versions of the Chrome, Safari and Firefox browsers are all supported (some older browsers, including Internet Explorer version 9 and below, are not).

**Windows:** Download and install [Anaconda](http://continuum.io/downloads.html).
Download the default **Python 2 graphical installer** installer (do not follow the link to version 3). Use all of the defaults for installation except make sure to check _Make Anaconda the default Python_.

**Mac OS X:** Download and install [Anaconda](http://continuum.io/downloads.html).
Download the default "Mac OS X **Python 2.7** Graphical Installer" (do not follow the link to version 3). Use all of the defaults for installation.

**Linux:** We recommend the all-in-one scientific Python installer [Anaconda](http://continuum.io/downloads.html).

