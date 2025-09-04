# Hazard assessment for river flooding using river discharge statistics

This workflow uses the dataset of hydrological climate impact indicators by SMHI that is [available via the Copernicus Data Store](https://doi.org/10.24381/cds.73237ad6).

The following variables are used in this workflow:

- daily timeseries of gridded river discharges in the historical period based on the E-HYPEgrid model.
- monthly means of gridded river discharges over a 30-year period (1971-2000) based on the E-HYPEgrid model.
- monthly means of catchment-level river discharges (in the period 1971-2000) based on the E-HYPEcatch multi-model ensemble.
- extreme river discharges in the historical climate (1971-2000) based on the E-HYPEcatch multi-model ensemble.
- relative change in extreme river discharges in early-, mid- and end-century under climate scenarios based on the E-HYPEcatch multi-model ensemble.

The resolution of the gridded dataset is 5 km. The resolution of the catchment-level data is approx. 0.11 degrees (5-10 km).

Relative change in flood recurrence data is available for 2, 5, 10, 50-year return periods and for the following timelines:

- early century (2011-2040)
- mid-century (2041-2070)
- end-century (2071-2100)

For each time period, climate scenarios RCP2.6, RCP4.5 and RCP8.5 are available. 
Relative increases in flood recurrence for these periods are expressed relative to the reference period (1971-2000).


## Structure of the workflow

1. [Accessing data](./hazard_assessment_get_data.ipynb)
2. [Analyzing historical river discharge statistics](./hazard_assessment_timeseries_analysis.ipynb)

:::{note}
This workflow currently assesses hazard only.
:::


## Author

Natalia Aleksandrova (Deltares)
