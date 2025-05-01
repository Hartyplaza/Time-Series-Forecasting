# Time Series Forecasting with ARIMA Model: Monthly Champagne Sales Analysis

This repository contains a Jupyter Notebook that demonstrates time series forecasting using an ARIMA model to analyze monthly champagne sales data.

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Results](#results)
- [Limitations](#limitations)
- [Future Improvements](#future-improvements)
- [Usage](#usage)
- [Dependencies](#dependencies)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This project aims to predict future monthly champagne sales based on historical data using an ARIMA model. The analysis includes data preprocessing, stationarity analysis, seasonal decomposition, ACF and PACF analysis, model selection, and evaluation.

## Dataset

The dataset used is "Monthly Champagne Sales," which contains monthly observations of champagne sales volume (in units/bottles) spanning multiple years. The data exhibits strong seasonality with peaks typically occurring during holiday seasons.

## Methodology

1. **Data Preprocessing:** Loading, renaming columns, converting to datetime, and setting 'date' as the index.
2. **Yearly Average Sales Analysis:** Calculating and visualizing average sales per year.
3. **Stationarity Analysis:** Performing the Augmented Dickey-Fuller (ADF) test to assess stationarity and applying differencing if necessary.
4. **Seasonal Decomposition:** Decomposing the time series into trend, seasonality, and residuals using `seasonal_decompose`.
5. **ACF and PACF Analysis:** Examining autocorrelation and partial autocorrelation functions to determine model parameters.
6. **Data Splitting:** Dividing the data into training and testing sets (80/20 split).
7. **SARIMA Model:** Fitting a baseline SARIMA model and evaluating its performance.
8. **Grid Search:** Performing a grid search to find optimal SARIMA parameters based on AIC.
9. **Model Training and Selection:** Training the best model with optimal parameters.
10. **Forecasting Performance:** Generating forecasts and comparing them to actual sales.
11. **Evaluation:** Assessing the model's accuracy using metrics like MAE and RMSE.

## Results

The analysis reveals a strong seasonal pattern in champagne sales, with predictable peaks around certain months and an underlying growth trend. The SARIMA model effectively captures these patterns, providing accurate forecasts.

## Limitations

- External factors like economic changes, competitor actions, and regulatory changes are not considered.
- The model assumes that historical patterns will continue without structural breaks.

## Future Improvements

- Include external regressors using SARIMAX.
- Explore machine learning alternatives like Facebook Prophet or LSTM models.
- Implement ensemble techniques.

## Usage

1. Clone this repository.
2. Open the Jupyter Notebook `Champagne_Sales_Forecast.ipynb`.
3. Run the cells to execute the code and view the results.

## Dependencies

- pandas
- numpy
- matplotlib
- statsmodels
- scikit-learn

Install dependencies using:
