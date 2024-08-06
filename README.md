# credit-risk-classification
Module 20 Challenge

## Analysis Files:
  - /Credit_Risk/Crypto_Clustering.ipynb
  - /Credit_Risk/lending_data.csv

## Overview of the Analysis
* This is a supervised machine learning model used to identify loan risk.
* Financial information inludes the following: 
    - loan size
    - interest rate
    - borrower income
    - debt to income
    - num of accounts
    - derogatory marks
    - total debt
    - loan status

* The loan status lets us know if a loan defaulted or not. We use this as our y variable.

* Analysis process:
    - The data was imported from a csv file and reviewed.
    - The data was then seperated into two dataframes. One for y and one for X.
    - Using train_test_split, the data was split into training and tesing data.
    - A logic regression model was then fit with the training data using LogisticRegression solver 'lbfgs'
    - Predictions were then made using the test data and compared against the actual data.
    - A confusion matrix was generated and a classification report was generated to evaluate the accuracy of the model.


## Classification Report

                    precision    recall  f1-score   support
    
      healthy loan       1.00      0.99      1.00     18765
    high-risk loan       0.85      0.91      0.88       619
    
          accuracy                           0.99     19384
         macro avg       0.92      0.95      0.94     19384
      weighted avg       0.99      0.99      0.99     19384


## Analysis Summary
* Machine Learning Model 1:
    * The Healthy loan label is predicted well. 
    * The precision and f1-score are 100%. 
    * The recall is at .99 showing that some High Risk was predicted as healthy.
    * In the High Risk loan, the precision, recall and f1-score was slightly low. This is most likely due to a class imbalance between heathy and high risk loans. ( support ratio of 18765 / 619 ).
    * The imbalance needs to be addressed to improve the high risk accuracy.

## This model is not recomeneded for use. It will require more data from high risk loans to balance the classes.

