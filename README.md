# Credit_Risk_Analysis

## Overview

The purpose of this analysis is to understand the factors that affect the risk levels associated with individuals who may apply for loans based on their credit status and history.  This analysis utilised various supervised machine learning models to attempt to accurately predict whether or not individuals were "high" or "low" credit risk.  Due to the heavy imbalance of the data (far more low risk individuals vs. high risk), several techniques were implemented to improve model accuracy, including:
- Naive Random Oversampling
- Synthetic Minority Oversampling Technique (or SMOTE)
- Undersampling using the Cluster Centriods algorithm
- Combination (Over and Under) Sampling using SMOTEEN
- Ensemble Classifier Decision Tree method using the Balanced Random Forest Algorithm
- Adaptive Boost (AdaBoost) Classifier

## Results

Each of the methods produced distict results as follows:

![Results_Table](/Resources/Methods_Results_Table.png)

Oversampling method and its SMOTE enhancement provided marginal improvement on the Recall of low risk classification, which would be the key performance indicator as limiting false negatives is integral to lender control of financial risk.  An actual high risk individual labelled as low risk is a potential unknown liability.

Simple undersampling is probably the worst method of the lot, as the balanced accuracy score and low risk recall is the lowest of all the methods tested by close to 10 and 20 points respectively.  However the balanced Over/Undersampling SMOTEENN method proves to be significant enhancement to the Undersampling method, but is effectively the same as the SMOTE method in this case.

The best results for this dataset are in the Balanced Random Forest and further in the Ensemble AdaBoost methods with provide significant improvments to balanced accuracy and Low Risk Recall.

## Summary

To summarize, the ensemble machine learning algorithms, particularly with the adaptive boost enhancement proved to be the better method for determining credit risk of individuals and particularly in limiting the potential number of low risk false negatives.

Undersampling proved to be the worst method used and the false negative rate was significantly worse and would potentially expose any lenders using this model to lend money to high risk individuals without adequate risk mitigation.

