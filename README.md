# LSTM-Based Air Temperature Prediction: Deep Learning Project

![Python](https://img.shields.io/badge/language-Python-blue)
![Jupyter Notebook](https://img.shields.io/badge/output-Jupyter%20Notebook-orange)

## Overview
This repository contains a **temperature prediction project using LSTM**.  
The project is developed as a **final project for the Deep Learning course**.  

Dataset contains air quality and environmental features including air temperature (AT) for time series prediction. After preprocessing, windowing, and scaling, baseline and modified LSTM models are trained to predict AT.

---

## Repository Structure

- `AP004.csv` → raw dataset containing air quality and environmental variables  
- `LSTM_AirQuality.ipynb` → main notebook containing EDA, data preprocessing, model training, and evaluation

---

## Methodology

1. **Exploratory Data Analysis (EDA)**
   - Descriptive statistics, missing value analysis, boxplots, histograms
   - Correlation matrix to identify features most related to air temperature

2. **Data Preprocessing**
   - Drop redundant columns and rows with NaN target
   - Drop columns with >50% missing values
   - Forward fill & backward fill missing values
   - Scale features using `RobustScaler`
   - Time series windowing (window size = 5)

3. **Model Training**
   - **Baseline LSTM:** 10 hidden units, 25 epochs, batch size 32
   - **Modified LSTM:** Added Dropout(0.1), EarlyStopping, increased epochs to 50

4. **Evaluation**
   - Metrics: MAE, MSE, R²
   - Compared baseline vs modified model performance
   - Visualization of predicted vs actual air temperature

---

## Key Insights

- Baseline model achieves **MAE 0.096, MSE 0.0176, R² 0.918**  
- Modified model improves performance to **MAE 0.0873, MSE 0.0147, R² 0.9318**  
- Dropout and EarlyStopping enhanced generalization and stability  
- Modified LSTM captures temporal patterns in air temperature more accurately  

---

## Presentation Video
[LSTM Air Temperature Prediction – Video Presentation](https://drive.google.com/file/d/1EVIqaG9C8k7nvYFEymbF_acKaqDdPpAe/view?usp=sharing)

---

## References
- Python libraries: pandas, numpy, matplotlib, seaborn, scikit-learn, tensorflow.keras

---

## Author

Syalista Galuh Nadira
