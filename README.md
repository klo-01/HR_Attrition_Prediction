# HR Attrition Prediction using Machine Learning
Predicting employee turnover is a critical challenge for organizations. This project applies machine learning techniques to identify the key drivers of attrition and build predictive models that help HR teams proactively retain talent.

## Project Overview
This project analyzes a dataset of 1,470 employees containing demographic, job‑related, compensation, and satisfaction attributes.The goal is to build classification models that predict whether an employee is likely to leave the company.

The workflow includes:
Data cleaning & preprocessing
Exploratory data analysis (univariate, bivariate, multivariate)
Feature engineering & encoding
Model development (KNN, Naive Bayes, Logistic Regression)
Model evaluation using multiple metrics
Insights & business recommendations

## Tools & Technologies
Python (Jupyter Notebook)
NumPy, Pandas
Matplotlib, Seaborn
Scikit‑learn

## Dataset
Source: HR Employee Attrition Dataset (Kaggle)
Records: 1,470 employees
Features: 31 variables (after cleaning, irrelevant constant‑value columns removed)
Target Variable: Attrition (Yes/No → 1/0)

## Data Preparation
A. Data Cleaning
1. Removed duplicates
2. Verified no missing values
3. Dropped irrelevant or constant‑value columns:
a. EmployeeNumber
b. mployeeCount
c. Over18
d. StandardHours

B. Feature Engineering
1. Binary encoding of target variable
2. One‑hot encoding for categorical variables
3. Standard scaling for numerical features (important for KNN)

C.   Train/Test Split
70% training
30% testing

## Exploratory Data Analysis (EDA)
A. Univariate Insights
1. Younger employees and low‑income employees show higher attrition.
2. Most employees have short tenure (0–5 years).
3. Low job satisfaction strongly correlates with leaving.

B. Bivariate Insights
1. Employees working overtime have significantly higher attrition.
2. Longer commute distances slightly increase attrition.
3. Low satisfaction (job, environment, work‑life balance) increases turnover.
4. Frequent business travel and single marital status are associated with higher attrition.

C. Multivariate Insights
1. Correlation heatmaps show:
a. Positive correlation with attrition: Overtime, Single marital status, Frequent travel
b. Negative correlation: Age, MonthlyIncome, JobLevel, TotalWorkingYears, YearsAtCompany

## Machine Learning Models
Four models were developed and evaluated:

1. Baseline Model (Dummy Classifier)
a. Accuracy: 0.839
b. Predicts only “No Attrition”
c. Serves as benchmark

2. K‑Nearest Neighbors (k = 7)
a. Accuracy: 0.850 (highest)
b. Precision: 0.692
c. Recall: 0.127 (very low)
d. Good when predicting attrition, but misses many actual cases

3. Naive Bayes (GaussianNB)
a. Accuracy: 0.635
b. Precision: 0.266
c. Recall: 0.718 (highest)
d. Useful when identifying as many attrition cases as possible

4. Logistic Regression (Best Overall Model)
a. Accuracy: 0.760
b. Precision: 0.370
c. Recall: 0.704
d. F1‑Score: 0.485 (highest)
e. Best balance between precision and recall
f. Highest ROC‑AUC among all models

## Key Insights
From the analysis and modeling:
1. Employees with low income, short tenure, and low satisfaction are more likely to leave.
2. Overtime is one of the strongest predictors of attrition.
3. Younger employees and single employees show higher turnover.
4. Frequent business travel increases attrition risk.
5. Logistic Regression provides the most reliable predictive performance.

## Business Recommendations
Based on the findings, HR teams should consider:
1. Improving compensation for lower‑income employees
2. Reducing overtime or offering better overtime compensation
3. Enhancing work‑life balance programs
4. Targeted retention strategies for high‑risk groups (e.g., Sales Reps, Lab Technicians)
5. Monitoring early‑tenure employees more closely
6. Improving workplace environment and satisfaction

## Author
Ke Ping Lo  
Business Insights & Analytics
Toronto, Canada
