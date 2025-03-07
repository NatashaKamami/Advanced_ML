# Air Quality Forecasting Project

## Project Overview
This project focuses on air quality forecasting using two time-series forecasting models: SARIMAX and Prophet. The goal is to predict key air pollutants such as PM2.5, PM10, SO2, NO2, CO, and O3 based on historical data and meteorological factors.

## Project Goal
The primary objective of this project is to compare SARIMAX and Prophet for air quality forecasting and analyze how meteorological factors influence pollutant levels. By leveraging time-series modeling techniques, this project provides insights into air pollution trends, aiding environmental monitoring and decision-making.

## Dataset
The dataset used in this project is an `.arff` file containing air quality measurements. It includes pollutant levels and meteorological factors such as temperature, pressure, dew point, rainfall, and wind speed.

## Methodology
### 1. Data Cleaning
Interpolation was used to fill in missing values in the dataset and unneccessarry columns were also dropped.

### 2. Data Preprocessing
I ensured the 'year', 'month', 'day', 'hour' columns were combined into a datetime column. I then set the datetime column as the index and i then resampled the data to monthly frequency for easy plotting and readability.

### 3. Time-Series Decomposition
The dataset was decomposed into trend, seasonality, and residuals using both additive and multiplicative decomposition models.

### 4. Forecasting Models
#### **SARIMAX Model**
First, a SARIMAX model was trained for each pollutant using meteorological variables as the exogenous inputs. The dataset was split into training and test sets and the SARIMAX model was fitted. The model was evaluated using Mean Absolute Error (MAE), and the predictions were visualized.

#### **Prophet Model**
A Prophet model was also trained for each pollutant with meteorological factors as regressors. The dataset was reformatted to fit Prophet's requirements and the model was trained, and future forecasts are generated for the next 12 months. The predictions were evaluated using MAE, and forecasted trends were visualized.

## Conclusion
This project demonstrates how time-series forecasting techniques can be applied to predict air pollution levels. Both SARIMAX and Prophet models generated forecasts for air pollutants and their effectiveness was evaluated using MAE. The results gotten help in understanding air quality trends, which can be beneficial for policymakers, environmental agencies, and researchers interested in air pollution monitoring and control.


