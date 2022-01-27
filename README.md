# Home

Anthony Leotta GitHub Home Page - Notes Tutorials READMEs Procedures HowTos : C++ Python JavaScript SQL Docker NodeJS

## Procedures

1. [How to create a Anaconda Python Environment](##procedure-1.-how-to-create-a-anaconda-python-environment)

### Procedure 1. How to create a Anaconda Python Environment
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