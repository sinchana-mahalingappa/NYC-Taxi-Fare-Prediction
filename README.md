# 🗽 NYC Taxi Fare Prediction using Machine Learning

### 📌 Project Overview
This project predicts taxi fares for New York City trips using machine-learning regression models.  
The dataset contains trip details such as pickup/drop-off coordinates, date-time, and passenger count.  
The goal is to understand what factors drive fare amounts and to build a model that can accurately estimate prices.

---

### 🎯 Objectives
- Clean and preprocess real-world NYC taxi trip data  
- Engineer meaningful features like trip distance and time-based variables  
- Train, evaluate, and compare multiple regression models  
- Identify the most influential features affecting taxi fares  

---

### 🧠 Tools & Libraries
- **Python**  
- **Pandas, NumPy** — data manipulation  
- **Matplotlib** — data visualization  
- **Scikit-learn** — model training and evaluation  
- **Google Colab** — execution environment  

---

### 📊 Dataset
- Source: [Kaggle – New York City Taxi Fare Prediction](https://www.kaggle.com/c/new-york-city-taxi-fare-prediction)
- Rows used: ~48 k after cleaning  
- Features: pickup/dropoff coordinates, date-time, passenger count, fare amount  

---

### 🔧 Data Preprocessing
- Removed negative or unrealistic fare values  
- Filtered out invalid coordinates (outside NYC region)  
- Created new features:
  - `distance_km` — Haversine distance between pickup and drop-off points  
  - `hour`, `weekday`, `month`, `year` — extracted from pickup time  

---

### 🤖 Models & Performance

| Model | MAE ↓ | RMSE ↓ | Comment |
|--------|--------|--------|----------|
| **Linear Regression** | 2.33 | 4.64 | Simple baseline model |
| **Random Forest Regressor** | **1.99** | **3.92** | Better accuracy, captures nonlinear patterns |

---

### 🌲 Feature Importance
| Feature | Importance |
|----------|-------------|
| distance_km | 0.918 |
| year | 0.027 |
| hour | 0.024 |
| month | 0.015 |
| weekday | 0.012 |
| passenger_count | 0.005 |

> **Insight:** Trip distance overwhelmingly determines fare price (≈ 92 % importance).  
> Temporal variables such as hour and month contribute modestly.

---

### 🧾 Key Results
- Achieved **MAE = 1.99** and **RMSE = 3.92** using Random Forest  
- Model predicts fares within ± $2 for most trips  
- Demonstrated full pipeline: data cleaning → feature engineering → model evaluation → insight visualization  

---

### 📂 Folder Structure
NYC-Taxi-Fare-Prediction/
│
├── NYC_Taxi_Fare_Prediction.ipynb   # Google Colab notebook
├── README.md                        # Project documentation 
└── taxi_rf_model.joblib             # Saved Random Forest model 


