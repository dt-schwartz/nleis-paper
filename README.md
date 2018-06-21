### Code and analysis for "Nonlinear electrochemical impedance spectroscopy of lithium-ion batteries: Experimental approach, analysis, and initial findings"
------------------------------------------------------------------------------------------------------

[This repository](https://github.com/mdmurbach/nleis-battery-manuscript) contains all of the data, code, and figures, used in the manuscript. To refer to the code or analysis, please use the ECSarXiv DOI:

**Please cite the following paper if you use this code:**

[M. D. Murbach\*, V. W. Hu\*, and D. T. Schwartz. Nonlinear electrochemical impedance spectroscopy of lithium-ion batteries: Experimental approach, analysis, and initial findings]()

---------------------------
#### Software dependencies
---------------------------

The code in this repository has been tested with the following versions of software:

- Python 3.6.3 [https://www.python.org/](https://www.python.org/)
- Conda 4.3.30 (through Miniconda 3) [https://conda.io/miniconda.html](https://conda.io/miniconda.html)
- Git Bash on Windows

The environment.yml file can be used to recreate the same Conda environment with the following commands:

`conda env create -f environment.yml`

`source activate nleis-manuscript`

-------------------------
#### Repository Structure
-------------------------

**comsol:**  This folder contains the COMSOL model used to simulate the linear EIS and second harmonic NLEIS spectra of a lithium-ion battery using the pseudo-two-dimensional (P2D) model.

**data:** This folder will need to be added once the repository has been cloned (see below). For minimal changes to the supplementary notebook, put all data downloaded through the OSF page here.

**figures:**  This folder is where the figures generated by the Python code are located.

**jupyter:**  This folder contains the Jupyter notebook (Supplementary Notebook.ipynb) and utility module that are used to compile the dataset, perform any analysis, and generate the manuscript figures.

**matlab:**  This folder contains the MATLAB .m files for running the COMSOL model using LiveLink for MATLAB.

**supplementary-files:** This folder contains the input files required for reproducing the simulations found in the manuscript.

----------
#### Data
----------

All of the data files are stored with OSF Projects: https://osf.io/4a6g9/

The data directory is organized into experimental data (`/raw`) and simulation data (`/simulation`). The raw experimental data is further organized by:

- `/new`: contains the the data files and the corresponding Kramers-Kronig validation for the EIS/NLEIS experiments done on three fresh LiNMC|C cells. Each cell subdirectory has experimental data for 10, 30, 40, 50, and 60% state of charge and the open-circuit potentials the experiments were done at.
- `/aged`: contains the the data files and the corresponding Kramers-Kronig validation for the EIS/NLEIS experiments done on three LiNMC|C cells that were aged for 100 cycles at 2C. Each cell subdirectory has experimental data for 10, 30, 40, 50, and 60% state of charge and the open-circuit potentials the experiments were done at.
- `resistor`: contains the data files for the EIS/NLEIS experiment done of the purely resistive wire to determine the instrument offset

To reproduce the figures: Clone the repository and then download/unzip the folder from the [OSF Project](https://osf.io/4a6g9/) into the main repository directory.
