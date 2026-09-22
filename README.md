# Customer-churn-prediction
Consumer churn prediction using machine learning, including data preprocessing, exploratory data analysis, and comparison of Decision Tree, Logistic Regression, Naive Bayes, and Neural Network classifiers.

A machine learning project for predicting customer churn using a consumer classification dataset. The project covers data preprocessing, exploratory data analysis (EDA), training multiple classification models, and comparing their performance using classification metrics, Precision-Recall curves, and ROC-AUC analysis.

# Project Overview

The goal of this project is to classify consumers into two categories:

0 — No Churn

1 — Churn

Four machine learning approaches are trained and evaluated:

1. Decision Tree Classifier

2. Logistic Regression

3. Gaussian Naive Bayes

4. Neural Network (MLP Classifier)

# Dataset

The dataset contains 1,500 records and 9 columns.

# Features

Feature -----                Description

Age -----                  Consumer age

Income  -----             Consumer income

Gender -----            Consumer gender

Marital_Status -----      Marital status

Credit_Score -----    Consumer credit score

Num_Purchases -----       Number of purchases

Membership_Years -----  Length of membership

Device_Used -----      Device used by the consumer

Churn -----          Target variable: 0 = No Churn, 1 = Churn

The original dataset contains missing values in Age, Income, Credit_Score, and Gender.

# Data Preprocessing

The project performs the following preprocessing steps:

1. Inspects missing values and dataset structure.

2. Imputes missing numerical values (Age, Income, and Credit_Score) using the mean.

3. Imputes missing Gender values using the mode.

4. Encodes categorical variables (Gender, Marital_Status, and Device_Used) using LabelEncoder.

5. Standardizes numerical features using StandardScaler.

6. Separates the features from the Churn target.

7. Splits the dataset into 70% training and 30% testing data using random_state=42 and stratification.

# Exploratory Data Analysis (EDA)

The project includes visual analysis of:

1. Overall feature distributions

2. Age distribution by churn status

3. Income distribution by churn status

4. Churn by gender

5. Churn by marital status

6. Churn by device used

7. Churn class distribution

8. Correlation heatmap of numerical features

# Machine Learning Models

1. Decision Tree Classifier

A Decision Tree Classifier is trained on the preprocessed training data.

2. Logistic Regression

A Logistic Regression model is trained for binary churn classification.

3. Gaussian Naive Bayes

A Gaussian NB classifier is used to model the probability of churn based on the available features.

4. Neural Network

An MLPClassifier is used with:

- One hidden layer

- 50 hidden units

- Maximum of 500 iterations

# Model Evaluation

The models are evaluated using: Accuracy, Precision, Recall, F1-score, ROC-AUC, Confusion matrices, Precision-Recall curves, ROC curves

# Test Set Results


Model -----                   Accuracy  -----                            ROC-AUC

Decision Tree -----             0.53  -----                               0.5310

Logistic Regression -----      0.52 -----                                0.5013

Gaussian Naive Bayes -----     0.52 -----                                0.5191

Neural Network (MLP) -----     0.51 -----                                0.5091

The classification reports and confusion matrices in the notebook provide additional precision, recall, and F1-score details for each model.

Note: The MLP classifier reached the maximum of 500 iterations without fully converging, as indicated by the warning generated during training.

Tech Stack

Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Graphviz

# Project Scope

This project demonstrates an end-to-end machine learning workflow for a binary consumer churn classification problem, from preprocessing and exploratory analysis to model training, evaluation, and comparative visualization.

Jupyter Notebook
