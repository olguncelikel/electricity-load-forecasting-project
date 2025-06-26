# Electricity Load Forecasting Project

This repository contains the project code and data for forecasting **Turkiye’s hourly electricity consumption** using various models and techniques such as **LightGBM**, **XGBoost**, and **Gradient Boosting**, along with detailed **EDA**, **feature engineering**, and **model explainability** (e.g., LIME, SHAP).

---

## Objective

To develop accurate models that predict electricity demand based on:
- Temporal features (hour, day, month, weekend, holiday)
- Meteorological data (temperature)
- Population & calendar-based variables

The goal is to support better energy planning and grid management in Turkey with estimating the consumption with the lowest error possible.

---

## Models Used

- Linear Regression
- Ridge Regression
- Lasso Regression
- Elastic Net
- DecisionTreeRegressor
- Random Forest
- Gradient Boosting Regressor
- XGBoost Regressor
- LightGBM Regressor

All models were tuned using `GridSearchCV` and `RandomSearchCV`, also evaluated with:
- R² (R-squared)
- RMSE (Root Mean Squared Error)
- MAPE (Mean Absolute Percentage Error)

---

## Features

- `day`, `month`, `year`, `hour`
- `is_weekend`, `is_holiday`, `is_non_working_day`
- Temperature (°C) and population data of all the cities in Turkiye

---

## Workflow

1. **Data Cleaning & Preprocessing**
   - Missing value imputation
   - Outlier removal (via IQR method)
   - Filtering invalid records (e.g., consumption = 0)

2. **EDA**
   - Boxplots & scatterplots for outlier analysis
   - Dual-axis plots comparing temperature & load

3. **Model Training**
   - Hyperparameter tuning with `GridSearchCV` and `RandomSearchCV`
   - Comparison of unoptimized vs optimized models

4. **Model Evaluation**
   - Error metrics
   - Visual prediction checks

5. **Explainability**
   - Local explanations with LIME
   - SHAP plots (optional/coming soon)

---

## Visuals

- Load vs Temperature scatter plots  
- Hourly consumption trends over 2024  
- LIME and SHAP explanations for feature impact  
- Boxplots grouped by hour of day  

---

## Suggested Folder Structure

electricity-load-forecasting-project/
├── data
├── data_preparation.ipynb
├── models.ipynb
├── requirements.txt
└── README.md

---

## How to Run

1. Clone the repository:
```bash
git clone https://github.com/olguncelikel/electricity-load-forecasting-project.git
cd electricity-load-forecasting-project
```

2. Install required packages:
```
pip install -r requirements.txt
```

3. Open and run notebooks with Jupyter Notebook or any other IDE

---

## Author

Developed by @olguncelikel

