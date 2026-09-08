
# Rossmann Store Sales Forecasting

## 📌 Project Overview
This project tackles a classic retail business problem: forecasting daily sales for over 1,000 Rossmann drug stores across Europe. Accurate sales predictions allow store managers to optimize staff schedules, manage inventory, and plan for store refurbishments up to six weeks in advance. 

**Goal:** Build a robust machine learning pipeline to predict daily sales based on historical data, promotions, seasonality, and competitor proximity.

## 📊 The Data
The dataset is sourced from the [Kaggle Rossmann Store Sales Competition](https://www.kaggle.com/c/rossmann-store-sales). 
* **Train set:** Historical daily sales data from 2013 to 2015.
* **Store features:** Store types, assortment levels, and competitor distances.
* **Time-series factors:** School holidays, state holidays, and promotional events.

*(Note: The data files are not included in this repository to keep it lightweight. See the setup instructions below to download them via the Kaggle API).*

## 🧠 Methodology
This project strictly follows a clean, modular data science workflow:
1. **Exploratory Data Analysis (EDA):** Investigating the impact of promotions, holidays, and store types on purchasing behavior.
2. **Feature Engineering:** Creating rolling averages, extracting date components (month, day of week), and handling missing competitor distances.
3. **Data Preprocessing:** Utilizing `scikit-learn` pipelines for imputation, one-hot encoding, and feature scaling.
4. **Modeling:** Training and evaluating a **Random Forest Regressor** using a chronological train/validation split to prevent data leakage in time-series forecasting.

## ⚙️ Repository Structure
```text
rossmann-sales-forecasting/
├── data/
│   ├── raw/           <- Original, immutable data dump (ignored by git)
│   └── processed/     <- Cleaned data ready for modeling (ignored by git)
├── notebooks/         <- Jupyter notebooks for EDA and experimental modeling
├── src/               <- Clean, modular Python scripts for data processing and training
├── models/            <- Pickled trained models (ignored by git)
├── requirements.txt   <- Project dependencies
└── README.md          <- The top-level project description
