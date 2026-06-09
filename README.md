# 🌍 Seoul Air Pollution Analysis & PM2.5 Forecasting

## 📌 Project Overview

Air pollution is a major environmental and public health challenge in urban areas. Fine particulate matter (**PM2.5**) is particularly dangerous because it can penetrate deep into the lungs and bloodstream, increasing the risk of respiratory and cardiovascular diseases.

This project analyzes air quality data collected from monitoring stations across **Seoul, South Korea**, and develops machine learning models to forecast PM2.5 concentrations. The project combines data cleaning, exploratory data analysis, feature engineering, and predictive modeling to uncover pollution patterns and improve air quality forecasting.

---

## 🎯 Objectives

- Analyze air pollution trends across Seoul districts.
- Study relationships among major pollutants.
- Identify temporal pollution patterns.
- Forecast PM2.5 concentrations using machine learning.
- Compare Random Forest and XGBoost models.

---

## 📂 Dataset Description

The project uses three datasets:

### 1. Measurement Information
Contains:
- Pollutant measurements
- Observation timestamps
- Monitoring station IDs

### 2. Item Information
Contains:
- Pollutant metadata
- Units of measurement
- Air quality thresholds

### 3. Station Information
Contains:
- District names
- Latitude and Longitude
- Monitoring station details

---

## 🏭 Pollutants Analyzed

| Pollutant | Description |
|------------|------------|
| SO₂ | Sulfur Dioxide |
| NO₂ | Nitrogen Dioxide |
| CO | Carbon Monoxide |
| O₃ | Ozone |
| PM10 | Particulate Matter ≤ 10 µm |
| PM2.5 | Particulate Matter ≤ 2.5 µm |

---

## ⚙️ Project Workflow

### Data Integration
- Merged Measurement, Item, and Station datasets into a unified analytical dataset.

### Data Cleaning
- Removed invalid measurements.
- Handled missing values.
- Standardized timestamps and pollutant records.

### Exploratory Data Analysis (EDA)
- Correlation Analysis
- District-wise Pollution Analysis
- Monthly Trend Analysis
- Hourly Trend Analysis
- Yearly Trend Analysis

### Feature Engineering
Created the following features:

- Year
- Month
- Day
- Hour
- DayOfWeek
- PM25_lag1
- PM25_lag24

These lag features help capture temporal dependencies in PM2.5 concentrations.

---

## 🤖 Machine Learning Models

### Random Forest Regressor

Random Forest was used as the baseline machine learning model for PM2.5 prediction.

#### Performance

| Metric | Score |
|---------|---------:|
| MAE | 3.21 |
| RMSE | 4.57 |
| R² | 0.944 |

---

### XGBoost Regressor

XGBoost was implemented to improve predictive performance through gradient boosting and advanced ensemble learning techniques.

#### Hyperparameters

```python
XGBRegressor(
    n_estimators=300,
    learning_rate=0.05,
    max_depth=6,
    subsample=0.8,
    colsample_bytree=0.8,
    random_state=42
)
```

#### Performance

| Metric | Score |
|---------|---------:|
| MAE | YOUR_XGB_MAE |
| RMSE | YOUR_XGB_RMSE |
| R² | YOUR_XGB_R2 |

---

## 📊 Model Comparison

| Model | RMSE | R² Score |
|---------|---------:|---------:|
| Random Forest | 4.57 | 0.944 |
| XGBoost | YOUR_XGB_RMSE | YOUR_XGB_R2 |

**Best Model:** Update this section after running XGBoost and comparing results.

---

## 🔍 Key Findings

### Pollutant Relationships

- PM10 exhibited the strongest positive correlation with PM2.5.
- CO showed a moderate positive correlation with PM2.5.
- Pollutant concentrations demonstrated strong interdependencies.

### District-Level Analysis

Several districts consistently recorded higher PM2.5 concentrations than others, indicating localized pollution hotspots.

### Temporal Trends

- PM2.5 levels were generally lowest during early morning hours.
- Pollution concentrations increased during evening periods.
- Significant seasonal and yearly variations were observed.

### Feature Importance

The most influential feature for PM2.5 prediction was:

- PM25_lag1

This highlights the strong temporal dependence of PM2.5 concentrations.

---

## 📈 Visualizations

### Correlation Heatmap

![Correlation Heatmap](images/correlation_heatmap.png)

### Monthly PM2.5 Trend

![Monthly PM2.5 Trend](images/monthly_pm25.png)

### Feature Importance

![Feature Importance](images/feature_importance.png)

### Actual vs Predicted PM2.5

![Prediction Results](images/prediction_results.png)

---

## 🛠️ Tech Stack

### Programming Language
- Python

### Data Analysis
- Pandas
- NumPy

### Data Visualization
- Matplotlib
- Seaborn

### Machine Learning
- Scikit-Learn
- XGBoost

### Development Environment
- Jupyter Notebook

---

## 📁 Project Structure

```text
Seoul-Air-Pollution-Analysis/
│
├── data/
│
├── notebooks/
│   └── Seoul_Air_Pollution.ipynb
│
├── images/
│   ├── correlation_heatmap.png
│   ├── feature_importance.png
│   ├── monthly_pm25.png
│   └── prediction_results.png
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

## 🚀 Future Improvements

- Interactive Streamlit Dashboard
- Pollution Hotspot Mapping using Latitude and Longitude
- Weather Data Integration
- Time-Series Cross Validation
- Prophet Forecasting
- LSTM-Based Forecasting
- Real-Time PM2.5 Prediction API

---

## 💡 Business Impact

Accurate PM2.5 forecasting can support:

- Environmental policy planning
- Public health advisory systems
- Smart city initiatives
- Air quality monitoring and decision-making

---

## 👨‍💻 Author

**Ishan Meshram**

B.Tech Computer Science

Interested in:
- Data Analytics
- Data Science
- Machine Learning
- Artificial Intelligence
- Cloud Computing
