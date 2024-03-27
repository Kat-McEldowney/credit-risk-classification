# credit-risk-classification
Module 20 Challenge, Machine Learning Models

# Module 20 Credit Analysis

## Overview of the Analysis

This analysis is looking at a csv with data about over 77,000 home loans. Each line in the CSV tells the story of an individual loan: the loan amount, interest rate, borrowers income and debt to income ratio, number of derogatory marks on their credit report as well as the number of open accounts, and their total debt. The purpose of this analysis is to assess if the Logistic Regression Model does a good job predicting if a loan is in danger of defaulting based on the given data.

The Logistic Regression model is a classification model of machine learning that looks at the relationship of the other data types in a set to predict the outcome. This model is limited to outcomes that contain only two choices (yes/no, true/fales, 0/1...). KMeans and Random Forests were also used to compare to the results that were generated using Logistic Regression. KMeans makes predictions based on clustering the training data together to see where the testing data might fit into these clusters. Random Forests creates multiple decision trees to then aggregrate the results of those trees to make predictions. 

The purpose of this analysis is to predict if a loan would be assigned a 0 or 1 loan status. 0 indicates that the loan is healthy, 1 indicates that the loan is in danger of defaulting. Being able to predict what loans are in danger of defaulting is of great importance to lenders who might want to take proactive steps to help their borrowers aviod default and avoid initiating legal proceedings once the default occurs. 

The data was split into testing and training sets. The training sets were used to trin the machine learning models on the data to be able to make predictions and the testing data was then used as a guage to see how accurate and effective the machine learning model was at making predictions.

Once the data was split, thre different models were created, one for each chosen model. The models were then fitted witht eh training data and then predictions were made. 


What is more important, identifying borrowers who will default or identifying borrowers who won't default.


## Results


* Logistic Regression:
    * Accuracy: 
        * macro: 0.9 
        * weighted: 0.99
    * Precision: 1
    * Recall: 0.99
 
* KMeans:
    * Accuracy: 
        * macro: 0.08
        * weighted: 0.15
    * Precision: 0.16
    * Recall: 0.01
    
* Random Forests:
    * Accuracy: 
        * macro: 0.92
        * weighted: 0.99
    * Precision: 1
    * Recall: 0.99
    
    


## Summary

The Logistic Regression and Random Forest Models' results were very close to each other and both far superior to the KMeans model which did a very poor job making accurate prediction on the supplied data. The Logistic Regression model was slightly better as it was able to correctly predict a greater number of the at risk loans as well as a smaller number of false positives. 

For this data set, it is more important to accurately predict the 1's, the loans in danger of defaulting. If a loan is incorrectly predicted to be at risk, there is no harm in reaching out to the borrower to see if they are in need of a temporary forbearance or financial counseling. If a loan is incorrectly categorized as healthy when it is indeed at risk, much needed help to avert an unwanted outcome will not be made available. 

While I think both the Logistic and Random Forest models do an adequate job of predicting at risk loans, they are both better preforming at predicting healthy loans rather than at risk ones. I think both models would perform better if the data supplied covered a couple more metrics that would be helpful in making predictions. The downpayment amount or total equity in the home would be a helpful category to include. Also, the derogatory marks on a credit report is great information to have, but including the actual credit score might be illuminating. Another great metric would be a calculation of any change credit score in the past 6 months or year. If a person has increasing credit card debt, it would not show up as a derogatory remark, but it would lower the score, providing insight into the persons financial health.

