---
layout: default
---

<img src="{{ site.url }}{{ site.baseurl }}/assets/img/eScience.png">


# Alaska Heating Loads

## The Team

**Project Lead:** Dr. Erin Trochim

**Data Science Lead:** Dr. Nicholas Bolten

**DSSG Fellows:** 
- Vidisha Chowdhury
- Maddie Gaumer
- Philippe Schicker
- Shamsi Soltani

# Abstract or executive summary
Alaska– and the wider Arctic region– have experienced accelerated effects of climate change over the past decade. Rapid decarbonization of energy is a critical step for mitigating climate change and ensuring sustainable development.. Since about 70% of energy consumption in Alaska can be attributed to commercial and residential heating, successful decarbonization requires an assessment of present and future heating needs in the region.

To date, comprehensive and accurate heating load estimates are lacking in Alaska. Modeling heating loads in Alaska is particularly complex for two distinct reasons: 
- First, many communities do not connect to the Energy Railbelt utility grid, making it difficult to accurately measure their heating loads. 
- Secondly, Alaska lacks centralization in utility providers and building codes, meaning there are no consolidated energy use data or efficiency standards for buildings.


This project is the first attempt to quantify large-scale Alaskan heating loads with high granularity, employing a geospatial-first methodology and machine learning techniques. Google Earth Engine (GEE), an open-source geographic information system, is used to combine the Open Street Map dataset to identify building footprints, with a Digital Elevation Model to calculate building volume. The age of each building is estimated using the World Settlements Footprint dataset. Data from the ERA5 climate dataset  is used to calculate local heating- and cooling degree days which are used to calculate projected energy consumption for each identified building. Statistical and machine learning regression approaches such as ordinary least squares, ridge, and random forests are explored in this project with the goal of estimating the hourly heating loads of Alaskan buildings along the Railbelt. The final regressions will be validated against existing models as well as against results from the AK Warm simulation software. The existing models are limited in that they only include small-scale regional estimations. These small-scale estimations will serve as a local validation option. We expect to verify heating load estimations for the past X years and generate heating load predictions for the next Y years using our model.

This project is scalable to the wider Arctic region, which mirrors many of the challenges that Alaska faces. Therefore, the methods developed can be used to estimate heating loads all across the arctic to contribute to climate change mitigation methods. 
