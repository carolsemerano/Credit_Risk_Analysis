# Credit Risk Analysis

## Overview

The purpose of this analysis is to compare the performance of different models of supervised machine learning to sample and predict credit risk in an imbalanced dataset. Analyses were created in Jupyter Notebooks, using Python libraries imbalanced-learn, and scikit-learn. The machine learning models used in this project were naive random oversampling, SMOTE, cluster centroids, SMOTEEN, Balanced Random Forest, and Easy Ensemble.

## Results

This project assumes that a credit risk assessment aims to identify those people at high risk of debt, precision and recall metrics highlighted below are related to high risk on loan_status.

- RandomOverSampler: This model resulted in a Balanced accuracy score of 0.6405, precision of 0.01, and recall of 0.72.

![NaiveOversampler](Resources/Results_Over.png) 

- SMOTE: This model resulted in a Balanced accuracy score of 0.6585, precision of 0.01, and recall of 0.62.

![SMOTE](Resources/Results_SMOTE.png) 

- ClusterCentroids: This model resulted in a Balanced accuracy score of 0.5447, precision of 0.01, and recall of 0.69.

![Under](Resources/Results_Under.png) 

- SMOTEENN: This model resulted in a Balanced accuracy score of 0.6585, precision of 0.01, and recall of 0.73.

![SMOTEENN](Resources/Results_SMOTEENN.png) 

- BalancedRandomForestClassifier: This model resulted in a Balanced accuracy score of 0.7888, precision of 0.03, and recall of 0.70.

![BRF](Resources/Results_BRF.png) 

- EasyEnsembleClassifier: This model resulted in a Balanced accuracy score of 0.9316, precision of 0.09, and recall of 0.92.

![EEC](Resources/Results_EEC.png) 

## Summary

Taking only accuracy into consideration, ensemble models - Balanced Random Forest (78,9%) and Easy Ensemble (93%) - presented significantly better results than sampling models, which range between 54% and 66%.
Regarding recall, while the easy ensemble model presented a result of 92%, all other modules have their values between 62% and 73%.
Lastly, precision presents a small variation, with slightly better performance for ensemble models. 
To sum up, Easy Ensemble is the model that presents an overall better performance. Although its precision is higher among all models, the value (0.09) is still low. As a result, a high number of low-risk customers were wrongly classified as high-risk. Thus, none of the models are recommended for this particular task.