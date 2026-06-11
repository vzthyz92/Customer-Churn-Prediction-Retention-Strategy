# Customer Churn Prediction & Retention Strategy

## Overview

Customer churn is a major challenge for subscription-based businesses, particularly in the telecommunications industry. This project develops machine learning models to predict customer churn and uncover actionable insights that can support customer retention strategies.

Using the Telco Customer Churn dataset, the project performs data preprocessing, exploratory data analysis (EDA), feature engineering, and predictive modeling to identify customers who are likely to cancel their services.

---

## Business Problem

Customer acquisition is significantly more expensive than customer retention. The goal of this project is to:

- Predict whether a customer is likely to churn
- Identify the factors that contribute most to churn
- Support proactive retention campaigns
- Improve customer lifetime value and profitability

---

## Dataset

### Telco Customer Churn Dataset

The dataset contains customer information including:

- Demographic information
- Service subscriptions
- Contract details
- Billing information
- Customer tenure
- Churn status

### Target Variable

```text
Churn
```

Values:

| Value | Meaning |
|---------|---------|
| 0 | Customer Retained |
| 1 | Customer Churned |

---

## Technologies Used

| Technology | Purpose |
|------------|----------|
| Python | Programming Language |
| Pandas | Data Analysis |
| NumPy | Numerical Computing |
| Matplotlib | Data Visualization |
| Seaborn | Statistical Visualization |
| Scikit-Learn | Machine Learning |
| Jupyter Notebook | Development Environment |

---

## Project Workflow

```text
Load Dataset
      ↓
Data Inspection
      ↓
Data Cleaning
      ↓
Feature Engineering
      ↓
Exploratory Data Analysis
      ↓
Correlation Analysis
      ↓
Feature Scaling
      ↓
Train/Test Split
      ↓
Model Training
      ↓
Model Evaluation
      ↓
Business Recommendations
```

---

## Data Preprocessing

The following preprocessing steps were performed:

### Data Cleaning

- Converted `TotalCharges` to numeric values
- Removed missing values
- Removed customer identifiers
- Converted churn labels into binary values

### Feature Engineering

Categorical variables were transformed using:

```python
pd.get_dummies()
```

This enabled machine learning algorithms to process categorical information.

### Feature Scaling

Min-Max Scaling was applied to normalize features between:

```text
0 → 1
```

This ensures consistent model performance across variables.

---

## Exploratory Data Analysis (EDA)

Several visualizations were created to better understand customer behavior.

### Correlation Heatmap

Used to identify relationships between features and churn.

### Tenure Distribution

Analyzed customer subscription length.

### Monthly Charges vs Total Charges

Explored billing behavior and spending patterns.

### Churn vs Tenure Boxplot

Compared subscription length between churned and retained customers.

---

## Machine Learning Models

Two classification models were developed and compared.

---

### 1. Logistic Regression

#### Purpose

A simple and interpretable model used as a baseline classifier.

#### Advantages

- Easy to interpret
- Fast training
- Good performance on structured data

#### Training

```python
LogisticRegression(max_iter=1000)
```

---

### 2. Random Forest Classifier

#### Purpose

An ensemble learning method capable of capturing non-linear relationships.

#### Hyperparameters

```python
RandomForestClassifier(
    n_estimators=2000,
    max_features='sqrt',
    max_leaf_nodes=50,
    bootstrap=True,
    random_state=42
)
```

#### Advantages

- Handles complex patterns
- Reduces overfitting
- Provides robust predictions

---

## Model Evaluation

The models were evaluated using:

### Accuracy

Measures overall prediction correctness.

### Confusion Matrix

Provides insight into:

- True Positives
- True Negatives
- False Positives
- False Negatives

### Precision

Measures how many predicted churners actually churned.

### Recall

Measures how many actual churners were successfully identified.

---

## Results

### Logistic Regression

- Strong overall performance
- Higher recall
- Better at identifying customers likely to churn

### Random Forest

- Slightly higher precision
- Lower recall
- More conservative churn predictions

### Model Selection

For churn prediction, recall is more important than precision because missing a churn-risk customer can result in lost revenue.

As a result:

✅ **Logistic Regression was selected as the preferred model**

---

## Key Insights

### Contract Type

Customers on month-to-month contracts are significantly more likely to churn.

### Customer Tenure

Long-term customers are much less likely to leave.

### Monthly Charges

Higher monthly charges are associated with increased churn risk.

### Billing Patterns

Customers with larger bills and shorter tenure represent higher-risk segments.

---

## Business Recommendations

### Retention Campaigns

Target customers who:

- Have short tenure
- Are on month-to-month contracts
- Have high monthly charges

### Loyalty Programs

Reward long-term customers to strengthen retention.

### Contract Incentives

Encourage customers to move from month-to-month agreements to longer-term contracts.

### Predictive Monitoring

Integrate the churn model into CRM systems to automatically flag high-risk customers.

---

## Installation

### Clone Repository

```bash
git clone https://github.com/yourusername/customer-churn-prediction.git
cd customer-churn-prediction
```

### Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
Customer Churn Prediction & Retention Strategy.ipynb
```

---

## Repository Structure

```text
project/
│
├── Customer Churn Prediction & Retention Strategy.ipynb
├── Telco-Customer-Churn.csv
├── README.md
│
├── Visualizations
│   ├── Correlation Heatmap
│   ├── Histograms
│   ├── Scatter Plots
│   └── Box Plots
│
└── Models
    ├── Logistic Regression
    └── Random Forest Classifier
```

---

## Skills Demonstrated

- Data Cleaning
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Data Visualization
- Feature Scaling
- Classification Modeling
- Logistic Regression
- Random Forest Classification
- Model Evaluation
- Business Analytics
- Customer Retention Strategy

---

## Future Improvements

- Hyperparameter optimization
- Cross-validation
- XGBoost implementation
- Feature importance analysis
- SHAP explainability
- Real-time prediction API
- Interactive dashboard development

---

## Business Impact

By identifying customers at risk of churning before they leave, businesses can:

- Reduce customer attrition
- Improve customer satisfaction
- Increase customer lifetime value
- Improve revenue retention
- Support data-driven decision-making

---

## Author

**Thys van Zyl**

---

## License

This project was developed for educational and portfolio purposes.
