# Credit_Risk_Analysis

## Overview of the analysis
Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, different techniques to train and evaluate models needed to be employed to evaluate models with unbalanced classes. Using the credit card dataset from LendingClub, a peer to peer lending services company, I oversampled the data using RandomOverSampler and SMOTE algorithms, and undersampled the data using ClusterCentroids. Then I used a combinatorial approach of over- and undersampling using the SMOTEEN algorithm. The final step was to use BalancedRandomForestClassifier and EasyEnsembleClassifier to predict credit risk.  

## Results
### Using Resampling Models to Predict Credit Risk
Using my knowledge of the inbalanced-learn and scikit-learn libraries, I evaluated six machine learning models by using resampling to determine which is better at predicting credit risk.

### RandomOverSampler

![RandomOverSampler](https://github.com/jstearns1988/Credit_Risk_Analysis/blob/main/Resources/RandomOverSampler.png?raw=true)

  - #### Balanced Accuracy Score: 0.6798605056669573
  - #### Precision: The precision for high_risk loans is low at 1% and is high for low_risk loans at 100%
  - #### Recall: The recall for high_risk loans is 59% and 68% for low_risk loans
  
### SMOTE Oversampling

![SMOTEOversampling](https://github.com/jstearns1988/Credit_Risk_Analysis/blob/main/Resources/SMOTE%20Oversampling.png?raw=true)
  
  - #### Balanced Accuracy Score: 0.626860815999291
  - #### Precision: The precision for high_risk loans is 1% and 100% for low_risk loans
  - #### Recall: The recall for high_risk loans is 61% and 64% for low_risk loans
  
### Undersampling
 
![Undersampling](https://github.com/jstearns1988/Credit_Risk_Analysis/blob/main/Resources/Undersampling%20corrected.png?raw=true)
)
 
  - #### Balanced Accuracy Score: 0.5163701447558731
  - #### Precision: The precision for high_risk loans is 1% and 100% for low_risk loans
  - #### Recall: The recall for high_risk loans is 61% and 45% for low_risk loans
  
### Combination (Over and Under) Sampling

![Combination](https://github.com/jstearns1988/Credit_Risk_Analysis/blob/main/Resources/Combo%20Over%20Under%20Sampling.png?raw=true)

  - #### Balanced Accuracy Score: 0.5428654460912525
  - #### Precision: The precision for high_risk loans is 1% and 100% for low_risk loans
  - #### Recall: The recall for high_risk loans is 71% and 54% for low_risk loans
  
### Balanced Random Forest Classifier

![Random Forest Classifier](https://github.com/jstearns1988/Credit_Risk_Analysis/blob/main/Resources/Balanced%20Random%20Forest%20Classifier.png?raw=true)

  - #### Balanced Accuracy Score: 0.7885466545953005
  - #### Precision: The precision for high_risk loans is 3% and 100% for low_risk loans
  - #### Recall: The recall for high_risk loans is 70% and 87% for low_risk loans
  
### Easy Ensemble AdaBoost Classifier

![Easy Ensemble AdaBoost Classifier](https://github.com/jstearns1988/Credit_Risk_Analysis/blob/main/Resources/Easy%20Ensemble%20AdaBoost%20Classifier.png?raw=true)

  - #### Balanced Accuracy Score: 0.9316600714093861
  - #### Precision: The precision for high_risk loans is 9% and 100% for low_risk loans
  - #### Recall: The recall for high_risk loans is 92% and 94% for low_risk loans

## Summary
I would advise against using any of these algorithms to detect the difficult to predict credit risk. While the Easy Ensemble AdaBoost Classifier model showed the highest accuracy overall, it can be said this is due to the fact that the dataset is significantly unbalanced. All of the models used in this analysis show weak precision in determining if a credit risk is high. With a low precision, a lot of low-risk credits are still falseley detected as high risk. 
