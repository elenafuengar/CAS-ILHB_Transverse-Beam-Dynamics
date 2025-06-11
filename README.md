# CAS-ILHB: Transverse Beam Dynamics
> Transverse beam dynamics Hands-on exercises for 2025's CAS on Intensity Limitations in Hadron Beams 

## Content of the Hands-on

[TODO]

## Installation guide

To run this python notebook examples, we will need to install:

### Python 3.11

This can be easily done through `conda-forge`:
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
```

### Xsuite
  
[Xsuite](https://xsuite.readthedocs.io/en/latest/) is a collection python packages developed at CERN for the simulation of the beam dynamics in particle accelerators. It supports different computing platforms, in particular conventional CPUs and and Graphic Processing Units (GPUs). It can be easily installed by:
```
pip install xsuite xwakes
```

### Jupyter notebookS
To run python notebooks `.ipynb`, we need to install `Jupyter notebook` by doing:
```
pip install jupyter ipympl 
```

### Matplotlib and other support packages
For plotting, reading files and handling dataframes, we will need the following packages:
```
pip install matplotlib pandas h5py
```

That's all! Enjoy playing with the notebook tutorials 😊🚀
  
