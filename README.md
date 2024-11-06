Here's a detailed `README.md` for your Aircraft Engine Predictive Maintenance project:

---

# Aircraft Engine Health Analysis for Predictive Maintenance

## Overview
This project focuses on predicting the remaining useful life (RUL) of aircraft engines based on sensor and operational data. The goal is to analyze time series data from multiple sources, clean and preprocess the data, and build machine learning models that estimate how long an engine can operate before requiring maintenance. This predictive maintenance approach is essential to reduce costs, improve safety, and prevent unexpected engine failures.

## Features
- **Data Collection**: Gathered data from multiple sources with over 20 sensor readings and operational settings.
- **Exploratory Data Analysis (EDA)**: Conducted in-depth analysis to understand data distributions, identify patterns, and detect anomalies.
- **Data Cleaning and Transformation**: Filled missing values, calculated rolling averages, and engineered additional features like RUL values for each unit.
- **Model Development**: Built and evaluated machine learning models, including Random Forest and Gradient Boosting, for RUL prediction.
- **Evaluation Metrics**: Used Mean Absolute Error (MAE), Mean Squared Error (MSE), and R² Score to assess model accuracy.

## Technologies Used
- **Programming Language**: Python
- **Libraries**:
  - `pandas`, `numpy` for data manipulation
  - `matplotlib`, `seaborn` for data visualization
  - `scikit-learn` for machine learning

## Data Description
The data consists of the following features:
- **unit_number**: Unique identifier for each engine unit
- **time_in_cycles**: Operational time of the engine in cycles
- **operational_setting_1, 2, 3**: Operational settings for the engine
- **sensor_reading_1 - sensor_reading_21**: Sensor readings capturing various aspects of the engine's performance

Additionally, the **RUL** (Remaining Useful Life) column indicates the number of cycles left for each engine at a given time point.

## Key Steps
### 1. Data Preprocessing
- **Normalization**: Scaled numerical features to improve model performance.
- **Feature Engineering**: Calculated rolling averages of sensor readings to capture short-term trends and added the RUL values for training.

### 2. Exploratory Data Analysis (EDA)
Analyzed sensor and operational data to uncover trends and potential indicators of engine health:
- Distribution of each sensor reading across engine units
- Rolling averages to understand trends in sensor readings over time
- Unique units in the dataset and the maximum cycles for each unit

### 3. Model Development
- **Random Forest Regressor** and **Gradient Boosting Regressor** were trained on historical engine data to predict RUL.
- **Train-Test Split**: Split the dataset into training and testing sets (80-20 split).
- **Evaluation**: Models were evaluated on MAE, MSE, and R² Score to ensure accurate RUL predictions.

### 4. Model Evaluation
- **Mean Squared Error (MSE)**: Measures the average squared difference between predicted and actual values.
- **Mean Absolute Error (MAE)**: Provides the average magnitude of errors in predictions.
- **R² Score**: Indicates the proportion of variance explained by the model.

## Results
The best model achieved the following performance metrics:
- **Mean Squared Error (MSE)**: 0.4707834391721695
- **Mean Absolute Error (MAE)**: 0.5121738698069621
- **R² Score**:  0.9999250731232194

## Conclusion
This project demonstrates a robust approach to predicting the remaining useful life of aircraft engines using time series analysis and machine learning. By analyzing engine data and predicting maintenance needs, it is possible to enhance safety, reduce costs, and optimize engine utilization.