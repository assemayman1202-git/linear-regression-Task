# data analysis , second level (1st task) linear-regression-Task
Data on notebook : 
https://colab.research.google.com/drive/1wNCcN6yVsJHQ46zQ6sZGigyGG3nMF4li?usp=sharing

# 🚗 Car Price Prediction — Linear Regression Model

A machine learning project that predicts used car prices 
using Linear Regression, built with Python and scikit-learn.

## 📂 Dataset Description

The dataset contains **4,345 records** of used cars with the following features:

| Column | Type | Description |
|---|---|---|
| Brand | Categorical | Car manufacturer (BMW, Audi, Toyota...) |
| Price | Numerical | Car price in USD — Target Variable (Y) |
| Body | Categorical | Car body type (sedan, crossover, van...) |
| Mileage | Numerical | Distance driven in thousands of km |
| EngineV | Numerical | Engine size in liters |
| Engine Type | Categorical | Fuel type (Petrol, Diesel, Gas) |
| Registration | Categorical | Whether the car is registered (yes/no) |
| Year | Numerical | Year of manufacture |
| Model | Categorical | Car model name |

---

## 🔧 Project Steps

1. **Data Exploration** — Understanding variables and distributions
2. **Outlier Detection** — Using Boxplots to identify abnormal values
3. **Data Cleaning** — Removing outliers and missing values
4. **Visualization** — Scatter plots to explore relationships
5. **Model Building** — Linear Regression with Train/Test Split
6. **Model Evaluation** — R² Score and Mean Squared Error (MSE)

---

## 📊 Model Results with one-variable

| Metric | Training | Test |
|---|---|---|
| R² Score | 0.2922 | 0.299 |
| MSE | 1.339423e+08  | 1.220285e+08 |


Price = 28,836 + (-78 × Mileage)
Every 1,000 km increase = Price drops by $78




## 📊 Model Results with +2 variables
| Metric | Training | Test |
|---|---|---|
| R² Score | 0.558 | 0.587 |
| MSE | 8.438813e+07 | 8.667456e+07 |

R² = 0.57 — The model successfully explains 57% of the variation in used car prices using only 3 features (Mileage, EngineV, Year).
Train ≈ Test (difference of 0.03) — The model generalizes well to unseen data with no signs of Overfitting, meaning it learned patterns rather than memorizing the training data.
High MSE — The average prediction error is roughly $9,000, which is expected given the wide price range in the dataset ($600 — $75,000)

Limitations & Future Improvements:
R² of 0.57 leaves 43% unexplained — adding categorical features like Brand, Body Type, and Engine Type could push R² above 0.75+
Linear Regression assumes a straight-line relationship, which may not fully capture real-world pricing complexity
A more advanced model like Random Forest or XGBoost would likely yield better results

---

## 🧮 Model Equation
```
Price = Intercept + (Coef_Mileage × Mileage)  + (Coef_EngineV × EngineV)  + (Coef_Year × Year)


## ⚙️ Technologies Used

- Python 3
- Pandas
- NumPy
- Matplotlib
- Scikit-learn

---


## 📁 Project Structure
```
car-price-prediction/
│
├── data/
│   └── Real-life_example.csv
├── notebook/
│   └── linear_regression_model.ipynb
└── README.md
```
