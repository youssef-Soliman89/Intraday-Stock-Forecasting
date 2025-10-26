# 📈 Intraday Stock Forecasting  
**Python | Databricks | PySpark | XGBoost | ANN | PCMCI | Alpha Vantage API**

## 🧠 Overview
This project builds a complete end-to-end data pipeline for **intraday stock price forecasting** using **1-minute and 2-minute interval data** from the **Alpha Vantage API**.  
It combines **data engineering**, **feature engineering**, and **machine learning** to evaluate how traditional rule-based strategies compare to modern ML approaches for short-term price direction prediction.

---

## ⚙️ Key Features
- **Data Ingestion:**  
  Automated extraction of 1-min and 2-min stock data (AMZN, META, MSFT, NVDA) using the Alpha Vantage API.  
  Implemented pipeline orchestration and ETL on **Databricks (PySpark)**.

- **Data Processing & Feature Engineering:**  
  - Cleaned high-frequency data and removed false signals using rolling median filters.  
  - Engineered 30+ technical indicators (MACD, ROC, RSI, Bollinger Bands, etc.).  
  - Conducted causal feature selection using **PCMCI (Tigramite)** to identify significant lagged relationships.

- **Machine Learning Models:**  
  - Trained **XGBoost** and **Artificial Neural Networks (ANN)** for intraday price direction prediction.  
  - Implemented multi-timeframe modeling (1-min, 2-min, combined) for performance comparison.  
  - Tuned hyperparameters using Keras Tuner and Scikit-learn pipelines.

- **Backtesting & Evaluation:**  
  - Automated backtesting with realistic transaction-cost adjustments.  
  - Compared performance of brute-force rule-based thresholds vs ML models.  
  - Visualized results and equity curves for multiple assets.

---

## 🏗️ Tech Stack
- **Languages:** Python (Pandas, NumPy, Scikit-learn, TensorFlow)
- **Frameworks & Tools:** Databricks, PySpark, MLflow, DBT, Git
- **APIs & Data:** Alpha Vantage API (Intraday OHLCV data)
- **Visualization:** Matplotlib, Seaborn

---

## 📊 Results Summary
| Model | Interval | Accuracy | Notes |
|--------|-----------|-----------|--------|
| XGBoost | 1-min | 52.8% | Stronger in upward prediction recall |
| ANN (with PCA) | 1-min | 55.9% | Improved balance and recall via PCA |
| XGBoost | Multi-frame | 54.4% | Better overall sensitivity to long opportunities |

Both ML models achieved modest predictive power but highlighted critical insights:  
⚡ *Feature selection and transaction cost modeling are essential in high-frequency trading.*

---
