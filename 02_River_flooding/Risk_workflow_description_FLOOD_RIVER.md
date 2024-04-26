Risk assessment for river flooding
=======================

## Risk assessment methodology

In this workflow we will consider the potential impacts of river flooding. The flood risk is calculated by combining maps of potential river flood extent with exposure and vulnerability data in the form of economic damage functions for infrastructure. 
In particular, flood damage is calculated by applying damage curves to the flood inundation depth maps, taking into account the local situation. For each grid point, the damage is calculated based on the flood depth, land use type, damage curves, and country-specific parameters (can be defined by the user) that approximate the economic value of different land use types.
The resulting data and maps help the user to assess the hotspots of potential economic damage due to river flooding for different return periods of high river flows.

**Attention:** The hazard (flood maps) data is pre-processed using the dedicated hazard assessment script. If you would like to use the provided hazard data and have not yet retrieved the necessary data using that script, please do so before using this risk assessment script (see *Hazard_assessment_FLOOD_RIVER.ipynb*).

Please note that the underlying flood map dataset does not include river flood defences that may already be in place. It is important to always check the result against existing local knowledge of the infrastructure. More information on the applicability of the dataset is found below.

## Datasets

The following datasets are used in this workflow:

- Flood maps: river flood extent and water depth: available from the  [Joint Research Centre](https://data.jrc.ec.europa.eu/dataset/1d128b6c-a4ee-4858-9e34-6210707f3c81) for different return periods. The flood maps come at a resolution of 3 arc-seconds (30-75m in Europe depending on latitude). Additionally we use coarse-resolution flood maps (30 arc-seconds resolution) from [Aqueduct Flood Hazard Maps dataset](https://www.wri.org/data/aqueduct-floods-hazard-maps) to assess qualitatively the change in river flood hazard under climate scenarios.  
- Land-use information: The land cover map is available from the [Copernicus Land Monitoring Service](https://land.copernicus.eu/pan-european/corine-land-cover).
- Damage curves for infrastructure expressed as relative damage percentage (available [here](https://publications.jrc.ec.europa.eu/repository/handle/JRC105688)).
- Data on economic value for different types of land use, which can be country/location specific. This data is specified in the Excel file provided on the GitHub repository of the workflow (see **LUISA_damage_info_curves_template.xlsx**)

`````{admonition} JRC's high-resolution flood maps - dataset of present-day river flood potential and its applicability for local hazard assessment
:class: hint dropdown
The methodology behind this dataset is documented and can be accessed through this ([article](https://doi.org/10.5194/essd-14-1549-2022)). We will use the most recently updated version of the dataset (v3) that became available in March 2024. 

Important to take into account when interpreting the flood maps:
 - This dataset helps to understand the **river flood potential** at a given location. The flood modelling in this dataset does not account for man-made protections that may already be in place in populated regions (e.g. dams, levees, dykes). Therefore, it is always important to survey the local circumstances when interpreting the flood maps.

For a more accurate estimate of river flood risks, it is recommended to perform local flood modelling, taking the results of the global model as boundary conditions. Local models can take better account of complex topography, and incorporate local data and knowledge about e.g. flood protection measures.
`````

`````{admonition} Aqueduct Floods coarse-resolution flood maps - dataset of **future** river flood potential under climate change
:class: hint dropdown
The methodology behind this dataset is available in the corresponding [technical note](https://www.wri.org/research/aqueduct-floods-methodology).

This is a global dataset which on a local scale may lead to considerable uncertainty in the results. Please keep the following in mind when interpreting the data from this dataset:
-	The flood maps provide a first indicative estimate and should be interpreted with care.
-	Results of all scenarios and all models should be consulted before drawing any conclusions on the potential future changes in flood depth.
-	The underlying hydrological model and flood mapping method have a relatively coarse resolution and thus only include local characteristics up to this level of detail. Water management, weirs and sluices are not included in the model.
-	The analysis is based on time-series of limited length and thus extreme value analysis is also based on limited number of annual maxima and quite uncertain.
`````

## Output of the workflow

The outputs of this workflow are:  
 - Potential flood depth and extent maps for the area of interest for extreme events with different return periods.
 - Potential flood damage maps, expressed in economic value, for extreme events with different return periods.
 

