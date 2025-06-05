Florida Palmetto Species Classification with Binary Logistic Regression
================

# Contents

This repository (knitted HTML linked here:
[palmetto-regression](https://jadenorli.github.io/palmetto-species/code/palmetto-regression.html))
applies binary logistic regression models to classify two palmetto
species, ***Sabal etonia*** and ***Serenoa repens***, based on
morphological characteristics. The analysis compares a **standard
logistic regression model** and an **elastic net regularized
regression**, with the goal of evaluating classification performance and
interpretability.

# Techniques

This repository highlights a variety of skills and techniques including:

1.  Data Management
    - Wrangling and tidying data using \[@tidyverse\], \[@here\], and
      \[@janitor\]

    - Visualizations with \[@ggplot2\] and \[@tmap\]

    - Clear documentation and folder structures for reproducibility,
      collaboration, and modularity

    - Integration of conditional statements and custom checks to
      increase reproducibility, error handling, and modularity

    - Development of generalizable functions to allow for
      reproducibility and flexibility in analyses
2.  Geospatial Analysis
    - Handling spatial data with \[@terra\] and \[@sf\]

    - Generating informative interactive maps with \[@tmap\]

    - Map algebra with spatial objects within \[@terra\] and \[@sf\]
3.  Sustainable Fisheries Science
    - Adapting concepts from \[@gentry2017\] and \[@troell2009\] to
      analyze potential locations within the West Coast EEZs that are
      suitable for integrative multi-trophic aquaculture (IMTA) with
      oysters and a variety of potential finfish species

    - Integration of flexible species-specific tolerances throughout the
      spatial analyses

# Data

- The first dataset is Sea Surface Temperature (SST) from the [NOAA
  Coral Reef Watch Daily 5km Satellite Sea Surface Temperature (SST)
  (v3.1)](https://coralreefwatch.noaa.gov/product/5km/index_5km_sst.php)
  to characterize the average annual sea surface temperature inside the
  region of interest for the years 2008 to 2012 (@noaa_crw_sst_2024).

- The second dataset is bathymetry data from the [General Bathymetric
  Chart of the Oceans
  (GEBCO)](https://www.gebco.net/data_and_products/gridded_bathymetry_data/#area)
  which we used to generate a depth profile for the areas with the
  Economic Exclusion Zones (EEZ) (@gebco2024).

- The third dataset is a shapefile from the [Flanders Marine
  Institute](https://www.marineregions.org/eez.php) that was used to
  define the area of U.S. waters within the EEZ (@flanders2024).

- The fourth dataset was created in two steps:

  1.  First, potential finfish species were identified through an
      evaluation of the harvested species managed by the [West Coast
      NOAA Fisheries](https://www.fisheries.noaa.gov/species-directory)
      to compile a list of potentially compatible species
      (@noaa_west_coast).
  2.  Then, life history parameters (thermal range of tolerance and
      vertical distribution) were obtained from
      [FishBase](https://www.fishbase.org.au/v4) (@fishbase2024).

# Repository Structure

``` bash
      .
      ├── README.md
      ├── bibs
      │   ├── packages.bib
      │   └── references.bib
      ├── code
      │   ├── custom.css
      │   ├── marine_aquaculture.html
      │   └── marine_aquaculture.qmd
      ├── data
      │   ├── average_annual_sst_2008.tif
      │   ├── average_annual_sst_2009.tif
      │   ├── average_annual_sst_2010.tif
      │   ├── average_annual_sst_2011.tif
      │   ├── average_annual_sst_2012.tif
      │   ├── depth.tif
      │   ├── potential_finfish_species.csv
      │   ├── wc_regions_clean.dbf
      │   ├── wc_regions_clean.prj
      │   ├── wc_regions_clean.shp
      │   └── wc_regions_clean.shx
      ├── figures
      │   ├── heatmap
      │   │   └── species_vs_region_heatmap.png
      │   ├── maps
      │   │   ├── NULL_map.png
      │   │   ├── anoplopoma_fimbria_map.html
      │   │   ├── anoplopoma_fimbria_map.png
      │   │   ├── ...
      │   └── tables
      │       ├── potential_species_kable.html
      │       ├── spatial_properties_kable.html
      │       ├── spatial_properties_kable_sst_bath.html
      │       ├── spatial_properties_kable_sst_bath_transform.html
      │       └── top_regions_kable.html
      ├── marine-aquaculture.Rproj
      └── structure.txt
```

# References
