# Fraud-Detection-in-Online-Payments 

In this article, we employ different machine learning models to identify fraud from online transactions data. The data comes from Kaggle, ["Online Payments Fraud Detection Dataset"](https://www.kaggle.com/datasets/rupakroy/online-payments-fraud-detection-dataset?resource=download), and has the following columns:

* `step`: represents a unit of time where 1 step equals 1 hour
* `type`: type of online transaction
* `amount`: the amount of the transaction
* `nameOrig`: customer starting the transaction
* `oldbalanceOrg`: balance before the transaction
* `newbalanceOrig`: balance after the transaction
* `nameDest`: recipient of the transaction
* `oldbalanceDest`: initial balance of recipient before the transaction
* `newbalanceDest`: the new balance of recipient after the transaction
* `isFraud`: fraud transaction

In this classification problem, our target variable is `isFraud`. Unsurprisingly, it is imbalanced where we only have 8,213 cases of fraud out of roughly 6.36 million onservations. Thus we implement  under sampling method to balance out fraud observations however we retain the skewed distribution by keep the majority class to have five times more observations than the minority class. We then split the data into training set (60 percent) and testing set (40 percent) and standardize the data. 

We apply different classification models:

* Logistics Regression
* Support Vector Machine (SVM)
* Random Forest
* Naive Bayes
* Artificial Neural Networks (ANN)

We especially have high performance expectations for SVM and ANN as they historically performed well with imbalanced data and skewed distributions. The performance metrics to be compared across models in this analysis includes the confusion matrix, accuracy score, and the ROC curve.  
All models perform well with accuracy over 90 percent and AUC over 93 percent. According to the performance metrics, particularly the accuracy scores, ANN (accuracy = 0.9755) significantly outperforms other models, followed by random forest (accuracy - 0.9528).

Analysis can also be accessed via Google Colab at https://colab.research.google.com/drive/1QeMHHsWcApAi2Id_ov4SdTIaBUsKevq0?usp=sharing.

