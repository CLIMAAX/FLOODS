# # Risk assessment for coastal flooding



## Risk assessment methodology

In this workflow we will consider the potential impacts of coastal flooding caused by extreme sea water levels. The flood risk is calculated based on maps of potential coastal flood extent that are combined with two types of exposure and vulnerability data:  
 - Economic damage functions for infrastructure to map out potential damages.
 - Maps of critical infrastructure to locate the infrastructure at risk.

The resulting data and maps help the user to assess the hotspots of potential economic damage due to coastal flooding for different return periods of extreme sea levels, and to view which critical infrastructure is most likely to be affected.

Please note that the underlying flood map dataset does not include coastal flood defences that may already be in place. It is important to always check the result against existing local knowledge of the infrastructure. More information on the applicability of the dataset is found below.

## Datasets

The following datasets are used in this workflow:

- Flood maps: the maps of flood depth (coastal inundation depth) are based on the Global Flood Maps dataset openly available via the Microsoft Planetary Computer ([source](https://planetarycomputer.microsoft.com/dataset/deltares-floods)). 
- Land-use information: The land cover map is available from the [Copernicus Land Monitoring Service](https://land.copernicus.eu/pan-european/corine-land-cover).
- Damage curves for infrastructure expressed as relative damage percentage (available [here](https://publications.jrc.ec.europa.eu/repository/handle/JRC105688)).
- Data on economic value for different types of land use, which can be country/location specific. This data is specified in the Excel file provided on the GitHub repository of the workflow (see **LUISA_damage_info_curves.xlsx**)
- Maps of critical infrastructure obtained from [OpenStreetMap](https://www.openstreetmap.org).

In this workflow we use the postprocessed version of the Global Flood Maps dataset that is downloaded using the dedicated hazard assessment workflow, where the flood maps were downloaded and aggregated for the specific area of interest (**link**). If you would like to use this dataset, please first execute the coastal flood hazard assessment workflow to download the flood maps.

## Output of the workflow

The outputs of this workflow are:  
 - Flood damage maps per scenario and return period.
 - Flood depth and extent maps overlay with critical infrastructure.

Flood damage is calculated by applying damage curves to the flood inundation depth maps, taking into account the local situation. For each grid point, the damage is calculated based on the flood depth, land use type, damage curves, and country-specific parameters (can be defined by the user) that approximate the economic value of different land use types.

The flood maps are considered for two climates: present day climate (ca. 2018) and 2050 (RCP8.5 climate scenario). For each climate, different return periods of the extreme conditions are considered.

`````{admonition} Global Flood Maps dataset and its applicability for local risk assessment
:class: hint dropdown
The Global Flood Maps dataset was developed by Deltares based on global modelling of water levels that are affected by tides, storm surges and sea level rise. In this dataset, maps for present climate (ca. 2018) and future climate (ca. 2050) are available, with extreme water levels corresponding to return periods of 2, 5, 10, 25, 50, 100 and 250 years. The 2050 scenario assumes sea level rise as estimated under RCP8.5 (high-emission scenario). The flood maps have a resolution of 3 arcseconds.

The methodology behind this dataset is documented and can be accessed on the ([data portal](https://planetarycomputer.microsoft.com/dataset/deltares-floods)). The dataset is based on the GTSMv3.0 (Global Tide and Surge model), forced with ERA5 reanalysis atmospheric dataset. Statistical analysis of modelled data is used to arrive at extreme water level values for different return periods. These values are used to calculate flood depths by applying static inundation modelling routine ("bathtub" method, with a simplified correction for friction over land) over a high-resolution Digital Elevation Model (MERIT-DEM or NASADEM). 

Several things to take into account when interpreting the flood maps:
 - This dataset helps to understand the **coastal flood potential** at a given location. The flood modelling in this dataset does not account for man-made coastal protections that may already be in place in populated regions (e.g. dams, storm barriers). Therefore, it is always important to survey the local circumstances when interpreting the flood maps.
 - The resolution of this global dataset is very high, when considered on a global scale. However, for local areas with complex bathymetries the performance of the models is likely reduced (e.g. in estuaries or semi-enclosed bays) and the results should be treated with caution.
 - The dataset is based on`m a static topography. In some coastal areas flood risk may be increased by land subsidence. If this is a known issue in the area of interest, it should be taken into account when interpreting the coastal flood maps.

For a more accurate estimate of coastal flood risks, it is recommended to perform local flood modelling, taking the results of the global model as boundary conditions. Local models can take better account of complex bathymetry and topography, and incorporate local data and knowledge about e.g. flood protection measures.
`````

`````{admonition} Using your own hazard or exposure data
:class: hint dropdown
TODO
`````

