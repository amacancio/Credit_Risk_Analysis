# Credit_Risk_Analysis


## Overview of the Analysis

The purpose of the analysis was to employ different techniques to train and evaluate models with unbalanced classes in order to best be able to predict credit risk.


## Results

### The Initial Results

These are the results of just the initial cleaning of the data and split into testing and training, without any over- or under- sampling techniques.

<ul>
  <li>Accuracy score: 0.995</li>
</ul>

![This is an image](https://github.com/amacancio/Credit_Risk_Analysis/blob/main/Images/Initial%20Confusion%20Matrix.png)
![This is an image](https://github.com/amacancio/Credit_Risk_Analysis/blob/main/Images/Initial%20Classification%20Report.png)



### RandomOverSampler

These are the results of the RandomOverSampler technique.

<ul>
  <li>Accuracy score: 0.833</li>
</ul>

![This is an image](https://github.com/amacancio/Credit_Risk_Analysis/blob/main/Images/ROS%20CM.png)
![This is an image](https://github.com/amacancio/Credit_Risk_Analysis/blob/main/Images/ROS%20CR.png)

### SMOTE

These are the results of the SMOTE technique.

<ul>
  <li>Accuracy score: 0.844</li>
</ul>

![This is an image](https://github.com/amacancio/Credit_Risk_Analysis/blob/main/Images/SMOTE%20CM.png)
![This is an image](https://github.com/amacancio/Credit_Risk_Analysis/blob/main/Images/SMOTE%20CR.png)

### ClusterCentroids

These are the results of the ClusterCentroids technique.

<ul>
  <li>Accuracy score: 0.820</li>
</ul>

![This is an image](https://github.com/amacancio/Credit_Risk_Analysis/blob/main/Images/CC%20CM.png)
![This is an image](https://github.com/amacancio/Credit_Risk_Analysis/blob/main/Images/CC%20CR.png)

### SMOTEENN

These are the results of the SMOTEENN technique.

<ul>
  <li>Accuracy score: 0.844</li>
</ul>

![This is an image](https://github.com/amacancio/Credit_Risk_Analysis/blob/main/Images/SMOTEENN%20CM.png)
![This is an image](https://github.com/amacancio/Credit_Risk_Analysis/blob/main/Images/SMOTEENN%20CR.png)

### BalancedRandomForestClassifier

These are the results of the BalancedRandomForestClassifier technique.

<ul>
  <li>Accuracy score: 0.759</li>
</ul>

![This is an image](https://github.com/amacancio/Credit_Risk_Analysis/blob/main/Images/BRFC%20CM.png)
![This is an image](https://github.com/amacancio/Credit_Risk_Analysis/blob/main/Images/BRFC%20CR.png)

### EasyEnsembleClassifier

These are the results of the EasyEnsembleClassifier technique.

<ul>
  <li>Accuracy score: 0.932</li>
</ul>

![This is an image](https://github.com/amacancio/Credit_Risk_Analysis/blob/main/Images/EEC%20CM.png)
![This is an image](https://github.com/amacancio/Credit_Risk_Analysis/blob/main/Images/EEC%20CR.png)


## Summary

Each machine learning model interpreted the data a little bit differently.  Although the inital machine learning model, without any of the over- or under- sampling techniques had the highest accuracy score, this result is biased towards the low credit risks.  In other words, the original model was able to correctly identify most of the low risk loans, but marked a significant amount of high risk loans as low risk.  This is due to the fact that the dataset is imbalanced, meaning there are significantly more low risk loans than high risk loans.  The purpose of utilizing other sampling models is to attempt to correct the imbalance as much as possible without sacrificing the integrity of the data and its conclusions.  

To that end, the Easy Ensemble Classifier would be my recommendation of model to use.  Of all the models, it was able to correctly predict the greatest amount of high risk loans while also correctly predicting the greatest amount of low risk loans.  This model strikes the best balance between accuracy, precision, and recall of all the models, while still compensating for the imbalance in the dataset.
