# ARIMA
Generic ARIMA analysis for time series implemented from https://towardsdatascience.com/time-series-in-python-exponential-smoothing-and-arima-processes-2c67f2a52788

## Related works:

* Kumar, Prashant. "Forecasting Cloud Resource Utilization Using Time Series Methods." (2018). http://www.diva-portal.se/smash/get/diva2:1273037/FULLTEXT01.pdf
(ARIMA + ES) > ARIMA
 FFNN > (ARIMA + ES)
  * Good description of data preparation. We can adapt our data to use the same configuration without too many problems
Just uses the CPU measurements

* Paul Newbold and C W. J. Granger. “Experience with Forecasting Univariate Time Series and the Combination of Forecasts”
  * This paper suggested that a combination of individual forecasting models performs better than any individual forecasting.

* Islam, S., Keung, J., Lee, K., & Liu, A. (2012). Empirical prediction models for adaptive resource provisioning in the cloud. Future Generation Computer Systems, 28(1), 155-162.
  * “... Individual samples may not be a representative of the true resource utilization level… ”

## Data prep:

* “This kind of data tends to have a trend” - Kumar, Prashant. "Forecasting Cloud Resource Utilization Using Time Series Methods." (2018).
* The same data gaps for CPU and Memory
* The CPU and Memory are High correlated
* It's a bad idea to use CPU and Memory together as a hyperparameters, but it’s a good idea to test them individually to check the true representativeness

## Completed tasks:
* The data gaps are filled using interpolation techniques 
* A standard  for all the files considering a hourly frequence

## Time series Analysis:

* A trend (upward or downwards movement of the curve on the long term)
* A seasonal component
* Residuals

About ARIMA:
* ARIMA models should be used on stationary data only. 
* To obtain the best performance of model, we need to make the data stationary
  * De-trending
  * Seasonal adjustment
  * Transformation
  * Smoothing
* Time series with trends, or with seasonality, are not stationary


## Smoothing methods:
* Smoothing methods work as weighted averages. Forecasts are weighted averages of past observations. 
* Simple Exponential Smoothing
  * Few data points, Irregular data, No seasonality or trend.
* Holt’s Linear Smoothing
  * Trend in data, No seasonality.
* Holt’s Damped Trend
  * Data has a trend
* Exponential smoothing (ES)
  * One of most flexible methods (related to time series patterns)

