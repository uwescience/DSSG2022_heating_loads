---
layout: page
title: Project Pipeline
---
Our workflow involves using Google Earth Engine’s public data archive to extract tabulated building-level features and then train machine learning models (using Python's Scikit Learn library) to predict heating loads.

<img src="{{ site.url }}{{ site.baseurl }}/assets/img/pipeline.png" width="800">

This section describes the following components of our data pipeline.
1. [Data Sources](#datasources)
2. [Optimizing Data Exports](## Optimizing Data Exports)
3. <a href="#FeatureExtraction">Feature Extraction</a>
5. <a href="#ModelEstimation">Model Estimation</a>

## Data Sources

The sources used to extract building-level attributes and local climate variables were open access and available in the Google Earth Engine archive. Features developed and their source datasets are:
+ Building footprint area
	+ [OpenStreetMap](https://www.openstreetmap.org)
+ Building age
	+ [World Settlement Footprint Evolution (1985-2015) & World Settlement Footprint 2019](https://samapriya.github.io/awesome-gee-community-datasets/projects/wsf/)
	+ [Dynamic World](https://developers.google.com/earth-engine/datasets/catalog/GOOGLE_DYNAMICWORLD_V1)
+ Building height
	+ [Forest and buildings removed Copernicus 30m Digital Elevation Model (FABDEM)](https://samapriya.github.io/awesome-gee-community-datasets/projects/fabdem/)
	+ [Copernicus Digital Elevation Model (GLO-30 DEM)](https://samapriya.github.io/awesome-gee-community-datasets/projects/glo30/)
+ Heating and cooling degree days (derived from average daily land temperature)
	+ [ERA5-Land Hourly](https://developers.google.com/earth-engine/datasets/catalog/ECMWF_ERA5_LAND_HOURLY)

<img src="{{ site.url }}{{ site.baseurl }}/assets/img/copernicus_sat.png" width="350">
<sub>_Photo credit: European Space Agency; Data for this project come from satellites like this one._</sub>

## Optimizing Data Exports

What did you do to prepare the data?


Regressions used to estimate heating loads in Anchorage and Fairbanks were sourced from the [2014 Alaska Housing Assessment](https://www.ahfc.us/pros/energy/alaska-housing-assessment/housing-assessment).

## Machine Learning / Modeling
<img src="{{ site.url }}{{ site.baseurl }}/assets/img/ak_anch_fair.png" width="350">
<!--  note you can make text wrap by adding img align="right" between img and src-->

With data on building features, climate, and simulated data on heating loads in Anchorage and Fairbanks, we estimate a _supervised learning?_ model that can predict heating loads at the building level across the rest of Alaska's Railbelt.

We explored a range of models including ordinary least squares linear regression, ridge regressions with and without polynomial features, decision trees, and random forests. We evaluated these models using their mean squared error (MSE) on the test data. Model MSEs are listed below: errors decrease from top to bottom, with the Random Forest Regression performing the best.

<img src="{{ site.url }}{{ site.baseurl }}/assets/img/mse.png" width="700">
We are yet to explore a wide range of models, but will have the opportunity to do so as we gain access to a more comprehensive heating loads database from the [Alaska Housing Finance Corporation](https://www.ahfc.us/), due to be made public this year.

## Data Challenges
+ Sparse or inaccurate data in the Arctic
+ Google Earth Engine big data exports
