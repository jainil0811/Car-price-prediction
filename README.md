# Car-price-prediction
# 🚗 Car Price Prediction

A machine learning project to predict the selling price of a used car based on its features like age, fuel type, engine power, and kilometers driven.

---

## 📌 Problem Statement

The used car market in India is huge — platforms like CarDekho, OLX, and Cars24 deal with thousands of listings daily. The goal of this project is to build a machine learning model that can accurately predict the selling price of a used car based on its specifications.

---

## 📊 Dataset

- **Source:** CarDekho Dataset
- **Records:** 8,000+ used cars
- **Features:**

| Feature | Description |
|---|---|
| name | Car model name |
| year | Year of manufacture |
| selling_price | Price at which car is sold (Target) |
| km_driven | Total kilometers driven |
| fuel | Fuel type (Petrol/Diesel/CNG) |
| seller_type | Individual / Dealer / Trustmark |
| transmission | Manual / Automatic |
| owner | First / Second / Third Owner |
| mileage | Fuel efficiency (km/ltr) |
| engine | Engine displacement (CC) |
| max_power | Maximum power (bhp) |
| seats | Number of seats |

---

## 🛠️ Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Joblib

---

## ⚙️ ML Models Used

| Model | Type |
|---|---|
| Linear Regression | Baseline model |
| Decision Tree Regressor | Tree based model |
| Random Forest Regressor | Ensemble model (Best) |

---

## 📈 Project Workflow

1. **Data Loading** — Loaded CarDekho dataset using Pandas
2. **Exploratory Data Analysis** — Checked shape, info, null values, duplicates
3. **Data Cleaning** — Removed nulls, duplicates, extracted numeric values from max_power column
4. **Feature Engineering** — Created `car_age` from manufacturing year
5. **Label Encoding** — Converted categorical columns (fuel, seller_type, transmission, owner) to numeric
6. **Train-Test Split** — 80% training, 20% testing
7. **Model Training** — Trained and compared 3 ML models
8. **Model Evaluation** — Compared R2 Score and MAE across all models
9. **Feature Importance** — Identified top features affecting car price
10. **Prediction Function** — Built function to predict price of any car
11. **Model Saving** — Saved final model using Joblib

---

## 📉 Model Comparison

| Model | R2 Score | MAE |
|---|---|---|
| Linear Regression | ~0.67 | Higher |
| Decision Tree | ~0.83 | Medium |
| **Random Forest** | **~0.92** | **Lowest** |

> Random Forest was selected as the final model based on highest R2 Score and lowest MAE.

---

## 🔑 Top Features (by Importance)

- max_power
- engine
- car_age
- km_driven
- mileage

---

## 🔮 Prediction Function

```python
predict_car_price(
    km_driven    = 45000,
    fuel         = 1,
    seller_type  = 1,
    transmission = 1,
    owner        = 0,
    mileage      = 23.4,
    engine       = 1248,
    max_power    = 74,
    seats        = 5,
    car_age      = 7
)
# Output: Estimated Car Price: ₹ 4,50,000
```

---

## 💾 Model Saving

```python
import joblib

# Save
joblib.dump(rf, 'car_price_model.pkl')

# Load
model = joblib.load('car_price_model.pkl')
```

---

## 👤 Author

**Jainil Jigarkumar Prajapati**
B.E. Computer Engineering | Sem 6
Government Engineering College, Gandhinagar
GTU | CGPA: 8.35

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://www.linkedin.com/in/gecgce2023jainilprajapati)
[![GitHub](https://img.shields.io/badge/GitHub-Profile-black)](https://github.com/jainil0811)
