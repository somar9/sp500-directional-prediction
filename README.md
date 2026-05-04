# S&P 500 Directional Prediction Analysis

## Overview

This project investigates whether the daily directional movement of the S&P 500 can be predicted using machine learning, focusing on model evaluation and reliability rather than raw predictive power. 
The findings highlights the challenges of extracting strong predictive signals from financial time series data.

## Methodology 

- Historical S&P 500 data with VIX and interest rate features
- Engineered extra features such as returns, rolling statistics and lagged variables
- Chronological 80/20 train-test split to prevent look-ahead bias
- Models: Random Forest and XGBoost (final model selected based on performance)

## Key Findings

- Model achieves ~54% accuracy, closely comparable to a majority-class baseline
- Strong bias towards predicting upward movements
- Poor detection of downside movements
- Model performance deteriorates during major market regime shifts (e.g. COVID-19)

## Dashboard
- Rolling accuracy over time
- Performance across volatility regimes
- Confusion Matrix and directional precision

![Dashboard](dashboard.png)

## Limitations 
- No meaningful improvement over baseline
- Weak predictive signal
- Financial markets are non-stationary, reducing model stability
- Predictive power is constrained by feature quality: the inputs are primarily price-derived and publicly available, which are unlikely to contain strong predictive signal
- Improving results would likely require access to richer data sources, such as order book information or higher frequency data, rather than increased model complexity.

# Tech Stack

Python, Pandas, NumPy, Scikit-learn, XGBoost, Tableau
