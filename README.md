# Supervised Machine Learning(ML)
## Overview of the analysis:
I have used the credit card credit dataset from LendingClub, a peer-to-peer lending services company,

- I have used the oversampling method for the data by using the RandomOverSampler and SMOTE algorithms, as well as used the undersampling method for the data by using the ClusterCentroids algorithm.
- The combination approach of oversampling and undersampling using the SMOTEENN algorithm were used for Deliverable #2.
- For Deliverable #3, I compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk.

Please note that I did ran into some programming errors, however I continued to work towards the end with the code that I have learnt in this module.

## Results:
### Deliverable 1: Use Resampling Models to Predict Credit Risk.
- I have used the Binary encoding with Pandas (multiple columns) to remove the string values and replace it with numeric values. It created the feature and target values that I used in the loan_status colunm. See file [credit_risk resampling](https://github.com/Judyhm2/Supervised_ML/blob/main/credit_risk_resampling.ipynb).
- The split train and test values had a Counter of ({1: 51366, 0: 246})
- For the combination of oversampling and undersampling 
![](https://github.com/Judyhm2/Supervised_ML/blob/main/Oversample.png)

### Deliverable 2: Use the SMOTEENN Algorithm to Predict Credit Risk.
- I have used the undersampling method in the file [credit_risk resampling](https://github.com/Judyhm2/Supervised_ML/blob/main/credit_risk_resampling.ipynb)
For this method, I got a balanced accuracy score of 0.66 and a prediction for high risk at 0.01 and low rish at 1.00. 
![](https://github.com/Judyhm2/Supervised_ML/blob/main/Undersample.png)
- The combination of Over and under sample methos was used to find confusion matrix, the confusion matrix produced an array for the y_prediction of 71, 30 and 7232, 9872. 
![](https://github.com/Judyhm2/Supervised_ML/blob/main/Over_Under.png)

### Deliverable 3: Use Ensemble Classifiers to Predict Credit Risk.
The Ensemble classifier with balancedrandon method was used in credit_risk_ensemble

- The BalancedRandomForestClassifier had a random_state of 1 for the X and y values. The variable clf stored the X and y value.
- The Accuracy score was stored in the variable acc_score for a value of 0.78.
- I sorted the values of the clf_model and the X.columns.
The Easy Ensemble AdaBoost Classifier generated a variable ecc.fit for the split testing; train and test.
The Imbalanced classification report for y_test and y_pred produced high_risk, low_risk and avg/total values respectively. 
## Summary
For the Combination(Over and Under) Sampling Precision = True Positive/(True Positive + False Positive), Sensitivity = True Positive/(True Positive + False Negative). The credit risk was low, therefore, the imbalance classification testing credit risk value would be good.
The sensitivity for credit_risk_resampling is lower than credit_risk_ensemble, therefore, it is important that we conduct good research on applicants.
