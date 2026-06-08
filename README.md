# Seoul Air Pollution Analysis and PM2.5 Forecasting

## Overview

This project analyzes air quality data collected from monitoring stations across Seoul, South Korea, and develops a machine learning model to forecast PM2.5 concentrations.

The workflow includes data integration, data cleaning, exploratory data analysis (EDA), feature engineering, and predictive modeling using a Random Forest Regressor.

---

## Problem Statement

Air pollution is a major public health concern in urban environments. Fine particulate matter (PM2.5) is particularly harmful because it can penetrate deep into the lungs and bloodstream.

The objective of this project is to:

* Analyze pollution patterns across Seoul districts.
* Identify relationships among major pollutants.
* Study temporal pollution trends.
* Forecast PM2.5 concentrations using machine learning.

---

## Dataset Description

The project uses three datasets:

### 1. Measurement Information

Contains:

* Pollutant measurements
* Timestamps
* Station identifiers

### 2. Item Information

Contains:

* Pollutant metadata
* Units of measurement
* Air quality thresholds

### 3. Station Information

Contains:

* District names
* Geographic coordinates
* Station details

---

## Pollutants Analyzed

| Pollutant | Description                |
| --------- | -------------------------- |
| SO2       | Sulfur Dioxide             |
| NO2       | Nitrogen Dioxide           |
| CO        | Carbon Monoxide            |
| O3        | Ozone                      |
| PM10      | Particulate Matter ≤10 µm  |
| PM2.5     | Particulate Matter ≤2.5 µm |

---

## Project Workflow

### Data Integration

* Merged Measurement, Item, and Station datasets.
* Created a unified analytical dataset.

### Data Cleaning

* Investigated instrument status codes.
* Retained only valid measurements.
* Handled missing values.

### Exploratory Data Analysis

* Correlation analysis
* District-level pollution analysis
* Monthly pollution trends
* Hourly pollution trends
* Yearly pollution trends

### Feature Engineering

Created:

* Year
* Month
* Day
* Hour
* DayOfWeek
* PM25_lag1
* PM25_lag24

### Machine Learning

Model:

* Random Forest Regressor

Target Variable:

* PM2.5

---

## Key Findings

### Pollutant Relationships

* PM10 showed the strongest correlation with PM2.5 (r ≈ 0.83).
* CO showed a moderate correlation with PM2.5 (r ≈ 0.60).

### District Analysis

The districts with the highest average PM2.5 concentrations were:

* Gwanak-gu
* Mapo-gu
* Yeongdeungpo-gu

### Temporal Trends

* PM2.5 concentrations were lowest during early morning hours.
* PM2.5 concentrations peaked during evening hours.
* 2018 recorded the lowest yearly average PM2.5.
* 2019 recorded the highest yearly average PM2.5.

### Feature Importance

The most important predictor was:

* PM25_lag1 (~91.7% importance)

This indicates strong temporal dependence in PM2.5 concentrations.

---

## Model Performance

| Metric   | Score |
| -------- | ----: |
| R² Score | 0.944 |
| MAE      |  3.21 |
| RMSE     |  4.57 |

The Random Forest model demonstrated strong predictive performance for PM2.5 forecasting.

---

## Visualizations

### Correlation Heatmap

![Correlation Heatmap](images/correlation_heatmap.png)

### Monthly PM2.5 Trend

![Monthly PM2.5](images/monthly_pm25.png)

### Feature Importance

![Feature Importance](images/feature_importance.png)

### Actual vs Predicted PM2.5

![Prediction Results](images/prediction_results.png)

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

---

## Future Improvements

* Streamlit Dashboard
* PM2.5 Forecasting API
* XGBoost and LightGBM comparison
* Time-series forecasting models (Prophet, LSTM)
* Interactive geospatial visualization

---

## Author

Ishan Meshram

B.Tech Computer Science

Interested in Data Analytics, Data Science, Machine Learning, and Cloud Technologies.
