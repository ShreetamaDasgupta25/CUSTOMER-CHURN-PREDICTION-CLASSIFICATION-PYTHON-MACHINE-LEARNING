## 📌 Project Overview

1. A telecommunications company providing home phone and Internet services wanted to better understand customer churn. The dataset contains information on 7,043 customers in California, including their demographics, subscribed services, contract details, tenure, and billing information.

| Feature | Description |
|---|---|
| `customerID` | Unique identifier for each customer. |
| `gender` | Gender of the customer. |
| `SeniorCitizen` | Indicates whether the customer is a senior citizen (`0` = No, `1` = Yes). |
| `Partner` | Indicates whether the customer has a partner. |
| `Dependents` | Indicates whether the customer has dependents. |
| `tenure` | Number of months the customer has been with the company. |
| `PhoneService` | Indicates whether the customer has phone service. |
| `MultipleLines` | Indicates whether the customer has multiple phone lines. |
| `InternetService` | Type of Internet service subscribed to by the customer. |
| `OnlineSecurity` | Indicates whether the customer has online security service. |
| `OnlineBackup` | Indicates whether the customer has online backup service. |
| `DeviceProtection` | Indicates whether the customer has device protection service. |
| `TechSupport` | Indicates whether the customer has technical support service. |
| `StreamingTV` | Indicates whether the customer has streaming TV service. |
| `StreamingMovies` | Indicates whether the customer has streaming movie service. |
| `Contract` | Type of customer contract. |
| `PaperlessBilling` | Indicates whether the customer uses paperless billing. |
| `PaymentMethod` | Payment method used by the customer. |
| `MonthlyCharges` | Monthly amount charged to the customer. |
| `TotalCharges` | Total amount charged to the customer. |
| `Churn` | Indicates whether the customer left the company (`Yes`/`No`). |

2. The objective of this project is to analyze customer behavior, identify factors associated with churn, and develop a machine learning classification model to predict whether a customer was likely to leave the company.

3. An end-to-end machine learning workflow was implemented, beginning with **data cleaning and exploratory data analysis (EDA)** to understand customer characteristics, identify patterns, and examine factors associated with churn. The data was then prepared for modelling through **feature preprocessing, categorical variable encoding, and numerical feature scaling**. Since the target variable was imbalanced, **SMOTE (Synthetic Minority Over-sampling Technique)** was applied to the training data to improve the representation of the minority churn class. Multiple classification algorithms, including **Logistic Regression, Decision Tree, Random Forest, and XGBoost**, were evaluated using classification metrics such as **accuracy, precision, recall, and F1-score**.
Based on the modelling results, **Logistic Regression with SMOTE** was selected for further development. **GridSearchCV with 5-fold cross-validation** was then used with **recall** used as the primary scoring metric to focus on identifying customers at risk of churn.
Finally, an end-to-end **Scikit-learn/imbalanced-learn pipeline** was developed to integrate preprocessing, SMOTE, and the Logistic Regression model into a single workflow. The trained pipeline was saved using **Pickle** so that it could be reused for predicting churn for new customers.

4. The final tuned Logistic Regression model achieved approximately **74% accuracy** on the test dataset, with **80% recall and a 62% F1-score for the churn class**.
The final pipeline combines data preprocessing, encoding, scaling, SMOTE, and Logistic Regression into one workflow. It was saved using Pickle so that it can be reused to predict churn for new customers.
