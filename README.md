# Credit_Risk_Analysis
A comparative analysis of machine learning models that utilize Python's imbalanced-learn and scikit-learn libraries to evaluate loan and credit risk.

## Overview
Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Using credit card data from LendingClub, a peer-to-peer lending services company, this analysis utilizes Python's imbalanced-learn and scikit-learn libraries and employs the following techniques to train and evaluate machine learning models with unbalanced classes.

1. Oversampling with RandomOverSampler
2. Oversampling with Synthetic Minority Oversampling Technique (SMOTE)
3. Undersampling with ClusterCentroids
4. Oversampling and Undersampling with Synthetic Minority Oversampling Technique and Edit Nearest Neighbor (SMOTEENN)
5. BalancedRandomForestClassifier 
6. EasyEnsembleClassifier

A breakdown of the results generated by these machine learning models is provided below.

## Results
> Using the RandomOverSampler, SMOTE, ClusterCentroids and SMOTEEEN algorithms from the imblearn and sklearn libraries to resample the datasets, for the first four machine learning models below, we viewed the count of the target classes, trained a logistic regression classifier, calculated the balanced accuracy score, and then generated a confusion matrix and a classification report.

### 1. Oversampling with RandomOverSampler
To create this model, data was oversampled to yield 51,366 rows of data for the target category, credit risk. An image of the classification report is shown below:

<img width="608" alt="naive_oversampling_1" src="https://user-images.githubusercontent.com/104729703/192146597-176f406a-0626-4544-b4a3-0fe4797531e5.png">

* Balanced Accuracy Score: 0.6620175698580149     
* Precision Score (Avg): 0.99     
* Recall Score (Avg): 0.60 

The balanced accuracy score indicates that 66% of the model's predictions as to whether an individual's credit risk was low or high, were correct. The model shows a 99% precision score, indicating that the data contains a large number of true positives. The recall (sensitivity) score indicates that the classifier correctly predicted 60% of the positive cases in relation to all the positive cases in the dataset.

### 2. Oversampling with Synthetic Minority Oversampling Technique (SMOTE)
To create this model, data was oversampled to yield 51,366 rows of data for the target category, credit risk. An image of the classification report is shown below:

<img width="611" alt="SMOTE_oversampling_2" src="https://user-images.githubusercontent.com/104729703/192146607-f5268650-972b-4f9e-9369-2c518c29a7b4.png">

* Balanced Accuracy Score: 0.6568196079430206     
* Precision Score (Avg): 0.99     
* Recall Score (Avg): 0.70

The balanced accuracy score indicates that roughly 66% of the model's predictions as to whether an individual's credit risk was low or high, were correct. This model, like the previous model, also shows a 99% precision score, indicating that the data contains a large number of true positives. The recall (sensitivity) score in this model, however, shows a significant improvement over the first, and indicates that 70% of the positive cases in relation to the positive cases in the dataset were correctly predicted.

### 3. Undersampling with ClusterCentroids.
To create this model, data was undersampled to yield 246 rows of data for the target category, credit risk. An image of the classification report is shown below:

<img width="618" alt="Undersampling_3" src="https://user-images.githubusercontent.com/104729703/192146615-0de8d0ed-bcc5-43a8-a6a0-5303bca933e9.png">

* Balanced Accuracy Score: 0.5447339051023905     
* Precision Score: 0.99     
* Recall Score: 0.40

The balanced accuracy score indicates that roughly 54% of the model's predictions as to whether an individual's credit risk was low or high, were correct. This model, like the previous two models, also shows a 99% precision score, indicating that the data contains a large number of true positives. The recall (sensitivity) score in this model, however, shows a significant decrease over the first and second, and indicates that only 40% of the positive cases in relation to all the positive cases in the dataset were correctly predicted.

### 4. Oversampling and Undersampling with Synthetic Minority Oversampling Technique and Edit Nearest Neighbor (SMOTEENN)
To create this model, data was oversampled and undersampled in combination to yield 68,460 rows of data for the target category, credit risk. An image of the classification report is shown below:

<img width="599" alt="Combo_under_over_4" src="https://user-images.githubusercontent.com/104729703/192146623-a77526be-eb9e-43c3-8c7b-c9d772d6513c.png">

* Balanced Accuracy Score: 0.6461148570422992     
* Precision Score: 0.99     
* Recall Score: 0.57

The balanced accuracy score indicates that roughly 65% of the model's predictions as to whether an individual's credit risk was low or high, were correct. This model, like the previous three models, also shows a 99% precision score, indicating that the data contains a large number of true positives. The recall (sensitivity) score in this model, while comparable to the SMOTE model, indicates that 57% of the positive cases in relation to all the positive cases in the dataset were correctly predicted.

> Using the BalancedRandomForestClassifier and EasyEnsembleClassifier algorithms from the imblearn.ensemble library to train ensemble classifiers, for the subsequent two models below, we resampled the dataset, viewed the count of the target classes, trained the ensemble classifier (using 100 estimators for each model), calculated the balanced accuracy score, and then generated a confusion matrix and a classification report.

### 5. BalancedRandomForestClassifier 
To create this classifier, data was resampled to yield 68,470 rows of data for the target category, credit risk. An image of the classification report is shown below:

<img width="631" alt="balancedrandomforestclassifier_5" src="https://user-images.githubusercontent.com/104729703/192146631-3c961aa5-bc42-4b29-84fc-178146a02e5a.png">

* Balanced Accuracy Score: 0.782387479276459      
* Precision Score: 0.99     
* Recall Score: 0.88

The balanced accuracy score indicates that roughly 78% of the model's predictions as to whether an individual's credit risk was low or high, were correct. This model, like the previous three models, also shows a 99% precision score, indicating that the data contains a large number of true positives. The recall (sensitivity) score in this model indicates that 88% of the positive cases in relation to all the positive cases in the dataset were correctly predicted, outperforming all four of the previous models in both accuracy and precision.

### 6. EasyEnsembleClassifier
To create this classifier, data was resampled to yield 68,470 rows of data for the target category, credit risk. An image of the classification report is shown below:

<img width="602" alt="easyensembleclassifier_6" src="https://user-images.githubusercontent.com/104729703/192146640-76892a7f-1695-43ed-b5aa-666711929bed.png">

* Balanced Accuracy Score: 0.9316600714093861     
* Precision Score: 0.99     
* Recall Score: 0.94

The balanced accuracy score indicates that roughly 93% of the model's predictions as to whether an individual's credit risk was low or high, were correct. This model, like the previous three models, also shows a 99% precision score, indicating that the data contains a large number of true positives. The recall (sensitivity) score in this model indicates that 94% of the positive cases in relation to all the positive cases in the dataset were correctly predicted, outperforming all five of the previous models in both accuracy and precision.

## Summary
Our initial view of the data showed that 68,470 rows were classified as having a low credit risk, and only 347 were classified as having a high credit risk (less than 1%). This imbalance can explain our unanimous 99% precision scores across all our models, which were all very good at predicting when credit risk would be low, but did not perform well in their prediction of when credit risk would be high.

The six models above show a uniformly high average precision, with variation in the accuracy and recall. While the EasyEnsembleClassifier model showed the highest accuracy score and the highest recall score, a 93% accuracy rate can be indicative of an overfit model, meaning that the model is very good at predicting data for our dataset, but might not perform as well when presented with another dataset.

If the goal of our model is to be able to predict when a person will present a high-credit risk, it's worth underscoring that none of the above models performed this task well. Looking at the precision rate for the "high-risk" feature in the classification reports above, the EasyEnsemble model had the highest score for this, but even this score was less than 10%, which does not meet the standard of a successful model.

We should be evaluating our model's performance by its ability to return True Negatives, that is, the model's ability to predict that a person is a high credit risk when they are in fact a high credit risk.

For all the reasons mentioned above, **it is our recommendation that none of the above models be used to predict high credit risk**. For further testing, it would be my recommendation to utilize stratification in resampling the data, which can be important when the imbalance is large and the dataset is small.  
