# CAS-ILHB: Transverse Beam Dynamics
> Transverse beam dynamics Hands-on exercises for 2025's CAS on Intensity Limitations in Hadron Beams 

## Content of the Hands-on

In the hands-on we will study the impedance of the LHC unshielded bellows and their impact on the transverse beam dynamics if they were to be added to the LHC without shielding. The hands-on utilizes CST Studio for the Wakefield simulations, in parallel with the following python notebooks:

#### 001_xwakes_tmci_hllhc.ipynb

This notebook investigates the Transverse Mode Coupling Instability (TMCI) threshold for a single LHC bunch at injection energy using the LHC impedance model. Key steps include:

- Setting up LHC machine and bunch parameters.
- Importing and visualizing the LHC wake function.
- Performing intensity scans and tracking with Xsuite.
- Analyzing turn-by-turn transverse positions and tune spectra.
- Visualizing tune shifts and mode coupling as a function of intensity.
- Exploring intrabunch motion and its relation to headtail modes.

#### 002_xwakes_tmci_hllhc_with_bellows.ipynb

This notebook extends the previous study by including the effect of 1700 unshielded LHC bellows, modeled as a broadband resonator, in the impedance model. It covers:

- Adding a resonator wake to the wake used for tracking.
- Comparing beam dynamics with and without the bellows contribution.
- Repeating intensity scans and tracking.
- Assessing the impact on TMCI threshold and instability mitigation.
- Visualizing changes in intrabunch motion and discussing mitigation strategies (e.g., lowering the bellows impedance in CST, increasing chromaticity, using a transverse damper).
  
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

If you are using Windows, we recommend installing [WSL Windows Subsystem for Linux](https://learn.microsoft.com/en-us/windows/wsl/install) and then proceed with the Miniforge install. Alternatively, the notebooks can be opened on CERN's [SWAN](https://swan.web.cern.ch/swan/) or Google collab notebooks. 

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
  
