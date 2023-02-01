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
 - Precision Score (high_risk/low_risk): 0.01 / 1.00
 - Recall Score (high_risk/low_risk): 0.71 / 0.60

<img src="https://github.com/Jay-ni13/Credit_Risk_Analysis/blob/main/Images/random_oversampling.png" width=75%>

### 2. SMOTE Oversampling Model
 - Balanced Accuracy Score: 0.6622
 - Precision Score (high_risk/low_risk): 0.01 / 1.00
 - Recall Score (high_risk/low_risk): 0.63 / 0.69

<img src="https://github.com/Jay-ni13/Credit_Risk_Analysis/blob/main/Images/smote_oversampling.png" width=75%>

### 3. Cluster Centroids Undersampling Model
 - Balanced Accuracy Score: 0.5443
 - Precision Score (high_risk/low_risk): 0.01 / 1.00
 - Recall Score (high_risk/low_risk): 0.69 / 0.40

<img src="https://github.com/Jay-ni13/Credit_Risk_Analysis/blob/main/Images/cluster_cent_undersampling.png" width=75%>

### 4. SMOTEENN Combination Model
 - Balanced Accuracy Score: 0.6392
 - Precision Score (high_risk/low_risk): 0.01 / 1.00
 - Recall Score (high_risk/low_risk): 0.70 / 0.58

<img src="https://github.com/Jay-ni13/Credit_Risk_Analysis/blob/main/Images/smoteenn_combination.png" width=75%>

### 5. Balanced Random Forest Classifier
 - Balanced Accuracy Score: 0.7885
 - Precision Score (high_risk/low_risk): 0.03 / 1.00
 - Recall Score (high_risk/low_risk): 0.70 / 0.87

<img src="https://github.com/Jay-ni13/Credit_Risk_Analysis/blob/main/Images/random_forest_clf.png" width=75%>

### 6. Easy Ensemble AdaBoost Classifier
 - Balanced Accuracy Score: 0.9317
 - Precision Score (high_risk/low_risk): 0.09 / 1.00
 - Recall Score (high_risk/low_risk): 0.92 / 0.94

<img src="https://github.com/Jay-ni13/Credit_Risk_Analysis/blob/main/Images/easy_ensemble_clf.png" width=75%>

## Summary
The first four resampling models have high precision for predicting low risk loans, but very low precision when it comes to predicting high risk loans; the recall for all four models ranges between 0.40 to 0.71, with the high risk loan prediction generally having the higher sensitivity value. Though these low precision values for high risk loan prediction mean a greater number of false positives--saving Lending Club money by reducing the number of loan applications being approved as low risk--the mediocre recall score for high risk loan prediction in these models means that a number of loan applications that are actually high risk will be categorized as low risk (i.e. false negatives)--only 70% of high risk loan applications will correctly be flagged as such.

For Lending Club to better evaluate loan applications and credit card risk, these models need more accurate recall scores to ensure they are identifying as many high risk loans as possible, because identifying some low risk applications as high risk is not as detrimental as classifying true high risk loans as low risk.

The two ensemble classifiers improve in both precision and recall over the resampling models, with the Easy Ensemble AdaBoost Classifier having a balanced accuracy score of 0.93, and a 0.09 precision score and 0.92 recall score for high risk prediction. While it correctly identifys 93 of the 101 high risk loans, it also incorrectly categorizes 983 low risk loans as high risk.

### Recommendation
Though the Easy Ensemble AdaBoost Classifier might work as an interim option, analysis of features importance in the Balanced Random Forest Classifier indicate that the models could be further improved by modifying the initial dataset.
 - The models' 11 most important features:
 <img src="https://github.com/Jay-ni13/Credit_Risk_Analysis/blob/main/Images/most_important_features.png" width=65%>

 - The models' 11 least important features:
 <img src="https://github.com/Jay-ni13/Credit_Risk_Analysis/blob/main/Images/least_important_features.png" width=35%>
 
 - The remaining 63 features only explain 0.0001 to 0.01 percent of the data.

New data points/features should be added to evaluate their relationship to credit risk and features with mininal to no impact should be dropped to avoid overfitting of the model. Then the machine learning models should be train on the modified dataset to find an option with a better high risk recall score to replace the interim option.


