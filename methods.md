---
layout: page
title: Project Pipeline
---
Our workflow involves using Google Earth Engine’s public data archive to extract tabulated building-level features and then train machine learning models to predict heating loads.

<img src="{{ site.url }}{{ site.baseurl }}/assets/img/pipeline.png" width="800">

This section describes the following components of our data pipeline.
1. [Data Sources](#data-sources)
2. [Feature Extraction](#feature-extraction)
3. [Optimizing Data Exports](#optimizing-data-exports)
4. [Model Estimation](#model-estimation)

## Data Sources

The sources used to extract building-level attributes and local climate variables were open access and available in Google Earth Engine's archive. Features developed and their source datasets are:
+ Building footprint area
	+ [OpenStreetMap](https://www.openstreetmap.org)
+ Building age
	+ [World Settlement Footprint Evolution (1985-2015) & World Settlement Footprint 2019](https://samapriya.github.io/awesome-gee-community-datasets/projects/wsf/)
	+ [Dynamic World](https://developers.google.com/earth-engine/datasets/catalog/GOOGLE_DYNAMICWORLD_V1)
+ Building height
	+ [Forest and buildings removed Copernicus 30m Digital Elevation Model (FABDEM)](https://samapriya.github.io/awesome-gee-community-datasets/projects/fabdem/)
	+ [Copernicus Digital Elevation Model (GLO-30 DEM)](https://samapriya.github.io/awesome-gee-community-datasets/projects/glo30/)
+ Heating and cooling degree days 
	+ [ERA5-Land Hourly](https://developers.google.com/earth-engine/datasets/catalog/ECMWF_ERA5_LAND_HOURLY)
+ Building zip codes 
 	+ [TIGER: US Census Roads](https://developers.google.com/earth-engine/datasets/catalog/TIGER_2016_Roads)
 	+ 

<img src="{{ site.url }}{{ site.baseurl }}/assets/img/copernicus_sat.png" width="350">
<sub>_Photo credit: European Space Agency; Data for this project come from satellites like this one._</sub>

## Feature Extraction

The extraction of building features from geospatial data was one of the biggest and most challenging aspects of our project. For this, we used Google Earth Engine which is a cloud computing platform that allows one to access and analyse geospatial big data. The public datasets we used from Google Earth Engine’s archive consisted of satellite images captured across time as well as geometries of building outlines in Alaska. We had to aggregate these data both temporally and spatially to arrive at building level features and then export these as tabular data for analysis.


## Optimizing Data Exports

Each building had to be matched to its area's zip code and then building information was exported in batches of zip code groups. 

## Model Estimation
<img src="{{ site.url }}{{ site.baseurl }}/assets/img/ak_anch_fair.png" width="350">
<!--  note you can make text wrap by adding img align="right" between img and src-->

With data on building features, climate, and simulated data on heating loads in Anchorage and Fairbanks, we estimate a supervised learning model that can predict heating loads at the building level across the rest of Alaska's Railbelt.

We explored a range of models including ordinary least squares linear regression, ridge regressions with and without polynomial features, decision trees, and random forests. We evaluated these models using their mean squared error (MSE) on the test data. Model MSEs are listed below: errors decrease from top to bottom, with the Random Forest Regression performing the best.

<img src="{{ site.url }}{{ site.baseurl }}/assets/img/mse.png" width="700">
We are yet to explore a wide range of models, but will have the opportunity to do so as we gain access to a more comprehensive heating loads database from the [Alaska Housing Finance Corporation](https://www.ahfc.us/), due to be made public this year.

