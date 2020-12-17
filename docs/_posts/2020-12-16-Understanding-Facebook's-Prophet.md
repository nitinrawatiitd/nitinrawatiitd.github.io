---
layout: post
tags: forecasting
---

Source - https://research.fb.com/blog/2017/02/prophet-forecasting-at-scale/#:~:text=How%20Prophet%20works,selecting%20changepoints%20from%20the%20data.

# Advantages of Prophet
* hourly, daily, or weekly observations with at least a few months (preferably a year) of history
* strong multiple “human-scale” seasonalities: day of week and time of year
* important holidays that occur at irregular intervals that are known in advance (e.g. the Super Bowl)
* a reasonable number of missing observations or large outliers
* historical trend changes, for instance due to product launches or logging changes
* trends that are non-linear growth curves, where a trend hits a natural limit or saturates

# How Prophet works
At its core, the Prophet procedure is an additive regression model with four main components:

* A piecewise linear or logistic growth curve trend. Prophet automatically detects changes in trends by selecting changepoints from the data.
* A yearly seasonal component modeled using Fourier series.
* A weekly seasonal component using dummy variables.
* A user-provided list of important holidays.

Note: Maybe changing trend in seasonality, like in sensor data, could be also help improve the model 
