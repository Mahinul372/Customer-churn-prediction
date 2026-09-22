# Customer-churn-prediction
Consumer churn prediction using machine learning, including data preprocessing, exploratory data analysis, and comparison of Decision Tree, Logistic Regression, Naive Bayes, and Neural Network classifiers.

A machine learning project for predicting customer churn using a consumer classification dataset. The project covers data preprocessing, exploratory data analysis (EDA), training multiple classification models, and comparing their performance using classification metrics, Precision-Recall curves, and ROC-AUC analysis.

Project Overview

The goal of this project is to classify consumers into two categories:

0 — No Churn

1 — Churn

Four machine learning approaches are trained and evaluated:

Decision Tree Classifier

Logistic Regression

Gaussian Naive Bayes

Neural Network (MLP Classifier)

Dataset

The dataset contains 1,500 records and 9 columns.

Features

Feature

Description

Age

Consumer age

Income

Consumer income

Gender

Consumer gender

Marital_Status

Marital status

Credit_Score

Consumer credit score

Num_Purchases

Number of purchases

Membership_Years

Length of membership

Device_Used

Device used by the consumer

Churn

Target variable: 0 = No Churn, 1 = Churn

The original dataset contains missing values in Age, Income, Credit_Score, and Gender.

Data Preprocessing

The notebook performs the following preprocessing steps:

Inspects missing values and dataset structure.

Imputes missing numerical values (Age, Income, and Credit_Score) using the mean.

Imputes missing Gender values using the mode.

Encodes categorical variables (Gender, Marital_Status, and Device_Used) using LabelEncoder.

Standardizes numerical features using StandardScaler.

Separates the features from the Churn target.

Splits the dataset into 70% training and 30% testing data using random_state=42 and stratification.

Exploratory Data Analysis

The project includes visual analysis of:

Overall feature distributions

Age distribution by churn status

Income distribution by churn status

Churn by gender

Churn by marital status

Churn by device used

Churn class distribution

Correlation heatmap of numerical features

Machine Learning Models

1. Decision Tree Classifier

A DecisionTreeClassifier is trained on the preprocessed training data.

2. Logistic Regression

A LogisticRegression model is trained for binary churn classification.

3. Gaussian Naive Bayes

A GaussianNB classifier is used to model the probability of churn based on the available features.

4. Neural Network

An MLPClassifier is used with:

One hidden layer

50 hidden units

Maximum of 500 iterations

Model Evaluation

The models are evaluated using:

Accuracy

Precision

Recall

F1-score

ROC-AUC

Confusion matrices

Precision-Recall curves

ROC curves

Test Set Results

The notebook reports the following test-set performance:

Model

Accuracy

ROC-AUC

Decision Tree

0.53

0.5310

Logistic Regression

0.52

0.5013

Gaussian Naive Bayes

0.52

0.5191

Neural Network (MLP)

0.51

0.5091

The classification reports and confusion matrices in the notebook provide additional precision, recall, and F1-score details for each model.

Note: The MLP classifier reached the maximum of 500 iterations without fully converging, as indicated by the warning generated during training.

Technologies Used

Python

Pandas

NumPy

Matplotlib

Seaborn

Scikit-learn

Graphviz

Project Scope

This project demonstrates an end-to-end machine learning workflow for a binary consumer churn classification problem, from preprocessing and exploratory analysis to model training, evaluation, and comparative visualization.

Jupyter Notebook
