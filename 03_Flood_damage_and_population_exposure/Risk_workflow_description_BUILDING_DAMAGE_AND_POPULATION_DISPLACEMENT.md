# Flood building damage and population exposed

## Introduction to the workflow

Flooding, whether coastal, fluvial, or pluvial, is a major hazard to humans. This workflow aims at assessing how this hazard affects built up areas by looking at economic damage represented by building damage, impact on critical infrastructures (such as hospitals, water tower, etc.), as well as the impact on the population through estimating the number of people exposed to the hazard and the number of people displaced by it.
 
## Risk assessment methodology

### How is risk calculated?
The risk from flooding is assessed in this worflow by creating flood maps using the water level projections under a variety of return periods, and perform risk analysis on these flood maps to estimate building damage (by using damage curves and building geometry/type) and populations exposed and displaced (by using a population map).
The datasets used in this workflow by default are further described [below.](#datasets-used-in-the-workflow)
The datasets are European European and Meditterenean wide flood data, global population data, and global building data. Local data can be used, and it is encoureged to do so, by modifying the code. 

```{note}
This workflow takes:
- Hazard: Flood event.
- Exposure: Building and population data.
- Vulnerabity: Damage curves and water height for displacement.
And outputs the risks:
- Economic damage to buildings.
- Population displaced.
![how_to_get_risk](../images/infographic_how_to_get_risk.png)
```


### Which flood maps to use?

The flood map used, taken from “River flood hazard maps for Europe and the Mediterranean Basin region”, and found on the [European Commission’s Joint Research Centre](https://data.jrc.ec.europa.eu/dataset/1d128b6c-a4ee-4858-9e34-6210707f3c81#description), is a European wide flood map. It is used to estimate water levels for 9 different return periods ranging from 10 to 500 years. 
While this data can be a good starting position, it has some limitations: it only contains large basins and does not include the impact of flood protection infrastrucutre. Hence, using local data may be necessary depending on the area of interest. 


## Description of workflow 

### Structure
The workflow example that is provided in this toolbox has a hazard and a risk assesment component:

**Hazard assessment:** Explore different flood return period's water levels in the area of interest.
In this assessment, the water level is retrieved and flood maps are generated for a variety of return periods.  

**Risk assessment:** Explore the building damage, critical infrastructure impacted, population exposed and displaced, for the area of interest.
In this assessment, the potential risks due to flooding are estimated by combining the flood maps generated from different return periods with the damage curves, populations maps, and building data. Moreover, the population map generated and used can be chosen from a variety of past and future dates (more information [below.](#datasets-used-in-the-workflow)).


### Datasets used in the workflow 

The following datasets are used in this workflow:
- **Flood map:** [“River flood hazard maps for Europe and the Mediterranean Basin region”](https://data.jrc.ec.europa.eu/dataset/1d128b6c-a4ee-4858-9e34-6210707f3c81#description) dataset, created by the Copernicus Emergency Management Service (Baugh et al., 2024), and available via the European Commission’s Joint Research Centre. The dataset maps flood water depths over return periods 10, 20, 50, 100, 200, and 500, at a resolution of 3 arc seconds, covering longitude -24.54° to 67.26°, and latitude 27.81° to 71.13°  
- **Population density:** [GHS-POP R2023A](https://data.jrc.ec.europa.eu/dataset/2ff68a52-5b5b-4a22-8f40-c41da8332cfe) dataset (Schiavina et al., 2023), published by the European Commission’s Joint research Centre is used for mapping the population estimates or projections, with a resolution of 3 arc seconds and a global cover. The workflow allows for selecting the population estimate in 5-year intervals between 1975 and 2020, or the population projection of either 2025 or 2030. 
- **Building data:** [OpenStreetMap](https://wiki.openstreetmap.org/wiki/Main_Page) is used to collect building information, both geometry and classification.


### Output of the workflow

For a specific area, this workflow outputs: 
- Flood depth maps for a specific return period. 
- Population raster for a specific date. 
- Damage curves by class type. 
- Map of building type and class. 
- Building water exposure maps. 
- Building damage maps and estimated annual building damage graph. 
- Critical infrastructure map with flooded area. 
- Population exposed maps and estimate annual exposed population graph. 
- Population displaced maps and estimate annual displaced population graph. 