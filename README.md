# Customer Churn Prediction

## Overview
This repository contains a Jupyter Notebook (`customer_churn_prediction.ipynb`) that implements a machine learning pipeline to predict customer churn using the **Credit Card Customer Churn Prediction dataset** from Kaggle. The project explores the dataset, performs exploratory data analysis (EDA), and applies multiple machine learning models to predict whether a customer will leave the bank (churn) or not. The notebook also includes an attempt to build an Artificial Neural Network (ANN) for churn prediction.

The primary goal is to identify key factors influencing customer churn and develop predictive models to help businesses reduce churn rates.

## Dataset
The dataset used in this project is the [Credit Card Customer Churn Prediction dataset](https://www.kaggle.com/datasets/rjmanoj/credit-card-customer-churn-prediction) from Kaggle. It contains customer-related features such as credit score, geography, gender, age, tenure, balance, and more, with the target variable `Exited` indicating whether a customer churned (1) or not (0).

### Key Features:
- **CreditScore**: Customer's credit score
- **Geography**: Customer's location (e.g., France, Spain, Germany)
- **Gender**: Customer's gender
- **Age**: Customer's age
- **Tenure**: Number of years the customer has been with the bank
- **Balance**: Customer's account balance
- **NumOfProducts**: Number of bank products the customer uses
- **HasCrCard**: Whether the customer has a credit card (1/0)
- **IsActiveMember**: Whether the customer is an active member (1/0)
- **EstimatedSalary**: Customer's estimated salary
- **Exited**: Target variable (1 = Churned, 0 = Not Churned)

## Project Structure
- **`customer_churn_prediction.ipynb`**: The main Jupyter Notebook containing the code for data loading, preprocessing, EDA, model training, and evaluation.
- **`Churn_Modelling.csv`**: The dataset file (not included in the repository; download from Kaggle).
- **`README.md`**: This file, providing an overview of the project and instructions.

## Methodology
The notebook follows these steps:
1. **Data Loading and Exploration**:
   - Load the dataset using pandas.
   - Perform basic checks (e.g., shape, duplicates, missing values).
   - Visualize the distribution of the target variable (`Exited`) and categorical features (`Geography`, `Gender`).

2. **Exploratory Data Analysis (EDA)**:
   - Analyze the distribution of churned vs. non-churned customers.
   - Generate a correlation matrix to understand feature relationships.
   - Identify the imbalanced nature of the dataset (more non-churned than churned customers).

3. **Data Preprocessing**:
   - Drop irrelevant columns (`RowNumber`, `CustomerId`, `Surname`).
   - Encode categorical variables (`Geography`, `Gender`) using `LabelEncoder`.
   - Split the data into training and testing sets (80-20 split).
   - Scale features using `StandardScaler`.
   - Address class imbalance using SMOTE (Synthetic Minority Oversampling Technique).

4. **Model Training and Evaluation**:
   - Train and evaluate three machine learning models:
     - **Logistic Regression**
     - **Random Forest Classifier**
     - **XGBoost Classifier**
   - Metrics used: Accuracy, Precision, Recall, F1 Score.
   - Visualize confusion matrices for each model.
   - Analyze feature importance using the Random Forest model.

5. **Artificial Neural Network (ANN)**:
   - Attempt to build an ANN for churn prediction (incomplete due to errors in the notebook).

## Installation
To run the notebook locally, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/<your-username>/customer-churn-prediction.git
   cd customer-churn-prediction
