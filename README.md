# Credit_Risk_Analysis
## Overview

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, we will oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, we will use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, we will compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. In the end, we will evaluate the performance of these models and make a recommendation on whether they should be used to predict credit risk.

## Results
#### Logistic Regression with Different Sampling Methods
##### Balanced Accuracy Score
Since we have imbalanced classes, we use the Balanced Accuracy score to measure how well our Logistic Regression performs with the different sampling methods.
- Random Oversampling: For the Random Oversampling, our Balanced Accuracy Score is 0.65 meaning that the model was correct (in predicting high_risk and low_risk loans) 65% of the time.
- SMOTE Sampling: Balanced Accuracy Score for the SMOTE sampling method sligly ouperformed the Random Sampling method at 66%
- Undersampling: With a Balanced Accuracy Score of 54%, the undersampling technique had the worst performnce of the different sampling methods.
- Combination Sampling: The Combination sampling method had similar performance with the Oversampling and SMOTE sampling with 66%
##### Recall and Precision
- Recall was 0.69 and 0.60 for high_risk and low_risk loans respectively for the oversampling method
- Recall was 0.63 and 0.69 for high_risk and low_risk loans respectively for the SMOTE method
- Recall was 0.69 and 0.40 for high_risk and low_risk loans respectively for the undrsampling method
  - the low recall for the undersampling method for the low_risk loans is indicative of a large number of false negatives. 
- Recall was 0.75 and 0.58 for high_risk and low_risk loans respectively for the combination method
- The combination sampling method had the best recall at 0.75 for correctly predicting high_risk loans
- Precision for all the sampling methods performed poorly, only correctly predicting high_risk loans 1% of the time; this is indicative of a large number of false positives
#### Random Oversampling
![Results_Oversampling](https://user-images.githubusercontent.com/67847583/129494703-176be304-f99c-4316-8697-2464116cabca.png)

#### SMOTE Oversampling
![Results_SMOTE](https://user-images.githubusercontent.com/67847583/129494743-4963d634-c4b7-4e43-bd74-2f8aa546be0e.png)

#### Undersampling
![Results_Undersampling](https://user-images.githubusercontent.com/67847583/129494756-6c6d7847-3f8b-4ef9-bd1e-28003327210d.png)

#### Combination (Over and Under) Sampling
![Results_Combination_Sampling](https://user-images.githubusercontent.com/67847583/129494779-d548816c-4383-4775-bf22-304a0efbd6e5.png)


#### Random Forest and Easy Ensemble Classifier
##### Balanced Accuracy Score
- Random Forest: With a balanced accuracy score of 79%, the Random Forest clasifier outperforms the logistic regression with different sampling techniques
- Easy Ensemble Classifier: With a balanced accuracy score of 93%, the Easy Ensemble Classifier outperforms variations of the logistic regression used for the project including the Random Forest Classifier

##### Recall and Precision
- Recall was 0.70 and 0.87 for high_risk and low_risk loans respectively for the Random Forest
- Recall was 0.92 and 0.94 for high_risk and low_risk loans respectively for the Easy Ensemble Classifier
- Precision for high_risk loans was 0.03 and 0.09 for the Random Forest and the Easy Ensemble Classifier respectively.

While the Ensemble Classifier has the best Precison of the models used, it still does a poor job at correctly pedicting high_risk loans

#### Random Forest
![Results_Random_Forest](https://user-images.githubusercontent.com/67847583/129494795-d74a3c45-0083-465e-a68c-4f6d6d0ef86d.png)

#### Easy Ensemble
![Results_EasyEnsemble](https://user-images.githubusercontent.com/67847583/129494807-12e8e270-eeff-48ed-9416-8f553d97472d.png)

## Summary

#### Balanced Accuracy Score: Ensemble Models vs Sampling Classifiers
##### Ensemble Models
![Ensemble_Classifier_Bal_Acc_Score](https://user-images.githubusercontent.com/67847583/129495017-c9fcf950-2fb6-49ab-968c-2fac72263cff.png)
##### Sampling Methods
![Sampling_Classifier_Bal_Acc_Score](https://user-images.githubusercontent.com/67847583/129495081-1220a41a-63d6-4f2e-8540-4a0b5590f516.png)

#### Recall_Precision: Ensemble Models vs Sampling Classifiers
##### Ensemble Models
![Ensemble_Classifier_Recall_Precision](https://user-images.githubusercontent.com/67847583/129495148-93117434-cf0c-4190-b278-82010ae5b800.png)
##### Sampling Methods
![Sampling_Classifier_Recall_Precision](https://user-images.githubusercontent.com/67847583/129495158-cffeeaf3-b2f7-46c0-95cd-33bafccee29c.png)


While, the Ensemble Classifier outperforms all other classifiers tested, the model still does a poor job at predicting high_risk loans. We may want to revaluate our feature selection or test a different model that would perform better.




