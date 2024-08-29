# FLOODS

Repository for collaboration on workflows for floods hazard.

[<img src="https://raw.githubusercontent.com/CLIMAAX/crabook/main/crabook/logo.png" height="100" />](https://climaax.eu)

Part of the [Climate Risk Assessment Handbook](https://handbook.climaax.eu/notebooks/workflows/floods.html).


## Workflows

- [River flood](02_River_flooding/)
- [Coastal flood](01_Coastal_flooding/)

Both workflows enable the user to retrieve relevant flood maps from open global databases and combine those with data on exposure and vulnerability in the form of land use maps and economic damage curves.

- [Flood building damage and population exposure](03_Flood_damage_and_population_exposure/)


## How to run

See our [how to run risk workflows](https://handbook.climaax.eu/notebooks/workflows_how_to.html) page in the handbook for more information.

### Launch a binder session

Binder sessions are not persistent and may not provide the necessary computing resources to run all workflow steps.
In particular, the workflows cannot be used on Binder to load multiple flood maps or perform all of the calculations in an efficient manner.

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/climaax/binder-env/main?urlpath=git-pull%3Frepo%3Dhttps%253A%252F%252Fgithub.com%252FCLIMAAX%252FFLOODS%26urlpath%3Dlab%252Ftree%252FFLOODS%252F%26branch%3Dmain)

### Quickstart: local setup

In a terminal where git and conda are available:

1.  Clone the repository

        git clone git@github.com:CLIMAAX/FLOODS.git

2.  Move into the cloned repository

        cd FLOODS

3.  Create a new environment from the `environment.yml` file

        conda env create -f environment.yml

4.  Activate the environment

        conda activate climaax_floods

5.  Launch the Jupyter interface of your preference with

        jupyter lab

    or

        jupyter notebook


## How to contribute

See our [contribute to risk recipes](https://handbook.climaax.eu/community/contribute.html) page in the handbook for more information.
