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
Alaska– and the wider Arctic region– have experienced accelerated effects of climate change over the past decade. For a complete picture of mitigation possibilities, there is a pressing need to understand heating loads across residential and commercial buildings in the state. The estimation and modeling of heating loads in Alaska is particularly complex for two distinct reasons. The primary challenge is that many communities along the Railbelt are often in remote areas, making it difficult to accurately measure their heating loads. Secondly, Alaska lacks centralization in its utility providers as well as in its building codes, meaning there is no centralized energy use data or standardized energy efficiency standards for buildings.

This project represents the first attempt to quantify large-scale Alaskan heating loads with a high granularity, employing a geospatial-first methodology combined with machine learning techniques. Google Earth Engine (GEE), an open-source geographic information system, is used to combine the Open Street Map dataset to identify building footprints, with the Digital Elevation Model to calculate building volume. For each building, its age is estimated using the World Settlements Footprint dataset. Data from the ERA5 climate dataset  is used to calculate local heating- and cooling degree days which are used to calculate projected energy consumption at an hourly level for each identified building. Statistical and machine learning regression approaches such as ordinary least squares, ridge, and random forests are explored in this project with the goal of estimating the hourly heating loads of Alaskan buildings along the Railbelt. The final regressions will be validated against existing models as well as against results from the AK Warm simulation software. The existing models are limited in that they only include small-scale regional estimations. These small-scale estimations will serve as a local validation option. We expect to verify heating load estimations for the past X years and generate heating load predictions for the next Y years using our model.

This project is scalable to the wider Arctic region, which mirrors many of the challenges that Alaska faces. Therefore, the methods developed can be used to estimate heating loads all across the arctic to contribute to climate change mitigation methods. 
