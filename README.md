# Santander-Customer-Transaction-Prediction-kaggle-
This is a kaggle [project](https://www.kaggle.com/c/santander-customer-transaction-prediction/submissions final accuracy on submission file is .80085 still working on it to get a better accuracy
## Porblem Statement
It is businesses prosper problem to make customer service more effective and helpful for them by understanding their financial health and figuring out the services that will help them  to achieve their monetary goals. The aim is to identify which customer will make a specific transaction in the future irrespective of the amount of money transacted.

## About the training data
It is a binary classfication problem. Training data is highly imbalance it contains 9:1 ratio of 0 and 1.It contains 200000 examples 
and 202 features so it a big data. Challenge is to deal with imbalance data so here we handle this problem by imblearn library.

## Data Preprocessing
1.Split data into train and Cross val

2.Remove Outlier(Z-score)

3.Feature Scaling(normlization)

4. Oversampling using SMOTE(Synthetic minority oversampling technique)

4.Removing Correlated feature

## Dealing with the imbalanced data
Undersampling is also used but this lead to loss of infromation and hence it reduces the accuracy due to lack of information. So here oversampling is used using imblearn library which makes copies of minority class by some fraction here we take .5 fraction so that after the oversampling 9:1 reduced to 2:1.
## Hyperopt parameter optimisation technique
This technique  is used for tuning parameter  light gradient boosting model and random forest classifier by minimising the cross val score.
Finally the 
##  Models Used
Random Forest Classifier and Light Gradient Boosting model are used for final prediction , finally LGB performed well as compare to RFC.
The model as the data that we create is artificial training data by oversampling to deal with imbalance data.Confusion matrix is used so 
useful to analyse the output as Cross val data is also imbalance.Analysis of the output is done by following:
Our aim is to increase acc_1 and acc_0 both and in cross val we achive acc_1=.77 and acc_0=.82 

**acc_1=(true positive)/(true positive + false negeative)**

**acc_0=(true negative)/(true negative + false positive)**



