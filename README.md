# Predicting Household Energy Consumption

## Problem 
The goal of this project is to predict **energy consumption of household appliances** (`Energy_Consumption`) based on environmental and household conditions such as temperature, humidity, and weather data. This is formulated as a **regression task** to support better resource management.

## Dataset

### Sources
1. **Household Data**:
   - Collected over 4.5 months (January 11 to May 27, 2016) using IoT devices.
   - Recorded at 10-minute intervals for energy consumption, temperature, and humidity in various rooms.
2. **Weather Data**:
   - Hourly weather data from Chievres Airport (Belgium), interpolated to 10-minute intervals.
   - Dataset available at the UCI Machine Learning Repository:  
     [Appliances Energy Prediction Dataset](https://archive.ics.uci.edu/dataset/374/appliances+energy+prediction)
### Features
The dataset contains the following:
- **Target Variable**: `Energy_Consumption` (Wh), representing the energy consumption of household appliances.
- **Environmental Features**: Temperature, humidity, wind speed, visibility, and pressure.
- **Temporal Features**: Hour, day of the week, cyclical encodings for periodic patterns.
- **Indoor Conditions**: Room-specific temperature and humidity data.
- **Outdoor Conditions**: Weather station data merged with IoT sensor readings.

## Models and Results

### Models
The following machine learning models were trained and evaluated:
1. **Ridge Regression**: Linear model with L2 regularization.
2. **Random Forest**: Tree-based ensemble model capturing non-linear patterns.
3. **XGBoost**: Gradient boosting framework optimized for accuracy and efficiency.

### Results
- **Best Model**: Random Forest
  - Test RMSE: **40.0705 Wh**
  - Test R²: **0.8039**
- **Baseline RMSE**: **90.4786 Wh**
- Feature engineering, including lagged consumption and rolling statistics, significantly improved model performance.