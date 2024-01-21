# Time Series Forecasting on COVID-19 and Cryptocurrency Data

This project involves time series analysis and forecasting on two distinct datasets: COVID-19 cases and cryptocurrency closing prices. The analysis implements various statistical and machine learning techniques to understand the underlying patterns, check for stationarity, and forecast future values.

## Dependencies

- Pandas
- NumPy
- Statsmodels
- Matplotlib
- SciPy
- Scikit-learn
- PMDARIMA

## Installation

To run the analysis, ensure that you have the latest versions of the dependencies installed. You can install them using pip:


## Dataset Description

### COVID-19 Dataset

- **Source**: Provided CSV file `covid19.csv`.
- **Variables**: Daily cases reported in a randomly selected country.
- **Period**: Data covers from March 5, 2020, to December 14, 2020.

### Cryptocurrency Dataset

- **Source**: Provided Excel file `dataset.xlsx`.
- **Variables**: Daily closing prices of a randomly selected cryptocurrency.
- **Period**: Specific time range not provided.

## Analysis Overview

### COVID-19 Time Series Analysis

1. **Data Visualization**: Plotting the daily cases to comment on the existence of seasonality and/or trend.
2. **Stationarity Checks**: Utilizing ADF and KPSS tests to check for stationarity and applying first-order differencing to achieve stationarity.
3. **Dependence Order Identification**: Using ACF and PACF plots to identify the orders for the SARIMA model.
4. **Model Estimation and Diagnostics**:
   - Dividing data into train and test sets.
   - Estimating SARIMA models.
   - Conducting residual diagnostics including Ljung-Box test.
5. **Forecasting**: Forecasting the next 7 days using the best SARIMA model based on AIC/BIC and comparing model performances.

### Cryptocurrency Time Series Analysis

1. **Data Visualization and Decomposition**: Describing the main features like seasonality and trend using plots and decomposing the series into trend, seasonal, and residual components.
2. **Model Selection and Forecasting**:
   - Dividing the series into train and test sets.
   - Choosing the best ETS model based on AIC/BIC.
   - Estimating SARIMA models using `auto.arima`.
   - Forecasting for the test set and comparing performances of ETS and SARIMA models.
3. **Extended Forecasting**: Generating and plotting forecasts for the next 10 days with both models on the original data.

## Results

- The analysis provides insights into the temporal dynamics of COVID-19 cases and cryptocurrency closing prices.
- Stationarity was achieved through differencing for the COVID-19 dataset, indicating non-stationary original series.
- The SARIMA(5,1,1)(1,0,0)[7] and SARIMA(2,1,0)(1,0,1)[7] models were identified and compared for the COVID-19 dataset, with forecasts generated for the next 7 days.
- For the cryptocurrency dataset, various ETS models were compared, and the best fitting model was used for forecasting the next 10 days.
- Model diagnostics and forecasting accuracy were assessed using residual analysis and mean squared error (MSE) respectively.

## Conclusion

The time series analysis and forecasting conducted on both COVID-19 and cryptocurrency datasets highlight the importance of understanding data characteristics, achieving stationarity, and selecting appropriate models for accurate forecasting. The analysis showcases the application of SARIMA and ETS models in addressing real-world forecasting problems.

