# Bengaluru House Price Prediction

## Overview
This project predicts house prices in Bengaluru using regression models. The workflow includes **data cleaning, feature engineering, model training, hyperparameter tuning, and evaluation**.

## What Was Done

- **Data Cleaning & Preprocessing**: Removed missing values, handled outliers, and converted categorical features (like `location`) into numerical format using one-hot encoding.
- **Feature & Target Selection**: Separated dataset into features (`X`) and target (`y`) for model training.
- **Model Training**: Trained three models:
  1. **Linear Regression (LR)** – baseline model.
  2. **Lasso Regression** – added regularization to reduce overfitting.
  3. **Decision Tree Regressor (DTR)** – captured non-linear relationships in the data.
- **Hyperparameter Tuning**: Used **GridSearchCV** to find the best parameters for Lasso and Decision Tree models.
- **Evaluation**: Compared models using **R², MAE, and RMSE** to determine prediction accuracy.

## Results

| Model                   | R² Score  | Best Parameters                                         |
|-------------------------|-----------|--------------------------------------------------------|
| Linear Regression (LR)  | 0.895912  | {'fit_intercept': True}                                |
| Lasso Regression        | 0.895939  | {'alpha': 0.001, 'max_iter': 1000}                    |
| Decision Tree Regressor | 0.860577  | {'max_depth': 20, 'min_samples_leaf': 1, ...}        |

- **Linear Regression** provided a solid baseline prediction.
- **Lasso Regression** slightly improved the R² while reducing overfitting.
- **Decision Tree Regressor** captured non-linear relationships but had slightly lower generalization.

## Future Work

- Explore ensemble methods like **Random Forest** or **XGBoost** for higher accuracy.
- Include additional features such as proximity to key locations or amenities.
- Deploy a **web application** for interactive price predictions.
