# Regression Analysis of Median House Prices in California Using Python

## 1. Introduction
An accurate prediction of house prices is important for buyers, sellers, and investors to make informed decisions. The objective of this analysis is to predict median house price in California using various regression models and compare their performance.

<div style="text-align: justify">

The data pertains to the houses found in a given California district and some summary stats about them based on the [1990 California census data](https://www.kaggle.com/datasets/camnugent/california-housing-prices) downloaded from Kaggle. The data is not clean so some preprocessing steps are required. The column names are as follows:

- Independent Variable
    - longitude
    - latitude
    - housing_median_age
    - total_rooms
    - total_bedrooms
    - population
    - households
    - median_income
    - ocean_proximity

- Dependent Variable
    - median_house_value

</div>

## 2. Models Used
The following models were used for this analysis:
- Linear Regression
- Random Forest Regressor
- Gradient Boosting Regressor
- K-Neighbors Regressor
- CatBoost Regressor
- XGBoost Regressor

## 3. Model Performance Comparison
The performance of each model was evaluated using the Root Mean Squared Error (RMSE), which measures the average magnitude of the errors between the predicted and actual median house prices. The lower the RMSE, the better the model's predictions align with the actual data.

As shown in the table below, the XGBoost model achieved the lowest RMSE score of 0.21430, indicating it provides the most accurate predictions among the models evaluated. Consequently, XGBoost was chosen as the best-performing model for predicting median house prices in California.

| Model | RMSE    |
| :---   | :--- |
| Linear Regression | 0.29933   |
| Random Forest Regression | 0.22374   |
| Gradient Boosting Regression | 0.21732   |
| K-Neighbors Regressor | 0.25952   |
| CatBoost | 0.21976   |
| XGBoost | 0.21430   |

## 4. Hyperparameter Tuning
Hyperparameter tuning is performed to improve the performance of the regression models. In this project, Randomized Search Cross-Validation is used to find the best combination of hyperparameters of the XGBoost Model.

The best set of hyperparameters identified through Randomized Search CV is:
```python
{'subsample': 0.6,
 'reg_lambda': 1,
 'reg_alpha': 0,
 'n_estimators': 100,
 'max_depth': 8,
 'learning_rate': 0.1,
 'gamma': 0.1,
 'colsample_bytree': 1.0}
```

The XGBoost model was then retrained using these best hyperparameters and the performance of the tuned model was evaluated on the test data by computing the RMSE.

## 5. Visual Comparison



## 6. Residual Analysis



## 7. Conclusion



## 8. Future Work


