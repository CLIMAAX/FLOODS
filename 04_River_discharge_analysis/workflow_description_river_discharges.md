# Hazard assessment for river flooding using river discharge statistics

This workflow uses the dataset of hydrological climate impact indicators by SMHI that is [available via the Copernicus Data Store](https://doi.org/10.24381/cds.73237ad6). Based on this dataset, we can assess the projected changes in river discharges due to climate change, modelled using a European-wide hydrological model forced with climate models.

The dataset contains two types of model data: gridded data (E-HYPEgrid model) and catchment-level data (E-HYPEcatch model). In this workflow we will only use the catchment-level model data. The resolution of the catchment-level data is approx. 0.11 degrees (5-10 km).

The following variables are used in this workflow:
- daily timeseries of river discharges for a historical period in order to assess the variation in discharge and compare to local observations.
- monthly means of catchment-level river discharges to assess the seasonal changes in river discharges in the historical and future climates.
- extreme river discharges for different return periods and their relative changes for different climate models, climate scenarios and timeframes (early-, mid- and end-century) to assess potential changes in flood hazard.

Relative change of extreme river discharges is available for 2, 5, 10, 50-year return periods and for the following timelines:
- early century (2011-2040)
- mid-century (2041-2070)
- end-century (2071-2100)

For each time period, climate scenarios RCP2.6, RCP4.5 and RCP8.5 are available. Relative increases in flood recurrence for these periods are expressed relative to the reference period (1971-2000).

## Structure of the workflow

1. [Accessing data](./hazard_assessment_get_data.ipynb)
2. [Hazard assessment using river discharge statistics](./hazard_assessment_discharge_analysis.ipynb)
3. [Validation with observations](./hazard_assessment_compare_to_observations_GRDC.ipynb)

:::{note}
This workflow currently assesses hazard only.
:::


## Author

Natalia Aleksandrova (Deltares)
