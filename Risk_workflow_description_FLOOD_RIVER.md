# # Risk assessment for river flooding



## Risk assessment methodology

In this workflow we will consider the potential impacts of river flooding. The flood risk is calculated based on maps of potential river flood extent that are combined with exposure and vulnerability data in the form of economic damage functions for infrastructure. The resulting data and maps help the user to assess the hotspots of potential economic damage due to river flooding for different return periods of high river flows.

Please note that the underlying flood map dataset does not include river flood defences that may already be in place. It is important to always check the result against existing local knowledge of the infrastructure. More information on the applicability of the dataset is found below.

## Datasets

The following datasets are used in this workflow:

- Flood maps: iver flood extent and water depth: available from the  [Joint Research Centre](https://data.jrc.ec.europa.eu/dataset/1d128b6c-a4ee-4858-9e34-6210707f3c81) for different return periods. The flood maps come at a resolution of 100m. 
- Land-use information: The land cover map is available from the [Copernicus Land Monitoring Service](https://land.copernicus.eu/pan-european/corine-land-cover).
- Damage curves for infrastructure expressed as relative damage percentage (available [here](https://publications.jrc.ec.europa.eu/repository/handle/JRC105688)).
- Data on economic value for different types of land use, which can be country/location specific. This data is specified in the Excel file provided on the GitHub repository of the workflow (see **LUISA_damage_info_curves.xlsx**)

In this workflow we use the postprocessed version of the Global Flood Maps dataset that is downloaded using the dedicated hazard assessment workflow, where the flood maps were downloaded and aggregated for the specific area of interest (**link**). If you would like to use this dataset, please first execute the river flood hazard assessment workflow to download the flood maps.

## Output of the workflow

The outputs of this workflow are:  
 - Flood depth and extent maps for the area of interest.
 - Flood damage maps, expressed in economic value, return period.
 
Flood damage is calculated by applying damage curves to the flood inundation depth maps, taking into account the local situation. For each grid point, the damage is calculated based on the flood depth, land use type, damage curves, and country-specific parameters (can be defined by the user) that approximate the economic value of different land use types.
