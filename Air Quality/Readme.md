# Air Quality Forecasting

## OBJECTIVE (Problem Statement)

Air quality modeling to predict future contaminants(e.g particulate matter 2.5mm) concentration in various Chineese Cities using time series algorithms ARIMA, SARIMA, and PROPHET.

# Data Preprocessing
- Converting dataset to proper datetime format
- Handle missing datetimes and values (Imputation strategies:

For meteorological data (TEMP, PRES, etc.) or pollutants (PM2.5, SO2, etc.), fill with mean, median, or interpolation

For categorical columns like wd (wind direction), use mode:)
- Daily Aggregation
Aggregation in time series data analysis refers to the process of summarizing or condensing data over specific time intervals, such as hourly, daily, weekly, or monthly. This involves combining multiple data points within a given time window into a single representative value, such as a sum, mean, maximum, or minimum.
Purpose of Aggregation

Reduce Noise: Aggregation smooths fluctuations, making trends and patterns more apparent.
Align with Analysis Goals: Hourly aggregation to study diurnal patterns.Daily aggregation to analyze day-to-day trends.
Improve Model Performance by simplifying data and reduce computational requirements while maintaining the essence of the underlying trends.
Highlight seasonal patterns, trends, or anomalies that may not be evident at finer resolutions.

## Splitting the Dataset into Training and Test sets
To split the dataset into training and test sets, I considered the temporal nature of the data. I used a time-based split rather than a random split. This ensures that the test set includes future data relative to the training set, which is more realistic for time series forecasting and analysis.

## Feature Engineering
Feature engineering on the train_data dataset based on the provided guidelines involves creating new features that enhance the predictive power of the model.

# Modeling
I used ARIMA, SARIMA, and PROPHET models for the time series air quality forecasting 

# INSIGHTS:

- ARIMA model performed poorly on future predictions, giving a near flat line prediction for particulate matter 2.5mm (PM2.5) on the station of Dingling
- SARIMA model did improve the prediction slightly by capturing small seasonal variations in the training data which match with seasonal variations in the test data.
- The prophet model predictions were able to match the general trend along the given timeling (Jan 2016 - March 2017) but failed to capture the seasonal variations with precision.


