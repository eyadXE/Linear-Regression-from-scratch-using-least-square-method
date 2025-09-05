# Linear-Regression-from-scratch-using-least-square-method

# 🏠 Linear Regression from Scratch (Least Squares) on the Boston Housing Dataset

This project implements **Linear Regression from scratch** using the **Least Squares Method** to predict housing prices from the classic **Boston Housing Dataset**.  
The goal is to understand how linear regression works mathematically and evaluate its limitations when applied to real-world data.

---

## 📘 Project Overview

- Implemented **Least Squares (LSQ) Method** manually (no scikit-learn `.fit()`).
- Used **one feature at a time** to predict the median house value (`MEDV`).
- Compared the model performance using **R² score** and **error metrics**.
- Visualized predictions vs. actual values.

---

## ⚙️ Methodology

### 1. Least Squares Method
We fit a straight line:

\[
y = b_0 + b_1 x
\]

with:
\[
b_1 = \frac{\sum (x_i - \bar{x})(y_i - \bar{y})}{\sum (x_i - \bar{x})^2}, \quad
b_0 = \bar{y} - b_1 \bar{x}
\]

where:
- \( b_0 \): intercept  
- \( b_1 \): slope  
- \( (x_i, y_i) \): data points  

### 2. Dataset
The **Boston Housing Dataset** contains 506 samples and 13 features describing housing conditions in Boston suburbs.  
The target variable is `MEDV` = median home value (in \$1000s).  

Example features:
- `RM`: average number of rooms per dwelling  
- `LSTAT`: % lower status of the population  
- `CRIM`: per capita crime rate  

---

## 📊 Results

- Using only one feature, the best performance was achieved with `RM` (average number of rooms).  
- Example performance:  
  - **R² ≈ 0.54** with `RM` → meaning ~54% of variance in housing prices is explained by this single feature.  
- Predictions improve when using **multiple features**.

---

## ⚠️ Weaknesses

### LSQ with One Feature
- Oversimplifies complex relationships.  
- Assumes linearity (not always true).  
- Sensitive to outliers.  

### Boston Dataset
- **Small & outdated** (1970s).  
- **Ethical concerns** (some socioeconomic/racial bias features).  
- **Not representative** of modern housing markets.  

---

## 🚀 Future Work
- Extend to **multiple linear regression**.  
- Try **regularization** (Ridge/Lasso).  
- Compare with **non-linear models** (Decision Trees, Random Forests).  
- Replace Boston dataset with **modern, fair datasets**.

---

## 🛠️ How to Run

1. Clone the repo:
   ```bash
   git clone https://github.com/your-username/linear-regression-boston.git
   cd linear-regression-boston
