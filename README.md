River flood workflow:
 - Hazard assessment for retrieving flood maps: [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/CLIMAAX/FLOODS/main?labpath=Hazard_assessment_FLOOD_RIVER.ipynb)
 - Risk assessment for mapping potential damage: [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/CLIMAAX/FLOODS/main?labpath=Risk_assessment_FLOOD_RIVER.ipynb)
   
Coastal flood workflow:  
 - Hazard assessment for retrieving flood maps: [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/CLIMAAX/FLOODS/main?labpath=Hazard_assessment_FLOOD_COASTAL.ipynb)
 - Risk assessment for mapping potential damage: [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/CLIMAAX/FLOODS/main?labpath=Risk_assessment_FLOOD_COASTAL.ipynb)

# FLOODS
Repository for collaboration on workflows for floods hazards, which contains two workflows:
 - river flood workflow
 - coastal flood workflow

Both workflows enable the user to retrieve relevant flood maps from open global databases and combine those with data on exposure and vulnerability in the form of land use maps and economic damage curves.

# How to run

## Running on Binder
The notebooks can be launched on Binder. However, please note that the available memory space on Binder is limited, which means that the workflow cannot be used to load multiple flood maps or perform all of the calculations in an efficient manner.
Click the **Launch Binder** button at the top level of the repository.

## Running locally
You can download the notebook from GitHub to run it locally:
1. Open your terminal

2. Check your conda install with `conda --version`. If you don't have conda, install it by following these instructions (see [here](https://docs.conda.io/en/latest/miniconda.html))

3. Clone the repository
    ```bash
    git clone https://github.com/CLIMAAX/FLOODS.git
    ```

4. Move into the cloned repository
    ```bash
    cd FLOODS
    ```

5. Create and activate your environment from the `environment.yml` file
    ```bash
    conda env create -f environment.yml
    conda activate climaax_floods
    ```  

6. Launch the jupyter interface of your preference, notebook, `jupyter notebook` or lab `jupyter lab`
   
8. Edit and run the notebook


# Credits
The **How to run** section was adapted from the [Environmental Data Science Book](https://edsbook.org/welcome.html) project.
