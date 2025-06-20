# CAS-ILHB: Transverse Beam Dynamics
> Transverse beam dynamics Hands-on exercises for 2025's CAS on Intensity Limitations in Hadron Beams 

## Content of the Hands-on

[TODO]

## Installation guide

To run this python notebook examples, we will need to install:

### Python 3.11

This can be easily done through `conda-forge`'s Miniforge downloading the executable:
🔗 https://conda-forge.org/download/ 

or from the terminal (Ubuntu/MACos):
```bash
# get, install and activate miniforge
wget "https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-$(uname)-$(uname -m).sh"
bash Miniforge3-$(uname)-$(uname -m).sh
conda activate
```
It is highly recommended to create a dedicated `python environment` to start with a clean installation:
```
# create dev python environment
conda create --name xsuite python=3.11
conda activate xsuite
conda install -c conda-forge compilers # to run on CPU
```

If you are using Windows, we recommend installing [WSL Windows Subsystem for Linux](https://learn.microsoft.com/en-us/windows/wsl/install) and then proceed with the Miniforge install. Alternatively, the notebooks can be opened on CERN's [SWAN](https://swan.web.cern.ch/swan/) or Google collab (not-tested).

### Xsuite
  
[Xsuite](https://xsuite.readthedocs.io/en/latest/) is a collection python packages developed at CERN for the simulation of the beam dynamics in particle accelerators. It supports different computing platforms, in particular conventional CPUs and and Graphic Processing Units (GPUs). It can be easily installed by:
```
pip install xsuite xwakes
```

If you're running the [notebooks on SWAN](https://swan.web.cern.ch/), we recommend choosing a configuration with 4cores/16Gb and make sure to activate the ☑️`Use Python packages installed on CERNBox` checkbox.

Then, you can import the repository clicking on the ☁️ symbol and pasting the GIT repository url: 

```
https://github.com/elenafuengar/CAS-ILHB_Transverse-Beam-Dynamics.git
```
Make sure to download it in the **root directory** and not inside an existing folder to avoid issues!

Then, add at the top of the `001` notebook the following lines in a dedicated cell to perform the installation of Xsuite on your user's CERNBox:
```
! pip install --user xsuite xwakes
! export PATH=$PATH:/eos/user/${USER::1}/$USER/.local/bin
```

### Jupyter notebooks
To run python notebooks `.ipynb` from your chosen IDE (e.g. Visual Studio) or from JupyterLab, we need to install `Jupyter notebook` and interactive widgets by doing:
```
pip install jupyter ipympl 
```

### Matplotlib and other support packages
For plotting, reading files and handling dataframes, we will need the following packages:
```
pip install matplotlib pandas h5py
```

That's all! Enjoy playing with the notebook tutorials 😊🚀
  
