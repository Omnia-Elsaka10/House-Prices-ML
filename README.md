# 🏠 Advanced House Price Prediction

Machine Learning project predicting house sale prices using the Ames Housing dataset from Kaggle.

## 📊 Project Overview

This project builds a regression pipeline to estimate house prices based on 79 housing features.  
The workflow focuses on data cleaning, feature engineering, and model blending to improve prediction accuracy.

Dataset source:
Kaggle – House Prices: Advanced Regression Techniques

---

## 🔍 Machine Learning Pipeline

### 1. Exploratory Data Analysis & Data Cleaning
- Handled missing values using feature-specific strategies  
- Example: `LotFrontage` filled using the **median value of each neighborhood**
- Outliers capped using **Winsorization**
- Target variable `SalePrice` transformed using **log transformation** to normalize distribution

### 2. Feature Engineering
Several additional features were created to improve model performance:

- **TotalSF** → Total house area (basement + 1st floor + 2nd floor)
- **HouseAge** → Years since construction
- **RemodAge** → Years since last remodeling

Categorical variables were encoded using **One-Hot Encoding** with proper train/test alignment.

---

## 🤖 Models Used

The final prediction uses a **blended ensemble model**:

- **Lasso Regression**
  - Performs feature selection using L1 regularization

- **XGBoost Regressor**
  - Captures non-linear relationships between features

The final prediction is a weighted combination of both models.

---

## 📈 Model Performance

Evaluation Metric: **RMSE (Root Mean Squared Error)** on log-transformed prices.

Final Score:

RMSE ≈ **0.128**

---


## 🚀 How to Run

```bash
git clone https://github.com/YourUsername/House-Prices-Advanced-Regression
pip install -r requirements.txt
