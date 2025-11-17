# 🛳️ Titanic Survival Analysis
A complete R project analyzing the Titanic dataset using statistical modeling, imputation, visualization, and machine learning techniques.

## 📁 Project Structure
```
├── titanic.Rmd        # Main analysis file (R Markdown)
├── titanic3.xls       # Dataset used in the project
└── README.md          # Documentation
```

## 📊 Project Objectives
- Clean and preprocess the Titanic dataset
- Handle missing values using imputation
- Explore relationships between demographic & travel features
- Build logistic regression models to predict survival
- Apply techniques such as:
  - Feature engineering
  - k-fold cross validation
  - ROC curves, AUC
  - Calibration plots
  - Model performance metrics
- Generate interpretable insights to understand which factors influenced survival

## 🛠️ Technologies & Packages Used
### Core R Packages
- tidyverse – data manipulation & visualization  
- caret – model training, cross-validation, performance metrics  
- rms – logistic regression, spline modeling, calibration  
- pROC – ROC curve + AUC  
- mice – missing data imputation  
- ggplot2 – custom visualizations  

## 📂 Dataset
Dataset: **titanic3.xls**

## 🧹 Data Cleaning & Preparation
Steps:
- Missing value inspection
- Imputation of age and embarked
- Handling categorical variables
- Removing unused columns
- Creating training-ready dataset

## 📈 Modeling Approach
### 1. Logistic Regression (Base Model)
- Predictors include sex, class, age, fare, sibsp, parch, embarked  
- Evaluation: AIC, pseudo-R², OR, CI, p-values

### 2. Logistic Regression with Restricted Cubic Splines
- Nonlinear modeling using rms::lrm
- Knots tested: 3, 4, 5
- Validation + calibration

### 3. caret Machine Learning Workflow
- 10-fold cross validation
- ROC, Sensitivity, Specificity
- Confusion matrix
- Feature importance

## 📊 Evaluation Metrics
- Accuracy
- Sensitivity & Specificity
- Precision / Recall / F1-score
- AUC (ROC Curve)
- KS Statistic
- Calibration Curve
- Variable Importance

## 📉 Visualizations
Includes:
- ROC curves  
- Survival distributions by gender/class  
- Odds ratio plots  
- Calibration curves  

## 🚀 How to Run
```
install.packages(c("tidyverse", "caret", "rms", "pROC",
                   "mice", "ModelMetrics"))
```
Open **titanic.Rmd** in RStudio and knit.

## 📚 Results Summary
- Females had significantly higher survival rates  
- Higher class → better survival  
- Age has nonlinear effects  
- Final model achieved high ROC AUC

