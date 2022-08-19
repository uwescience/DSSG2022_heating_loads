---
layout: page
title: Results
---
## Model Fit
With data on building features, climate, and simulated data on heating loads in Anchorage and Fairbanks, we estimate a model that can predict heating loads at the building level across the rest of Alaska's Railbelt.

We explored a range of models including ordinary least squares linear regression, ridge regressions with and without polynomial features, decision trees, and random forests. We evaluated these models using their mean squared error (MSE) on the test data. Model MSEs are listed below: errors decrease from top to bottom, with the Random Forest Regression performing the best.
<img src="{{ site.url }}{{ site.baseurl }}/assets/img/mse.png" width="700">
We are yet to explore a wide range of models, but will have the opportunity to do so as we gain access to a more comprehensive heating loads database from the [Alaska Housing Finance Corporation](https://www.ahfc.us/), due to be made public this year.

## Feature Importance

<img src="{{ site.url }}{{ site.baseurl }}/assets/img/feat.png" width="700">
## Data Sampling
<img src="{{ site.url }}{{ site.baseurl }}/assets/img/ds_res.png" width="700">

## Takeaways
+ We produce the first Alaskan heating load estimates that capture variation in local climate
+ These models allow prediction of future heating needs according to climate projections
+ This work can immediately inform renewable energy and climate mitigation policies in Alaska
