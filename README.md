# Project Report: Credit Score Prediction

## Introduction

This project aims to predict credit scores based on various financial and personal attributes of individuals. The dataset used for this project contains information on income, savings, debt, and other financial behaviors, along with categorical variables such as gambling habits, debt status, and credit card usage. The target variable is the credit score, which is a numerical value indicating an individual's creditworthiness.

## Data Preparation

The dataset was initially loaded from a CSV file located at `C:\Users\user\Desktop\Spreadsheets\credit_score.csv`. The data was then processed to ensure consistency and readiness for analysis. The following steps were taken:

1. **Column Renaming**: All column names were stripped of leading and trailing spaces and converted to lowercase to ensure uniformity and ease of reference.
2. **Data Inspection**: The dataset was inspected to understand its structure, including the columns, the first five rows, the number of rows and columns, and the data types of each column.
3. **Missing Value Check**: The dataset was checked for missing values. No missing values were detected across any of the columns.
4. **Duplicate Rows Check**: The dataset was checked for duplicate rows. No duplicate rows were found.
5. **Unique Values Count**: The number of unique values in each variable was counted to understand the diversity of the data.

## Data Splitting

The dataset was split into features (X) and the target variable (credit score, Y). The features included all columns except for 'credit_score', 'cust_id', and 'cat_gambling'. The target variable was the 'credit_score' column.

## Data Preprocessing

The data was preprocessed using a pipeline that included imputation and scaling for both numerical and categorical variables. The numerical variables were scaled using the StandardScaler, while the categorical variables were encoded using the OrdinalEncoder. The imputation strategy for numerical variables was the mean, and for categorical variables, the most frequent category was used.

## Model Training

The dataset was split into training and testing sets, with 75% of the data used for training and 25% for testing. The following models were evaluated for their performance in predicting credit scores:

- Linear Regression (LR)
- Random Forest Regressor (RF)
- Decision Tree Regressor (TREE)
- K-Nearest Neighbors Regressor (KN)
- XGBoost Regressor (xgb)

Each model was trained on the training set and evaluated on the testing set using Mean Absolute Error (MAE) and Mean Absolute Percentage Error (MAPE) as performance metrics.

## Results

The performance of the models was evaluated based on the MAE and MAPE metrics. The results are as follows:

- **Linear Regression (LR)**: MAE = 21.92, MAPE = 0.0381
- **Random Forest Regressor (RF)**: MAE = 21.72, MAPE = 0.0376
- **Decision Tree Regressor (TREE)**: MAE = 31.77, MAPE = 0.0552
- **K-Nearest Neighbors Regressor (KN)**: MAE = 34.77, MAPE = 0.0626
- **XGBoost Regressor (xgb)**: MAE = 23.35, MAPE = 0.0404

## Conclusion

The project successfully demonstrated the process of predicting credit scores using various machine learning models. The XGBoost Regressor showed the best performance in terms of both MAE and MAPE, indicating its effectiveness in predicting credit scores based on the given dataset. This model could be further refined and validated using additional data or through cross-validation techniques to improve its predictive accuracy.
