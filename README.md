# Credit Risk Analysis and Prediction

This project analyzes a dataset of credit card clients to predict the probability of default. It includes data exploration, feature engineering, and the development of a predictive model.

## Project Overview

The primary goal of this project is to build a model that can accurately predict whether a credit card holder will default on their payment in the next month. This is a classic binary classification problem in the financial domain, with significant implications for risk management.

## Files in this Repository

- **`CreditCardDefault.ipynb`**: A Jupyter Notebook containing the complete analysis, including data loading, preprocessing, exploratory data analysis (EDA), feature engineering, model training, and evaluation.
- **`credit-risk.pdf`**: A document that likely contains the problem statement, data dictionary, or other relevant information about the project.
- **`submission_23323005.csv`**: A sample submission file, likely from a competition or as an example of the model's output format.
- **`README.md`**: This file, providing an overview of the project.

## Analysis and Methodology

The analysis in the Jupyter Notebook (`CreditCardDefault.ipynb`) follows these key steps:

1.  **Data Loading and Initial Exploration**: The dataset is loaded, and initial checks are performed to understand its structure, data types, and identify any missing values.

2.  **Exploratory Data Analysis (EDA)**:
    -   **Target Variable Distribution**: The distribution of the `next_month_default` variable is examined to understand the class balance.
    -   **Categorical Features**: The distributions of categorical features like `sex`, `education`, and `marriage` are analyzed, both independently and in relation to the target variable.
    -   **Numerical Features**: The distributions of numerical features like `LIMIT_BAL` and `age` are explored.
    -   **Payment History**: The `pay_` columns, which represent the repayment status for the past six months, are a critical part of the analysis. Their relationship with default status is thoroughly investigated.
    -   **Bill and Payment Amounts**: The `BILL_AMT` and `PAY_AMT` columns are analyzed to understand spending and payment behaviors.

3.  **Feature Engineering**:
    -   New features are created to capture more complex patterns in the data. This includes:
        -   `repay_cv`: The coefficient of variation of repayment amounts, to measure payment consistency.
        -   `credit_util_ratio`: The ratio of average bill amount to the credit limit, to measure credit utilization.
        -   `delinquency_streak`: The longest consecutive period of payment delinquency.
        -   `repay_to_bill_ratio_avg`: The average ratio of repayment to bill amount.
        -   `repayment_trend` and `bill_trend`: The trends in repayment and bill amounts over the six-month period.
        -   `max_delay`: The maximum payment delay in months.

4.  **Data Preprocessing**:
    -   Categorical features are encoded.
    -   The data is prepared for modeling.

5.  **Modeling**:
    -   A predictive model is trained on the processed data. The notebook likely uses a classification algorithm such as Logistic Regression, Random Forest, or Gradient Boosting.

6.  **Evaluation**:
    -   The model's performance is evaluated using appropriate metrics for classification tasks, such as accuracy, precision, recall, F1-score, and the ROC AUC score.

## How to Use

To run this analysis, you will need to have Python and the following libraries installed:

-   pandas
-   numpy
-   seaborn
-   matplotlib
-   scikit-learn
-   scipy

You can then open and run the `CreditCardDefault.ipynb` notebook in a Jupyter environment.

## Conclusion

This project provides a comprehensive workflow for a credit risk modeling task. It demonstrates how to move from raw data to a predictive model, with a strong emphasis on feature engineering to improve model performance. The insights gained from the EDA and the engineered features are crucial for understanding the drivers of credit default.
