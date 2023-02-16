# Python virtual environments and dependency management

## Python environments using Conda

### Definition of conda environments
Conda environments have different versions of Python and/or packages installed in them. Switching or moving between environments is called activating the environment. You can also share an environment file.

[Manage envionments with conda](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html)

## Python native virtual environments 

### Definition of virtual environments
 Each virtual environment has its own Python binary (allowing creation of environments with various Python versions) and can have its own independent set of installed Python packages in its site directories, but shares the standard library with the base installed Python.

[Installing packages using pip and virtual environments](https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/#creating-a-virtual-environment)

[PEP 405 – Python Virtual Environments](https://peps.python.org/pep-0405/) 

``` cmd
python3 -m venv .venv-my-test

.venv-my-test\Scripts\activate

python -m pip install --upgrade pip

pip install numpy pandas

pip freeze

deactivate
```

## Python dependency management with PDM

Opt-in PEP 582 support, no virtualenv involved at all.
Simple and fast dependency resolver, mainly for large binary distributions.
A PEP 517 build backend.
PEP 621 project metadata.

[PDM](https://pdm.fming.dev/latest/)
[PEP 582 – Python local packages directory](https://peps.python.org/pep-0582/)

``` cmd
python3 -m venv .venv-my-test-pdm

.venv-my-test-pdm\Scripts\activate

python -m pip install --upgrade pip

pdm config

pdm init

pdm cache info

pdm add numpy pandas

pdm cache info

deactivate
```