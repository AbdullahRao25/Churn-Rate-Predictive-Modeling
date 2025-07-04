# Churn-Rate-Predictive-Modeling

# Telco Customer Churn Prediction

![Churn Prediction](https://img.shields.io/badge/Type-Machine_Learning-blue)  
![Python](https://img.shields.io/badge/Python-3.8%2B-green)  
![License](https://img.shields.io/badge/License-MIT-orange)  

A machine learning project to predict customer churn for a telecommunications company.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Methodology](#methodology)
- [Results](#results)
- [License](#license)

## Project Overview

This project analyzes customer data from a telecom company to predict which customers are likely to churn (cancel their service). The goal is to help the business identify at-risk customers and take proactive retention measures.

Key steps include:
- Exploratory data analysis
- Data preprocessing and feature engineering
- Handling class imbalance with SMOTE
- Building and optimizing a Random Forest classifier
- Evaluating model performance

## Dataset

The dataset contains information about 7,043 telecom customers with 20 features including:

- Demographic information (gender, senior citizen status)
- Account information (tenure, contract type)
- Services subscribed (phone, internet, additional services)
- Billing information (monthly charges, payment method)

Source: [WA_Fn-UseC_-Telco-Customer-Churn.csv](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

## Features

Key features used in the model:
- `tenure`: Number of months the customer has stayed with the company
- `MonthlyCharges`: The amount charged to the customer monthly
- `TotalCharges`: The total amount charged to the customer
- `Contract`: The contract term of the customer
- `OnlineSecurity`: Whether the customer has online security
- `TechSupport`: Whether the customer has tech support
- And other service-related features

## Installation

```bash
git clone https://github.com/yourusername/telco-churn-prediction.git
cd telco-churn-prediction
```

## Usage

Make sure you have Python 3.8+ installed, along with the required packages. Then run the main script to train and evaluate the model.

## Methodology

### Data Preprocessing
- Handled missing values in `TotalCharges`
- Encoded categorical variables using `LabelEncoder`
- Scaled numerical features using `StandardScaler`

### Feature Selection
- Used `Sequential Feature Selection` with `Logistic Regression`
- Selected 9 most important features

### Model Building
- Implemented `Random Forest Classifier`
- Used `RandomizedSearchCV` for hyperparameter tuning
- Addressed class imbalance using `SMOTE` oversampling

### Evaluation Metrics
- **Accuracy**: 77.25%
- **Precision**, **Recall**, and **F1-score** evaluated

## Results

The optimized Random Forest model achieved:

| Metric     | Score  |
|------------|--------|
| Accuracy   | 77.25% |
| Precision  | 63 %   |
| Recall     | 54 %   |
| F1-Score   | 58 %   |

The model can help identify approximately 77% of potential churn cases correctly, allowing the business to target retention efforts more effectively.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
