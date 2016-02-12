# Working locally

During the sessions, we have been working in the cloud. However, you might want to run jupyter notebooks locally. This instructions will guide you to get them running in your computer.

You will need `python3`, `jupyter` and some additional python packages. If you try to use `python2` and the old `ipython` unexpected things will happen.

We will show you how to:

- get python 3 installed
- how to use virtual environments
- how to install python packages
- which packages you will need to run the notebooks of the WwC python sessions
- how to work with jupyter notebooks

The instructions have been tested for Mac OS X 10.11 El Capitan, Ubuntu 15.10 Wily Werewolf, and Windows 7.

We will provide instructions to set up your environment:

- easy
- advanced

*Easy* is aimed at getting Python 3 and all necessary packages installed with a minimum effort. This option is good for you if disk space is not a problem, you have a good internet connection, and a few minutes.

*Advanced* is a a bit more involved and it is aimed at those who just want to install the minimum requirements. This is mostly command-line based. And for those how know what they are doing ;-)

## Easy

The easiest cross-platform solution is to use [`Anaconda`](https://www.continuum.io). `Anaconda` is a Python distribution and package manager maintained by a company, *Continuum*.

`conda` comes with very complete [documentation](http://conda.pydata.org/docs). We will follow their materials.

### Install `conda`

Follow the appropriate instructions for your operating system <http://conda.pydata.org/docs/install/full.html>.

### Get the notebooks

You can get them from GitHub. If you want to get detailed instructions, take a look at `using-git.md`.

1. Fork interrogator/wwc
1. Clone yourgithub/wwc

### Run the notebooks

#### Windows

#### Mac

You will see on your Desktop an icon called `Launcher`, if you don't just go to the folder where `conda` is installed `~/ananconda`, you will see the `Launcher` there.

1. Double click on `Launcher`
1. Click on `ipython-notebook`'s `Launch` button.

Two things will happen:

1. a terminal window opens
1. a new browser tab opens

Keep open the terminal window, this is running a server locally. Close it when you are done working with the notebooks. Otherwise you want be able to run the notebooks.

The browser tab displays the contents of your home folder. Navigate to the folder where you have cloned `wwc`. Click on any notebook you want to use. When you are done, shut down the notebook, and, in the terminal window type `Control-C`, confirm by typing `y` and press `Enter`.

#### Linux

### Try `conda`

If you want to learn more about `conda` and test that everything is working, you might be interested in `conda`'s [test drive](http://conda.pydata.org/docs/test-drive.html).

## Advanced

For the advanced we have to paths to follow:

- `conda`, if you use Windows, or if you want to stick to `conda` in any other operating system
- `official`, if you use Mac/Linux, or you don't want to use `conda`

### The `conda` way

#### Windows

#### Mac

##### Installing Python 3

Read and follow the [instructions](http://conda.pydata.org/docs/install/quick.html#os-x-miniconda-install):

1. Download the appropriate version for your operating system <https://repo.continuum.io/miniconda/Miniconda3-latest-MacOSX-x86_64.sh>
1. Change to the directory where you download it `cd ~/Downloads`
1. Run the: `bash Miniconda3-latest-MacOSX-x86_64.sh`
1. Follow the instructions on screen
1. Source the `source ~/.bash_profile`

Now, your default Python in Mac is conda's Python 3.

#### Linux

### The *official* way

#### Mac

##### Installing Python 3 with homebrew

Mac OS X comes with a python 2 distribution preinstalled. You still will need python 3. We will use in this tutorial the software manager `homebrew` <http://brew.sh>.

1. install Command Line Tools for Xcode
```shell
xcode-select --install
```
1. install homebrew
```shell
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
1. install python3
```shell
brew install python3
```
1. linkapps
```shell
brew linkapps python3
```
1. install yolk to keep track of your python packages (optional)
```shell
pip3 install yolk
```

Now, you check again if python 3 is installed by running:

```shell
python3 --version
```

You should see `Python 3.5.1`.

#####

#### Linux

##### Installing Python 3

Congratulations! Latest Ubuntu's releases come with Python 3.4 out of the box. The version can be a bit behind the latest official python 3 (3.5) release. But the notebooks should work anyway. You need to install `pip`, the python package manager.

#### Python 3

The first question we need to answer is:

> Do I have python 3?

You can open a Terminal or Console and type the following command:

```shell
python3 --version
```

If you get something like `Python 3.5.0`, congratulations! You have python 3 installed in your computer. However, if you get `python3: command not found`, either you don't have python 3 or your OS cannot find it.

If you DO have python 3 already installed in your machine, check the version you have. If the version is >= than 3.4. proceed to section [Python virtual environments](#python-virtual-environments), otherwise, you will need to install pip, go to section [Installing pip](#installing-pip). If you DO NOT have python 3 installed in your computer follow the instructions in section [Installing python 3](#installing-python-3).


#### Installing Python 3

Depending on the platform you are working, you will need to follow a different procedure:

- [Mac OS X](#installing-python-3-for-mac-os-x)
- [Ubuntu](#installing-python-3-for-ubuntu)

### Installing python 3 for Mac OS X

#### Installing python 3 with homebrew

Mac OS X comes with a python 2 distribution preinstalled. You still will need python 3. We will use in this tutorial the software manager `homebrew` <http://brew.sh>.

1. install Command Line Tools for Xcode
```shell
xcode-select --install
```
1. install homebrew
```shell
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
1. install python3
```shell
brew install python3
```
1. linkapps
```shell
brew linkapps python3
```
1. install yolk to keep track of your python packages (optional)
```shell
pip3 install yolk
```

Now, you check again if python 3 is installed by running:

```shell
python3 --version
```

You should see `Python 3.5.0`.

If you were successful go to section [Python virtual environments](#python-virtual-environments).





### Installing python 3 for Ubuntu

Congratulations! Latest Ubuntu's releases come with Python 3.4 out of the box. The version can be a bit behind the latest official python 3 (3.5) release. But the notebooks should work anyway. You need to install `pip`, the python package manager.

Go to [Installing pip](#installing-pip).

## Installing pip

Check if you already have `pip3` installed running the command below:

```shell
pip3 --version
```

If you DO have `pip3` installed go to section [Python virtual environments](#python-virtual-environments).
If you DO NOT have `pip3` follow this instructions: <http://pip.de>

### Installing pip for Ubuntu

Open a terminal and type:

```shell
sudo apt-get install python3-pip
```

Check again if you already have `pip3` installed running the command below:

```shell
pip3 --version
```

### Installing pip for Windows

If you followed the instructions to install python 3, you don't need to install pip. The latest versions come with pip already.

### Updating pip

#### UNIX

You might need to update `pip`:

```shell
pip3 list
```

If you read something like you could upgrade pip, run:

```shell
python -m pip3 install --upgrade pip
```

#### Windows

You might need to update `pip`:

```shell
pip list
```

If you read something like you could upgrade pip, run:

```shell
python -m pip install --upgrade pip
```

## Python virtual environments

We recommend you to work with python virtual environments. If you don't want to use virtual environments go to section [Installing python packages](#installing-python-packages), just remember to use `pip3` command instead of just `pip`.

**What are virtual environments?** Virtual environments are python setups that you can manage in an isolated way and keep independent from your system python installation. If you have installed the latest python 3 following the instructions above, or you have python 3 >= 3.5, you will have `pip` installed too. Otherwise, install `pip` as explained in section [Installing pip](#installing-pip).

Advantages:

- keep track of the dependencies of each project (packages and versions)
- reproducible research
- switch python versions
- test scripts for different python versions
- write code for an environment similar to the deployment

At the beginning, it might seem complicated. At the end, you will appreciate it.

### Installing virtual environments

<!-- this commands work for mac and lin -->

#### UNIX

1. install `virtualenv`
```shell
pip3 install virtualenv
```
1. install `virtualenvwrapper` (to ease `virtualenv` mangagement)
```shell
pip3 install virtualenvwrapper
```

#### Windows
1. install `virtualenv`
```shell
pip install virtualenv
```
1. install `virtualenvwrapper` (to ease `virtualenv` mangagement)
```shell
pip install virtualenvwrapper-win
```

The next step is to set up `virtualenv` and `virtualenvwrapper`.

### Setting up virtualenv and virtualenvwrapper

#### Setting up virtualenv and virtualenvwrapper for Mac OS X

This piece of code has to be added to `~/.bash_profile`.

```shell
# set where virtual environments will live
export WORKON_HOME=$HOME/.virtualenvs
# set where the location of development project directories
export PROJECT_HOME=$HOME/Devel
# ensure all new environments are isolated from the site-packages directory
export VIRTUALENVWRAPPER_VIRTUALENV_ARGS='--no-site-packages'
# use the same directory for virtualenvs as virtualenvwrapper
export PIP_VIRTUALENV_BASE=$WORKON_HOME
# makes pip detect an active virtualenv and install to it
export PIP_RESPECT_VIRTUALENV=true
if [[ -r /usr/local/bin/virtualenvwrapper.sh ]]; then
        source /usr/local/bin/virtualenvwrapper.sh
else
        echo "WARNING: Can't find virtualenvwrapper.sh"
fi
```

#### Setting up virtualenv and virtualenvwrapper for Ubuntu

Open a terminal window, and run the following commands:

```shell
sudo apt-get install virtualenv
sudo apt-get install virtualenvwrapper
source .bashrc
```

#### Setting up virtualenv and virtualenvwrapper for Windows

Good news! You don't need to set up anything.

### Working with virtual environments

We will show you how to set up a virtual environment for WwC python sessions.

#### Create a new virtual environment in Mac/Linux

You only have to this once.

```shell
mkvirtualenv --python=python3 wwc
```

#### Create a new virtual environment in Windows

```shell
mkvirtualenv.bat wwc
```

#### Work on the new virtual environment

Whenever you want to work in a particular virtual environment, you have to activate it like this:

```shell
workon wwc
```

#### Stop working on the virtual environment

Once you are finished, or you want to switch to another virtual environment you can deactivate it:

```shell
deactivate wwc
```

## Python packages

**NOTE**: if you are working **with virtual environments** or **with Windows** you just need to type `python` or `pip`. If you are working **in Mac/Linux**, and you are not using **virtual environments** you will need to use `python3` and `pip3` instead.

### Installing python packages for Mac OS X


You will need to install some packages in your `wwc` environment before you can use our notebooks.

Be sure you are working in the appropriate virtual environment:

```shell
workon wwc
```

If you prefer not to work with virtual environments just follow the instructions below.

Packages installed in a virtual environment

```shell
pip freeze
```

You will need to install the packages listed in `wwc-dependencies.txt`. Namely:

- jupyter
- pandas
- nltk
- numpy
- matplotlib

...

#### jupyter

`jupyter` is a package enabling the usage of jupyter notebooks and `ipython`.

Type in the terminal:

```shell
pip install jupyter
```

This procedure will install `jupyter` and many other packages which are dependencies. That's just fine.

#### nltk

```shell
pip install nltk
```

#### matplotlib

```shell
pip install matplotlib
```

#### pandas

```shell
pip install pandas
```

#### numpy

```shell
pip install numpy
```

### Installing python packages for Ubuntu

### Installing python packages for Windows


## Working with jupyter notebooks

We will learn in this session how to:

1. start jupyter,
1. open/create a notebook, and
1. close the notebooks and jupyter.

### Start jupyter

Run the following command in the Terminal (Mac/Linux) or Command Prompt (Windows):

```shell
jupyter notebook
```

Two things will happen:

1. you will see some text in your terminal
1. a new tab will be open in your web browser

You should not close the Terminal/Command Prompt window until you are finished.

The new tab shows a page that should be familiar to you. You can:

1. open an existing notebook
1. create a new empty notebook

### Open a notebook

Browse in the `Files` tab until you find the notebook you want to open. Click on it, and *voilà*!

### Create a new notebook

Click on the right upper button called `New`, and then choose `Notebooks Python 3`.

Click on the title and name it as you want. Or:

File -> Rename...

### Close a notebook

File -> Save and Checkpoint

File -> Close and Halt

### Stop jupyter

To stop jupyter, go to the terminal where you started it. Type twice `Control-C` to stop the server and shut down all kernels.
