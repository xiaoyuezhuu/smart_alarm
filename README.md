## Overview
This is a class project for the machine learning class. The smart alarm system is developed for behavioral neuroscience labs. It performs unsupervised anomaly detection on animal behavioral data (multivariate time series) and alerts the users of abrupt changes in animal performance.

## Details
It first performs ForeCA (forecastable component analysis) on the noisy multivariate time series to reduce dimensionality and smooth the data. It then performs ARIMA (autoregrdssive integrated moving average) on the individual ForeCA components to generate a prediction interval. The outliers in each ForeCA component is simply the points that lie outside of the prediction interval. Finally, a user-defined threshold is applied to determine how many ForeCA components with outliers are required for this to be quanlified as an anomaly. 

## Implementation
The system is currently being implemented in our lab. It can also be applied in other labs / areas where unsupervised anomaly detection on noisy multivariate time series is needed, espcially when low computing cost is prioritized (LSTM takes too much time). 
