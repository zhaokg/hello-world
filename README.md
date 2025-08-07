# GEE NDVI and LST Compositing Scripts

## Overview

These Google Earth Engine (GEE) scripts utilize surface reflectance data from **Landsat 7 ETM+** (Enhanced Thematic Mapper Plus) and **Landsat 8 OLI** (Operational Land Imager) to generate a series of NDVI images for a defined time period and study area. In addition, surface temperature data from **Landsat 8 TIRS** (Thermal Infrared Sensor) is used to produce composite Land Surface Temperature (LST) images over the same temporal and spatial extent.

The case study focuses on **Cuyahoga County, Ohio**. NDVI composites are based on growing season imagery from **April to October (2016–2018)** to align with **2017 high-resolution land cover data** from the Cuyahoga County Planning Commission. LST composites use imagery from **May to September** during the same time period.

## Preprocessing Notes

To enhance compatibility between Landsat 7 and Landsat 8 datasets, band-level transformations from Roy et al. (2016) were applied to Landsat 7 surface reflectance data:

> Roy et al., 2016. *Characterization of Landsat-7 to Landsat-8 reflective wavelength and normalized difference vegetation index continuity*.  
> https://doi.org/10.1016/j.rse.2015.12.024

## Usage

These scripts must be run within the **Google Earth Engine Code Editor** to access Earth Engine-hosted assets.

When exporting images, it is recommended to use a **UTM Zone 17N projection** or **EPSG:4326** for consistency with other spatial data.

## Data Sources

- [USGS Landsat 7 Level 2, Collection 2, Tier 1](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LE07_C02_T1_L2)
- [USGS Landsat 8 Level 2, Collection 2, Tier 1](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LC08_C02_T1_L2)
- [Landsat Level 2, Collection 2 Documentation](https://www.usgs.gov/media/files/landsat-8-9-olitirs-collection-2-level-2-data-format-control-book)
