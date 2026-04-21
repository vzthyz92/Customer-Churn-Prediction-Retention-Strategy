# Customer Churn Prediction & Retention Strategy

## Objective
Predict customer churn using machine learning and identify key drivers of churn to support retention strategies.

## Business Problem
Customer churn is costly. Reducing churn improves profitability and customer lifetime value.

This project aims to:
- Predict which customers are likely to churn
- Identify the main factors driving churn
- Provide actionable retention strategies

## Dataset
Telco Customer Churn dataset containing customer demographics, services, and account information.

## Approach

### Data Preparation
- Handled missing values
- Encoded categorical variables
- Scaled numerical features

### Modeling
- Logistic Regression
- Decision Tree / Random Forest (if used)
- Model evaluation using:
  - Accuracy
  - Precision
  - Recall
  - F1-score

### Evaluation
Focused on recall and F1-score to better capture churn risk.

## Key Insights

- Customers with month-to-month contracts are more likely to churn  
- High monthly charges increase churn probability  
- Customers with longer tenure are less likely to churn  

## Business Recommendations

- Offer incentives for long-term contracts  
- Target high-risk customers with retention campaigns  
- Monitor customers with high monthly charges  

## Tools Used
Python, pandas, scikit-learn, matplotlib, seaborn

## Results
Model achieved strong predictive performance and successfully identified key churn drivers.

## How to Run
Clone repo and run notebook
