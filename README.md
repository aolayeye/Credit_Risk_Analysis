# Credit_Risk_Analysis
## Overview

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, we will oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, we will use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, we will compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. In the end, we will evaluate the performance of these models and make a recommendation on whether they should be used to predict credit risk.

## Results
#### Random Oversampling
![Results_Oversampling](https://user-images.githubusercontent.com/67847583/129494703-176be304-f99c-4316-8697-2464116cabca.png)

#### SMOTE Oversampling
![Results_SMOTE](https://user-images.githubusercontent.com/67847583/129494743-4963d634-c4b7-4e43-bd74-2f8aa546be0e.png)

#### Undersampling
![Results_Undersampling](https://user-images.githubusercontent.com/67847583/129494756-6c6d7847-3f8b-4ef9-bd1e-28003327210d.png)

#### Combination (Over and Under) Sampling
![Results_Combination_Sampling](https://user-images.githubusercontent.com/67847583/129494779-d548816c-4383-4775-bf22-304a0efbd6e5.png)

#### Random Forest
![Results_Random_Forest](https://user-images.githubusercontent.com/67847583/129494795-d74a3c45-0083-465e-a68c-4f6d6d0ef86d.png)

#### Easy Ensemble
![Results_EasyEnsemble](https://user-images.githubusercontent.com/67847583/129494807-12e8e270-eeff-48ed-9416-8f553d97472d.png)

## Summary
Our results show that the ensemble models outperform the sampling methods including the combination sampling method.

#### Sampling Classifiers: Balanced Accuracy Score vs Ensemble Models
![Sampling_Classifier_Bal_Acc_Score](https://user-images.githubusercontent.com/67847583/129495058-398d60c4-a211-4b6f-b667-7042e477f1a3.png)
![Ensemble_Classifier_Bal_Acc_Score](https://user-images.githubusercontent.com/67847583/129495017-c9fcf950-2fb6-49ab-968c-2fac72263cff.png)

#### Ensemble Models: 
