# Data-Driven-Modeling-of-Urban-Air-Quality-AQI-Using-Integrated-Machine-Learning-
Data-Driven Modeling of Urban Air Quality (PM2.5) Using Machine Learning

-Project Overview:

Air pollution is a major public health concern, with PM2.5 (fine particulate matter) being one of the most harmful pollutants due to its ability to penetrate deep into the respiratory system. This project develops a data-driven machine learning framework to forecast daily PM2.5 concentrations in London, supporting proactive air quality monitoring and public health decision-making.

Using 12.5 years of daily air quality data (2013–2025) obtained from the Open-Meteo Air Quality API, this study compares sequential deep learning and traditional machine learning models under rigorous time-series validation.

- Objectives:

Collect and preprocess long-term London air quality data (2013–2025)

Apply temporal train–test splitting to prevent data leakage

-Develop and compare:

LSTM (Long Short-Term Memory) networks

XGBoost regression models

Support Vector Regression (SVR)

Evaluate models using RMSE, MAE, MAPE, and R²

Generate future PM2.5 forecasts (2026–2030)

Provide insights into model performance, interpretability, and limitations

-Dataset:

Source: Open-Meteo Air Quality API (CAMS – Copernicus Atmosphere Monitoring Service)

Location: London, United Kingdom

Period: April 2013 – September 2025

Frequency: Daily averages

Pollutants: PM10, PM2.5, CO, NO₂, SO₂, O₃, Dust

Target Variable: PM2.5 (µg/m³)

The dataset contains 4,566 observations and is publicly available, anonymized, and ethically compliant.

-Models Implemented:
1. LSTM (Deep Learning – Sequential Model)

Bidirectional LSTM architecture

30-day lookback window

Early stopping and learning rate scheduling

Captures temporal autocorrelation directly from sequences

2. XGBoost (Feature-Based Ensemble Model)

Time-based feature engineering (day, week, month, year, etc.)

Hyperparameter optimization using RandomizedSearchCV

Feature importance analysis for interpretability

3. Support Vector Regression (SVR)

RBF kernel for nonlinear regression

Feature scaling using StandardScaler

Hyperparameter tuning with GridSearchCV

 -Evaluation Metrics:

Models are evaluated on a future test set (2022–2025) using:

RMSE – Penalizes large prediction errors

MAE – Average absolute error

MAPE – Percentage-based error

R² – Explained variance

- Results:
Model	RMSE (µg/m³)	MAE (µg/m³)	R²
LSTM	4.03	2.93	0.50
XGBoost	5.58	4.15	0.06
SVR	5.93	3.80	-0.06

 LSTM outperformed traditional models, achieving 27.8% lower RMSE than XGBoost and capturing meaningful temporal dynamics essential for air quality forecasting.

 Future Forecasting (2026–2030)

Short-term forecasts (1–2 years) show realistic seasonal behavior

Long-term forecasts (3–5 years) reveal increasing uncertainty

Highlights the need for periodic model retraining in operational systems


-Technologies Used:

Python

NumPy, Pandas

Matplotlib, Seaborn

Scikit-learn

TensorFlow / Keras

XGBoost
