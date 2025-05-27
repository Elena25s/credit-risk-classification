
# Credit Risk Analysis Report

## Overview of the Analysis

The goal of this analysis was to build and evaluate a machine learning model that could help a financial institution assess credit risk by predicting whether a loan is **high-risk** or **healthy**. The dataset, `lending_data.csv`, contains financial information about loans, such as borrower income, debt-to-income ratio, number of accounts, and credit history.

The target variable is `loan_status`, where:
- `0` represents a **healthy loan**
- `1` represents a **high-risk loan**

The machine learning workflow included:
- Loading and preprocessing the dataset
- Splitting the data into training and testing sets
- Training a logistic regression model using `LogisticRegression` from `sklearn`
- Evaluating the model’s performance using accuracy, precision, recall, F1-score, and confusion matrix

## Results

* **Machine Learning Model 1: Logistic Regression**
  * **Accuracy Score**: 99%
  * **Precision Score**:
    * Class 0 (Healthy Loan): 1.00
    * Class 1 (High-Risk Loan): 0.84
  * **Recall Score**:
    * Class 0 (Healthy Loan): 0.99
    * Class 1 (High-Risk Loan): 0.94
  * **F1 Score**:
    * Class 0 (Healthy Loan): 1.00
    * Class 1 (High-Risk Loan): 0.89

## Summary

The logistic regression model performs exceptionally well in predicting both healthy and high-risk loans, achieving an overall accuracy of 99%. The model is highly precise when identifying healthy loans and maintains strong recall for high-risk loans, which is crucial in minimizing the number of missed high-risk cases.

Given the high recall (94%) and good precision (84%) for identifying high-risk loans, we recommend **using this logistic regression model** as a baseline tool for credit risk evaluation. Its performance is strong enough to be considered a valuable first step in an automated credit decision pipeline.

However, in future iterations, other models like Random Forest or XGBoost could be explored to see if precision for high-risk loans can be improved without sacrificing recall.
