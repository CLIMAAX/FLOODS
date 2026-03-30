# FLOODS

Repository for collaboration on workflows for floods hazard.

[<img src="https://raw.githubusercontent.com/CLIMAAX/crabook/main/crabook/logo.png" height="100" />](https://climaax.eu)

Part of the [Climate Risk Assessment Handbook](https://handbook.climaax.eu/notebooks/workflows/floods.html).


## Workflows

- [River floods](02_River_flooding/) (flood maps)
- [Coastal floods](01_Coastal_flooding/) (flood maps)
- [Flood building damage and population exposure](03_Flood_damage_and_population_exposure/)
- [River floods](04_River_discharge_analysis/) (discharges)


## How to run

See our [how to run risk workflows](https://handbook.climaax.eu/notebooks/workflows_how_to.html) page in the handbook for more information.

### Launch a binder session

Binder sessions are not persistent and may not provide the necessary computing resources to run all workflow steps.
In particular, the workflows cannot be used on Binder to load multiple flood maps or perform all of the calculations in an efficient manner.

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/climaax/binder-env/main?urlpath=git-pull%3Frepo%3Dhttps%253A%252F%252Fgithub.com%252FCLIMAAX%252FFLOODS%26urlpath%3Dlab%252Ftree%252FFLOODS%252F%26branch%3Dmain)

### Local setup with conda

```bash
# Clone the workflow repository
git clone git@github.com:CLIMAAX/FLOODS.git
cd FLOODS

# Create a new environment and activate it
conda env create -f environment.yml

# Start the JupyterLab from within the created environment
conda activate climaax_floods
jupyter lab
```

## How to contribute

See our [contributions](https://handbook.climaax.eu/community/contribute.html) page in the Handbook.

## License

`Apache-2.0 OR CC-BY-4.0` ([SPDX license identifier](https://spdx.dev/learn/handling-license-info/)).

## Acknowledgements

CLIMAAX has received funding from the European Union’s Horizon Europe – the Framework Programme for Research and Innovation (2021-2027) under grant agreement No. 101093864.
