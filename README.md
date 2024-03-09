## Credit Analysis Project: Loan Default Prediction (2007-2024)

# Project Overview:
This project focuses on credit risk analysis for loans issued between 2007 and 2024. The goal is to develop predictive models for Probability of Default (PD), Loss Given Default (LGD), and Exposure at Default (EAD) to estimate the Expected Loss (EL).

# Steps:
1. Data Preprocessing:
    * Handling Variables:
        Convert string and datetime variables into numerical data types.
    * Discrete Variables:
        Create functions to convert discrete variables into dummy variables using Weight of Evidence (WoE) and Information Value.
    * Continuous Variables:
        Implement functions for WoE and Information Value calculation for continuous variables, determining the number of categories, and finding reference categories.

2. Dummy Variable Conversion:
    * Train and Test Sets:
        Apply preprocessing steps to the test dataset for consistency.
    * Dummy Variables:
        Convert categorical variables into dummy variables for both training and test datasets.
    * Feature Selection:
        Identify and select relevant features, excluding reference categories for model training.

3. Logistic Regression Model for PD:
    * Model Creation:
        Develop a logistic regression model for Probability of Default (PD) using selected features.
    * P-Value Analysis:
        Extract p-values for each category from the logistic regression model.
    * Model Evaluation:
        Evaluate PD model accuracy using confusion matrix, threshold values, ROC curve, AUC, Gini coefficient, and Kolmogorov coefficient.

4. Population Stability Index (PSI):
    * New Data from 2015:
        Extract new data from 2015 for testing and comparing population stability.
    * PSI Calculation:
        Calculate the Population Stability Index (PSI) to compare distribution shifts between training and new data.
    * Model Upgradation:
        Consider model retraining or updating based on significant differences in data distribution.

5. LGD (Loss Given Default) and EAD (Exposure at Default) Models:
    * Creating Independent Variables:
        Filter the dataset to include only rows with charge-off or default for LGD and EAD model training.
    * LGD Model:
        Develop LGD model using logistic regression and linear regression to predict recovery rate.
    * EAD Model:
        Formulate EAD model with the dependent variable as Credit Conversion Factor (CCF).
    * Combining Models:
        Combine LGD, EAD, and PD models by multiplying their coefficients to obtain the Expected Loss (EL).


