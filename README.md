# texas-storms-power-crisis
Identifying impacts of Texas storms on power outages

# Purpose

This repository contains a spatial analysis of power outages in the Houston area during the February 2021 Texas winter storm. VIIRS nighttime light data from before and during the storm were compared to identify areas with decreases in nighttime light intensity. The analysis estimates the spatial extent of blackout areas and the number and percentage of homes potentially affected.

# Data

**Data Access**

The raw datasets are not included in this GitHub repository and must be downloaded separately.

Nighttime light data: VIIRS VNP46A1 nighttime light data for February 7 and February 16, 2021, from NASA's Level-1 and Atmosphere Archive & Distribution System Distributed Active Archive Center (LAADS DAAC).

Road data: OpenStreetMap road data for the Houston area, downloaded from Geofabrik.

Building data: OpenStreetMap building data for the Houston area, downloaded from Geofabrik.

**Data Organization**

```
texas-storms-power-crisis/
├── .gitignore                     # Contains data/ so raw data are not tracked by Git
├── README.md
├── texas-storms-power-crisis.qmd
├── texas-storms-power-crisis.pdf
└── data/                          # Local data folder, ignored by Git
    ├── VNP46A1/
    │   ├── VNP46A1.A2021038.h08v05.001.2021039064328.tif
    │   ├── VNP46A1.A2021038.h08v06.001.2021039064329.tif
    │   ├── VNP46A1.A2021047.h08v05.001.2021048091106.tif
    │   └── VNP46A1.A2021047.h08v06.001.2021048091105.tif
    ├── gis_osm_roads_free_1.gpkg
    └── gis_osm_buildings_a_free_1.gpkg
```
**Libraries**

```
library(sf)
library(tidyverse)
library(tmap)
library(here)
library(stars)
library(gt)
library(testthat)
```

## Author
Veronica Moran

Master of Environmental Data Science (MEDS), UC Santa Barbara

# References

[1] NASA Level-1 and Atmosphere Archive & Distribution System Distributed Active Archive Center (LAADS DAAC). VIIRS VNP46A1 nighttime light data.

[2]OpenStreetMap contributors. Road and building data distributed through Geofabrik.
