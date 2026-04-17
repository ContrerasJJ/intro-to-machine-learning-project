# Customer-Churn-Prediction-Beta-Bank

## Table of Contents
- [Project Objective](#project-objective)
- [Project Structure](#project-structure)
- [Tools and Techniques Utilized](#tools-and-techniques-utilized)
- [Results and Recommendations](#results-and-recommendations)
- [What I Have Learned From This Project](#what-i-have-learned-from-this-project)
- [How to Use This Repository](#how-to-use-this-repository)

---

## Project Objective
The goal of this project is to develop a machine learning model that predicts customer churn for Beta Bank. By analyzing historical customer behavior and account data, the model identifies customers who are likely to leave the bank.

This enables the business to take proactive retention actions, reduce customer attrition, and improve long term revenue.

---

## Introduction
Beta Bank is experiencing customer attrition, leading to revenue loss. Retaining existing customers is significantly more cost effective than acquiring new ones, making churn prediction a critical business problem.

In this project, we build a classification model to predict whether a customer will leave the bank based on demographic and behavioral features. The goal is to support data driven retention strategies by identifying high risk customers early.


---

## Dataset Overview

The dataset contains information on 10,000 bank customers, including demographic details, account information, and activity metrics.

**Target Variable:**
- `Exited` (1 = customer left, 0 = customer stayed)

The dataset includes features such as:
- Credit Score
- Geography
- Age
- Tenure
- Balance
- Number of Products
- Estimated Salary

---

## Project Structure

The project consists of the following main steps:

1. **Data Loading and Initial Exploration**
   - Loaded the `users_behavior` dataset.
   - Reviewed column types, basic statistics, and checked for missing values or obvious anomalies.

2. **Data Cleaning and Feature Preparation**
   - Handled missing values and corrected data types where necessary.
   - Engineered and selected features relevant for modeling.
   - Split the data into training and test sets.

3. **Model Training and Evaluation**
   - Trained several baseline models (e.g., Logistic Regression, Decision Tree, Random Forest).
   - Evaluated performance using accuracy, ROC-AUC, and confusion matrix.
   - Compared results and selected the best performing model.

4. **Interpretation and Business Impact**
   - Analyzed which features were most important to the model.
   - Translated model performance into practical business implications.

---

## Model Performance Comparison

Several models were trained and evaluated to identify the best performing approach:

- **Logistic Regression**
  - F1 Score: ~0.51
  - ROC-AUC: ~0.72
  - Struggled with class imbalance and recall for churned customers

- **Random Forest Classifier**
  - F1 Score: ~0.58–0.62
  - ROC-AUC: ~0.86
  - Better captured nonlinear relationships and improved recall

The Random Forest model was selected as the final model due to its superior performance across both F1-score and ROC-AUC metrics.

## Tools and Techniques Utilized

- **Programming & Libraries**
  - Python, Jupyter Notebook
  - pandas, NumPy
  - scikit-learn
  - matplotlib, seaborn

- **Methods**
  - Exploratory Data Analysis (EDA)
  - Data cleaning and preprocessing
  - Train/test split
  - Supervised learning (classification)
  - Model evaluation (accuracy, ROC-AUC, confusion matrix)

---

## Results and Recommendations

- Developed a machine learning model capable of predicting customer churn with strong performance.
- **Final Model (Random Forest):**
  - F1 Score: **0.619**
  - ROC-AUC: **0.864**
- Addressing class imbalance using upsampling and class weighting significantly improved model performance.
- The model demonstrates strong ability to distinguish between customers who will leave and those who will stay.

### Business Impact

This model can support business decisions such as:
- Identifying high risk customers before they churn
- Targeting retention campaigns more effectively
- Reducing customer acquisition costs by focusing on retention

### Recommendations

- Deploy the model as a decision support tool for customer retention teams
- Incorporate additional behavioral features (e.g., transaction history) to improve predictions
- Continue optimizing models using hyperparameter tuning or advanced algorithms (e.g., Gradient Boosting)
---

## What I Have Learned From This Project

- How to structure a complete supervised learning pipeline from raw data to model evaluation.
- The importance of data preprocessing and feature quality on model performance.
- How to interpret classification metrics and connect them to real business decisions.
- Practical experience in using scikit-learn for model training, evaluation, and comparison.

---

## How to Use This Repository

1. **Clone the repository**
```bash
git clone https://github.com/ContrerasJJ/customer-churn-prediction-beta-bank.git
cd customer-churn-prediction-beta-bank
