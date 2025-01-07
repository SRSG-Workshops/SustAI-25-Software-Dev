---
title: Setup for SustAI 2025 Introduction to Research Software Development
---


# The Bash Shell

## Text Editor ##

A text editor is the piece of software you use to view and write code. If you
have a preferred text editor, please use it. Suggestions for text editors are,
Notepad++ (Windows), TextEdit (macOS), Gedit (GNU/Linux), GNU Nano, Vim.
Alternatively, there are IDE's (integrated developer environments) that have
more features specifically for coding such as VS Code; there are also IDEs
specific to languages will be listed in the appropriate section(s) below.

## Open a Terminal ##

For this lesson, first you need to be able to open a terminal:

- **On Windows:** We'll be using Git Bash. If you've already installed Git Bash then go to the next section. Otherwise, go to [git for windows](https://gitforwindows.org/) and click **Download**, then install it. 
Most of the options can be left on default, but be sure you check these:
  - **Choosing the default editor used by Git:** Make sure **Nano** is selected from the drop-down. If you're comfortable with other editors, feel free to change it, but we recommend Nano - we use it as it's present on Windows, Mac *and* Linux. If you change it, you might not quite match what we're doing on-screen.
  - **Adjusting your PATH environment:** Make sure **Git from the command line and also from 3rd-party software** is selected.
  - **Choosing HTTPS transport backend:** Make sure **Use the native Windows Secure Channel Library** is selected.
  - **Configuring the terminal emulator to use with Git Bash:** Make sure **Use Windows' default console window** is selected.

- **On Mac OS X:** accessed by opening the “Terminal” application, which can be found in the “Utilities” folder which is in your “Applications” folder.
- **On Linux:** this will depend on the Linux distribution you are running, but you should be able to find a "Terminal" application in your desktop's application menu.



## Git Setup ##

### Windows
We'll be using Git Bash for both git and a shell to run it in. If you've already installed Git Bash then go to the next section. Otherwise, go to [git for windows](https://gitforwindows.org/) and click **Download**, then install it.
Most of the options can be left on default, but be sure you check these:
  - **Choosing the default editor used by Git:** Make sure **Nano** is selected from the drop-down. If you're comfortable with other editors, feel free to change it, but we recommend Nano - we use it as it's present on Windows, Mac *and* Linux. If you change it, you might not quite match what we're doing on-screen.
  - **Adjusting your PATH environment:** Make sure **Git from the command line and also from 3rd-party software** is selected.
  - **Choosing HTTPS transport backend:** Make sure **Use the native Windows Secure Channel Library** is selected.
  - **Configuring the terminal emulator to use with Git Bash:** Make sure **Use Windows' default console window** is selected.

#### Mac OS
To use Git you must install the Apple Command Line Tools, this may take a few minutes.  

You can obtain these [from Apple](https://developer.apple.com/download/more/?name=command%20line%20tools%20for%20xcode%2012) (requires your Apple ID)

- Select **Command Line Tools for Xcode 12 (or higher)** and click the link to download the dmg archive.
- If prompted, choose to allow downloads from developer.apple.com
- Open the downloaded dmg archive from the Downloads folder
- Double-click the Command Line Tools.pkg icon to install

Alternatively, you can install the tools from the command line:

~~~
$ xcode-select --install
~~~
{: .language-bash}

#### Linux
Git comes pre-installed on most Linux distributions. You can test if it's installed by running `git --version`. 
If it's not installed, you can install it by running `sudo apt-get install git` or `sudo yum install git`, depending on 
your distribution.


## GitHub ##
We'll be using the website [GitHub](https://github.com/) to host, back up, and distribute our code. You'll need to [create an account there](https://github.com/signup). As your GitHub username will appear in the URLs of your projects there, it's best to use a short, clear version of your name if you can.


## Download Data for Shell Lesson ##

Open a terminal and type the following into the prompt that appears (pressing enter/return after each line):

~~~
$ cd
$ git clone https://github.com/Southampton-RSG-Training/shell-novice.git
~~~
{: .language-bash}

`cd` will move to your home directory, and `git clone` will download a copy of the materials.

This should download all the content for the lesson to a new directory.
Please let the instructors know if you run into any problems.

{% include links.md %}

# Version Control with Git

# Building Programs with Python

## Python Setup ##

The “Anaconda3” package provides everything Python-related you will need for the workshop. 
To install [Anaconda](https://www.anaconda.com/products/individual), follow the instructions below.

Some old research projects may be in Python 2 but Python 2 has been retired and new projects should be in Python 3.

### Windows
Download the latest Anaconda Windows installer. Double-click the installer and follow the instructions. **When asked “Add Anaconda to my PATH environment variable”, answer “yes”. It will warn you not to, but it's required for it to be found by git bash** After it’s finished, close and reopen any open terminals to reload the updated PATH and allow the installed Python to be found.

Once the Anaconda installation is finished you will be asked if you want the installer to initialize Anaconda3 by
running conda init? You should select yes. Alternatively/additionally you will need to run the following command in 
GitBash

{: .bash}
~~~
conda init bash
~~~

Then close and reopen GitBash.

Please test the python install open GitBash (or your favorite terminal) and run the following command to verify that the installation was successful.

{: .bash}
~~~
cd ~
python
~~~

You can then type the following to exit:
{: .python}
~~~
quit()
~~~

{: .callout}
~~~
In some cases GitBash will hang on this command and not launch the Python interpreter. 
In this case close and reopen git bash and issue the following commands:
~~~

{: .bash}
~~~
cd ~
echo 'alias python="winpty python.exe"' >> ~/.bash_profile
source .bash_profile
python
~~~

Note that for older versions of git bash you will need to use `.bashrc` rather than `.bash_profile`


### Mac OS X

#### Mac OS Intel
Download the latest Anaconda Mac OS X installer. Double-click the .pkg file and follow the instructions.

#### Mac OS M1
If you have a M1 Mac you need a specific version of Anaconda follow the link below. 

[M1 Compatible Anaconda](https://repo.anaconda.com/archive/Anaconda3-2022.05-MacOSX-arm64.pkg)

Once the Anaconda installation is finished you will be asked if you want the installer to initialize Anaconda3 by
running conda init? You should select yes.

### Linux
Download the latest Anaconda Linux Installer.

Install via the terminal like this (you will need to change the version number to the latest version):

First move to the folder where you downloaded the installer, this is likely to be the Downloads folder e.g.

~~~
$ cd ~/Downloads
~~~
{: .language-bash}

~~~
$ bash Anaconda3-2021.11-Linux-x86_64.sh
~~~
{: .language-bash}

Answer ‘yes’ to allow the installer to initialize Anaconda3 in your .bashrc.

## Download Data for Python Lesson ##

Now we are ready to download the code that we need for this lesson. Open a terminal on your machine, and enter:
~~~
$ cd
$ git clone https://github.com/Southampton-RSG-Training/python-novice
~~~
{: .language-bash}

`cd` will move to your home directory, and `git clone` will download a copy of the materials.

{% include links.md %}

# Managing Academic Software Development

## Project Demo Repository

We'll be showing you how to manage an example academic software project. 
If you've completed our **Version Control with git** workshop, you'll have a finished version of our `climate-analysis` repository ([you'll have used the template from here](https://github.com/Southampton-RSG-Training/git-novice-template/))
If not, please [create a copy of it from this template (linked here)](https://github.com/Southampton-RSG-Training/project-novice-template/generate), and name it `climate-analysis`.


## Install Visual Studio Code

This workshop involves editing code files. 
Whilst you can use any text editor to do this, some code editors or Integrated Development Environments (IDEs) have features designed to make coding easier.
If you're already using a code editor or IDE (e.g. [Atom](https://atom.io/), [Sublime Text](https://www.sublimetext.com/) or [Spyder](https://www.spyder-ide.org/)), 
stick with what you're comfortable with. If not, we'd recommend installing [Visual Studio Code (link here)](https://code.visualstudio.com/).

### Windows / MacOS
Go to [the Visual Studio Code website](https://code.visualstudio.com/), and download and run the installer.

### Linux
If you're on **Ubuntu**, Visual Studio Code should be available through the software centre! 
If not, [follow the detailed instructions here](https://code.visualstudio.com/docs/setup/linux) to install it.