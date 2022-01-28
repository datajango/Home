# Home

Anthony Leotta GitHub Home Page

Notes, Tutorials, READMEs, Procedures, HowTos for C++ Python JavaScript SQL Docker NodeJS

## Contents

1. [How to create a Anaconda Python Environment](#how-to-create-a-anaconda-python-environment)
1. [What is the anaconda base environment.](#what-is-the-anaconda-base-environment)
1. [Setting the Python runtime in Visual Studio Code](#setting-the-python-runtime-in-visual-studio-code)


## How to create a Anaconda Python Environment
There are many ways to create a Python virtual environments, the advantage of using Anaconda is that you will not have to install a C compiler and build packages yourself.  Conda is stable and ahs few operational problems. (Note that install a C compiler on Windows using Visual Studio Code with also result in installing Python 2.7 and many other tools.)  If you want to get up and running ASAP, then Anaconda Python is a good choice.  There are other ways to manage packages and environments such as Poetry and PyEnv whic I will cover in other procedures.

1. Install Anaconda on Windows
    1. Follow this [Installing on Windows](https://docs.anaconda.com/anaconda/install/windows/)

1. Create a fresh Anaconda virtual wnvironment

```
conda create --name myenv python=3.9
```

1. To activate the environment

```
conda activate myenv
```

1. To deactivate the environment

```
conda deactivate
```

1. To install Python Packages into the environment

```
conda activate myenv
pip install -r requirements.txt
```

1. To remove the environment

If for some reason you need to remove the environment and start over.

```
conda env remove --name myenv
```

1. To list all the packages in a Python environment

```
conda list
```

## What is the anaconda base environment?

If you type ```conda activate``` you will be dropped into teh base anaconda environment. One way to find out about this environment is to type ```conda list``` which will display all the packages that are installed by default.  A freshly created Anaconda package will have a "base" installation of Python packages.   The packages about to be downloaded and installed by the default package plan are listed when a new anaconda environment is about to be created.

```
## Package Plan ##

  environment location: G:\ProgramData\Anaconda3\envs\myenv

  added / updated specs:
    - python=3.9


The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    certifi-2021.10.8          |   py39haa95532_2         152 KB
    openssl-1.1.1m             |       h2bbff1b_0         4.8 MB
    sqlite-3.37.0              |       h2bbff1b_0         785 KB
    wheel-0.37.1               |     pyhd3eb1b0_0          33 KB
    ------------------------------------------------------------
                                           Total:         5.8 MB

The following NEW packages will be INSTALLED:

  ca-certificates    pkgs/main/win-64::ca-certificates-2021.10.26-haa95532_2
  certifi            pkgs/main/win-64::certifi-2021.10.8-py39haa95532_2
  openssl            pkgs/main/win-64::openssl-1.1.1m-h2bbff1b_0
  pip                pkgs/main/win-64::pip-21.2.4-py39haa95532_0
  python             pkgs/main/win-64::python-3.9.7-h6244533_1
  setuptools         pkgs/main/win-64::setuptools-58.0.4-py39haa95532_0
  sqlite             pkgs/main/win-64::sqlite-3.37.0-h2bbff1b_0
  tzdata             pkgs/main/noarch::tzdata-2021e-hda174b7_0
  vc                 pkgs/main/win-64::vc-14.2-h21ff451_1
  vs2015_runtime     pkgs/main/win-64::vs2015_runtime-14.27.29016-h5e58377_2
  wheel              pkgs/main/noarch::wheel-0.37.1-pyhd3eb1b0_0
  wincertstore       pkgs/main/win-64::wincertstore-0.2-py39haa95532_2


Proceed ([y]/n)?
```

When looking at this list of package I see the "Hollywood A-List" of Python packages.  First, let's just ponder for 1 second why Python is loved.

Could it be #1 sqlite 3?

Yes, that's right.  It's Python the only language with its own built-in in-memory file-based SQL relational database.  Instantaneously create as many relational databases as you need.  Most applications only need one, by the way. The fact that Python applications can use a relational database without installing any additional software only adds to the many people love the Python programming language.

I think the main three packages are number one python, number two pip and number three setuptools.  The fact that a Python environment contains Python itself is the entire point of a virtual Python environment.  Only there is nothing "virtual" about it.  It's so not virtual that it in fact has it's own copy of the Python executable.  But the next two package say it all.  Number two is pip.

## Setting the Python runtime in Visual Studio Code

1. Create a folder called .vscode

1. add a file called settings.json if it does not already exist

1. activate your Python environment

1. do a which python to get the full path of your Pyrhoin executable

1.  Add the key value pair python.pythonPath to the settings.json file.

```
{
    "python.pythonPath": "/home/tonyl/anaconda3/envs/dev39/bin/python",
    "python.testing.unittestEnabled": false,
    "python.testing.pytestEnabled": true,
}

```