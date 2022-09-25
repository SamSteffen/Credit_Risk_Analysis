# Credit_Risk_Analysis
A comparative analysis of machine learning models that utilize Python's imbalanced-learn and scikit-learn libraries to evaluate loan and credit risk.

## Overview
Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Using credit card data from LendingClub, a peer-to-peer lending services company, this analysis utilizes Python's imbalanced-learn and scikit-learn libraries and employs the following techniques to train and evaluate data models with unbalanced classes.

1. Oversampling with RandomOverSampler
2. Oversampling with Synthetic Minority Oversampling Technique (SMOTE)
3. Undersampling with ClusterCentroids.
4. Oversampling and Undersampling with Synthetic Minority Oversampling Technique and Edit Nearest Neighbor (SMOTEENN)
5. BalancedRandomForestClassifier 
6. EasyEnsembleClassifier

A breakdown of the results of these models, as well as notes about how each model was established, is provided below.

## Results
Results: Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.

### 1. Oversampling with RandomOverSampler
To create this model, data was oversampled to yield 51,366 rows of data for the target category, credit risk. An image of the classification report is shown below:

[image 1]

* Balanced Accuracy Score: 0.6620175698580149
* Precision Score (Avg): 0.99
* Recall Score (Avg): 0.60 

The balanced accuracy score indicates that 66% of the model's predictions as to whether an individual's credit risk was low or high, were correct. The model shows a 99% precision score, indicating that the data contains a large number of true positives. The recall (sensitivity) score indicates that the classifier correctly predicted 60% of the positive cases out of all the positive cases in the dataset.

### 2. Oversampling with Synthetic Minority Oversampling Technique (SMOTE)
To create this model, data was oversampled to yield 51,366 rows of data for the target category, credit risk. An image of the classification report is shown below:

[image 2]

Balanced Accuracy Score: 0.6568196079430206
Precision Score (Avg): 0.99
Recall Score (Avg): 0.70

The balanced accuracy score indicates that roughly 66% of the model's predictions as to whether an individual's credit risk was low or high, were correct. This model, like the previous model, also shows a 99% precision score, indicating that the data contains a large number of true positives. The recall (sensitivity) score in this model, however, shows a significant improvement over the first, and indicates that 70% of the positive cases out of all the positive cases in the dataset were correctly predicted.

### 3. Undersampling with ClusterCentroids.
246 rows of data

Balanced Accuracy Score: 0.5447339051023905
Precision Score: 0.99
Recall Score: 0.40

### 4. Oversampling and Undersampling with Synthetic Minority Oversampling Technique and Edit Nearest Neighbor (SMOTEENN)
68,460 rows of data

Balanced Accuracy Score: 0.6461148570422992
Precision Score: 0.99
Recall Score: 0.57

### 5. BalancedRandomForestClassifier 
68470 rows

Balanced Accuracy Score: 0.782387479276459 
Precision Score: 0.99
Recall Score: 0.88

### 6. EasyEnsembleClassifier
68470 rows

Balanced Accuracy Score: 0.9316600714093861
Precision Score: 0.99
Recall Score: 0.94


Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, you’ll oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, you’ll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, you’ll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once you’re done, you’ll evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.


Deliverable 1: Use Resampling Models to Predict Credit Risk
Using your knowledge of the imbalanced-learn and scikit-learn libraries, you’ll evaluate three machine learning models by using resampling to determine which is better at predicting credit risk. First, you’ll use the oversampling RandomOverSampler and SMOTE algorithms, and then you’ll use the undersampling ClusterCentroids algorithm. Using these algorithms, you’ll resample the dataset, view the count of the target classes, train a logistic regression classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.

Deliverable 2: Use the SMOTEENN Algorithm to Predict Credit Risk
Using your knowledge of the imbalanced-learn and scikit-learn libraries, you’ll use a combinatorial approach of over- and undersampling with the SMOTEENN algorithm to determine if the results from the combinatorial approach are better at predicting credit risk than the resampling algorithms from Deliverable 1. Using the SMOTEENN algorithm, you’ll resample the dataset, view the count of the target classes, train a logistic regression classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.

Deliverable 3: Use Ensemble Classifiers to Predict Credit Risk
Using your knowledge of the imblearn.ensemble library, you’ll train and compare two different ensemble classifiers, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk and evaluate each model. Using both algorithms, you’ll resample the dataset, view the count of the target classes, train the ensemble classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.

## Summary
Summary: Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.