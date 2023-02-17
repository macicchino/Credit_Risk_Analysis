# Credit_Risk_Analysis
Module 18 - Credit Risk Analysis


## Overview of the loan prediction risk analysis:
- The purpose of the analysis is to identify credit risk using a credit card dataset. In order to test the detailed data, we first oversample using RandomOverSample and SMOTE. Then we undersample the data using the ClusterCentroids algorithm. Finally, we use a combination of both over and under sampling using the SMOTEENN algorithm. 
- Then we we use two difference machine learning techniques, reducing bias, to make predictions on credit card risk. First we use the BalancedRandomForestClassifier model and last we use the EasyEnsembleClassifier to compare the machine learning model's predictions of risk.

## Results:

- There is a bulleted list that describes the balanced accuracy score and the precision and recall scores of all six    machine learning models (15 pt)
  
1. RandomOverSample

  - The RandomOverSample balanced accuracy score and the precision and recall scores are as follows. 

![dev_1](images/1_RandomOverSample.png "Dev 1 Image")

2. SMOTE

  - The SMOTE balanced accuracy score and the precision and recall scores are as follows. 

![dev_2](images/2_SMOTE.png "Dev 2 Image")

3. ClusterCentroids

  - The ClusterCentroids balanced accuracy score and the precision and recall scores are as follows. 

![dev_3](images/3_ClusterControls.png "Dev 3 Image")

4. SMOTEENN

  - The SMOTEENN balanced accuracy score and the precision and recall scores are as follows. 

![dev_4](images/4_SMOTEENN.png "Dev 4 Image")

5. BalancedRandomForestClassifier

  - The BalancedRandomForestClassifier balanced accuracy score and the precision and recall scores are as follows. The balance accuracy score is much high for this model then the first four. 

![dev_4](images/5_BalancedRandomForestClassifier.png "Dev 5 Image")

6. EasyEnsembleClassifier

  - The EasyEnsembleClassifier balanced accuracy score and the precision and recall scores are as follows. The balance accuracy score is much high for this model then the first four. 

![dev_6](images/6_EasyEnsembleClassifier.png "Dev 6 Image")



## Summary:

- As we can see the Machine Learning Techiniques of (1) BalancedRandomForestClassifier and (2) EasyEnsembleClassifier are better models to use for this very grainular data. We can see the balanced accurancy scores of both of these models is about 0.95 which is much higher than the other four models with balanced accurancy scores in the range of 0.52 to 0.65. 

- In additon, I would recommend using the EasyEnsembleClassifier as the best model to analyze the data and make predictions. It's confusion matrix offers a better balance and thus more precision. We can see this when reviewing the F1 scores. The F1 scores for BalancedRandomForestClassifier were 0.10 for high-risk and 0.95. for low-risk. In comparison, the F1 scores for EasyEnsembleClassifier were 0.18 for high-risk and 0.98 for low-risk. So it is more accurate at predicting both the high risk and low risk events. However, we are most interested in credit risk! So the prediction of 'high risk' credit cards is very important. So the high F-1 score of the EasyEnsembleClassifier at 0.18 for high-risk is almost twice as accurate as the BalancedRandomForestClassifier with an F-1 score 0.10 for high-risk.



