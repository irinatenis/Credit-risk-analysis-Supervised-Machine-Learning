# credit-risk-classification

## Overview of the Analysis
Purpose of the analysis was to build a model that could identify the creditworthiness of borrowers based on a dataset of historical lending activity from a peer-to-peer lending services company .
The dataset contained information about the size of the loan, interest rate, borrow's income, date to income ratio, number of accountsderofatory marks, and total debt. The goal was to predict the status of each loan: healthy loan or high-risk loan.

## Stages of the machine learning process for this analysis:
- Created the labels and the features.
- Split the data into training and testing datasets by using *train_test_split*.
- Instantiated and then fitted a *logistic regression model* by using the training data.
- Saved the predictions for the testing data labels by using the testing feature data.
- Evaluated the model performance by creating a *confusion matrix* and printing the *classification report*.
- Used the *RandomOverSampler module* to resample the training data and repeated the steps above to evaluate the logistic regression model on the resampled data.

## Results
**Machine Learning Model 1: Logistic Regression Model with the Original Data**
 - Accuracy: 94%
 - Precision: 100% for healthy loans and 87% for high-risk loans
 - Recall: 100% for healthy loans and 89% for high-risk loans
**Machine Learning Model 2:Logistic Regression Model with the Reasampled Training  Data**
 - Accuracy: 99%
 - Precision: 100% for healthy loans and 87% for high-risk loans
 - Recall: 100% for both healthy and high-risk loans
 
### Summary

- Machine Learning Model 2 performs best in terms of the total accuracy score. However, as predicting high-risk loans is more important for this analysis, we can conclude that there is no difference between the models as they both showed 87% precision for the high-risk loans. Even though the number of detected high-risk loans is higher in Model 2, it's accounted for by the higher number of high-risk loans predicted in general (714 vs 638 in Model 1) with the higher number of false positives.
- I would recommend trying a different model to see if we can get a higher precision for the high-risk loans.


