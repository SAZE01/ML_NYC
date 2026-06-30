# 🚕 NYC Taxi Trip Duration — Machine Learning Project

> Predicting and classifying NYC taxi trip durations using Regression & Classification models.

---

## 📌 Project Overview

This project analyzes hundreds of thousands of NYC taxi trips and builds Machine Learning models to **predict the duration of a trip** (in seconds) based on GPS coordinates, time, and passenger data.

- **Dataset**: [NYC Taxi Trip Duration — Kaggle](https://www.kaggle.com/c/nyc-taxi-trip-duration)
- **Type**: Regression & Binary Classification
- **Year**: 2025 / 2026

---

## 🎯 Objectives

- Explore and understand the data (EDA)
- Clean and prepare data for modeling
- Engineer new useful features
- Build and evaluate Regression and Classification models
- Optimize performance with Grid Search & Cross-Validation

---

## 📊 Main Variables

| Variable | Type | Description | Role |
|---|---|---|---|
| `trip_duration` | Numeric | Trip duration (seconds) | Target (regression) |
| `distance_km` | Numeric | Haversine distance | Key feature |
| `pickup_hour` | Numeric | Departure hour (0–23) | Temporal feature |
| `pickup_month` | Numeric | Departure month (1–12) | Temporal feature |
| `passenger_count` | Numeric | Number of passengers | Feature |
| `vendor_id` | Category | Vendor identifier | Feature |

---

## 🛠️ Tools & Libraries

![Python](https://img.shields.io/badge/Python-3.x-blue)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange)
![pandas](https://img.shields.io/badge/pandas-Data-green)
![matplotlib](https://img.shields.io/badge/matplotlib-Viz-red)

- **Python**
- **scikit-learn** — ML models
- **pandas** — Data manipulation
- **matplotlib** — Data visualization

---

## 📁 Project Structure

```
ML_NYC/
│
├── ML_NYC.ipynb       # Main notebook — full ML pipeline
├── NYC.ipynb          # Exploratory analysis notebook
└── README.md
```

---

## 🤖 Models & Results

### Regression

| Model | MAE | RMSE | R² |
|---|---|---|---|
| Linear Regression | ~220 sec (3.7 min) | ~310 sec | ~0.55 |
| **Random Forest** | **~155 sec (2.6 min)** | **~225 sec** | **~0.73** |

### Classification (Short vs Long trip)

| Model | Accuracy | F1 Short | F1 Long |
|---|---|---|---|
| Logistic Regression | ~0.62 | ~0.67 | ~0.65 |
| **Random Forest** | **~0.79** | **~0.80** | **~0.78** |
| SVM (RBF) | ~0.75 | ~0.77 | ~0.76 |

✅ **Best model: Random Forest** — outperforms all others on both tasks.

---

## 🔍 Key Findings

- **Distance (Haversine)** is the most predictive variable (correlation > 0.7)
- **Log transformation** improves modeling and reduces outlier impact
- **Random Forest** outperforms Linear Regression and SVM
- **5-fold Cross-Validation** confirms model stability: R² ≈ 0.72 ± 0.02

---

## 🚀 How to Run

```bash
# 1. Clone the repo
git clone https://github.com/SAZE01/ML_NYC.git
cd ML_NYC

# 2. Create a virtual environment
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows

# 3. Install dependencies
pip install pandas scikit-learn matplotlib jupyter

# 4. Launch Jupyter
jupyter notebook
```

---

## 🔮 Future Perspectives

- Integration of weather data
- Deployment via Flask / FastAPI
- Testing advanced models (XGBoost, LightGBM)

---

*Project completed as part of a Data Science & Machine Learning training program.*
