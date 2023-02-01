# Credit_Risk_Analysis
## Project Overview
Creating and testing a variety of supervised machine learning models for Lending Club--a peer-to-peer lending services company--to address the unbalanced classification problem and prediction of credit risk.

## Resources
 - Data Source: Lending Club; LoanStats_2019Q1.csv
 - Software: Python v3.7.13, Jupyter Notebook v6.4.8, Scikit-learn v1.0.2, Imbalanced-learn v0.10.1

## Results
After cleaning and modifying the Loan Stats dataset to utilize 85 features to train the models for the target variable, three resampling models, one combinatorial model, and two ensemble classifier models were tested to determine which is better at predicting credit risk. The results from each of the six algorithms are as follows:

### 1. Random Oversampling Model
 - Balanced Accuracy Score: 0.6573
 - Precision Score(high_risk/low_risk): 0.01 / 1.00
 - Recall Score(high_risk/low_risk): 0.71 / 0.60

<img src="https://github.com/Jay-ni13/Credit_Risk_Analysis/blob/main/Images/random_oversampling.png" width=75%>

### 2. SMOTE Oversampling Model
 - Balanced Accuracy Score: 0.6622
 - Precision Score(high_risk/low_risk): 0.01 / 1.00
 - Recall Score(high_risk/low_risk): 0.63 / 0.69

<img src="https://github.com/Jay-ni13/Credit_Risk_Analysis/blob/main/Images/smote_oversampling.png" width=75%>

### 3. Cluster Centroids Undersampling Model
 - Balanced Accuracy Score: 0.5443
 - Precision Score(high_risk/low_risk): 0.01 / 1.00
 - Recall Score(high_risk/low_risk): 0.69 / 0.40

<img src="https://github.com/Jay-ni13/Credit_Risk_Analysis/blob/main/Images/cluster_cent_undersampling.png" width=75%>

### 4. SMOTEENN Combination Model
 - Balanced Accuracy Score: 0.6392
 - Precision Score(high_risk/low_risk): 0.01 / 1.00
 - Recall Score(high_risk/low_risk): 0.70 / 0.58

<img src="https://github.com/Jay-ni13/Credit_Risk_Analysis/blob/main/Images/smoteenn_combination.png" width=75%>

### 5. Balanced Random Forest Classifier
 - Balanced Accuracy Score: 0.7885
 - Precision Score(high_risk/low_risk): 0.03 / 1.00
 - Recall Score(high_risk/low_risk): 0.70 / 0.87

<img src="https://github.com/Jay-ni13/Credit_Risk_Analysis/blob/main/Images/random_forest_clf.png" width=75%>

### 6. Easy Ensemble AdaBoost Classifier
 - Balanced Accuracy Score: 0.9317
 - Precision Score(high_risk/low_risk): 0.09 / 1.00
 - Recall Score(high_risk/low_risk): 0.92 / 0.94

<img src="https://github.com/Jay-ni13/Credit_Risk_Analysis/blob/main/Images/easy_ensemble_clf.png" width=75%>

## Summary


