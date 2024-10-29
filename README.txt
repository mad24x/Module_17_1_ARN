Comparing Classifiers for Marketing Bank Products

Business Understanding
The goal of this analysis is to evaluate and compare the performance of various classification algorithms (K Nearest Neighbors, Logistic Regression, Decision Trees, and Support Vector Machines)
in predicting customer responses to marketing campaigns by a Portuguese banking institution. The objective is to identify potential customers likely to subscribe to a term deposit, 
thereby optimizing marketing strategies and improving acquisition rates.

Data Cleaning
The dataset was sourced from the UCI Machine Learning Repository and contains information on various demographic and behavioral attributes of customers. 


The following steps were taken to clean and preprocess the data:
Handled Missing Values: 
	Identified and imputed or removed rows with missing values to ensure data integrity.
Data Type Conversion: 
	Converted categorical variables to numeric using one-hot encoding for effective model training.
Feature Scaling: 
	Applied standard scaling to ensure that the features are on the same scale, especially for distance-based algorithms like KNN.


Statistical Analysis
Descriptive Statistics
	Train Accuracy: Indicates how well the model fits the training data.
	Test Accuracy: Measures the model's ability to generalize to unseen data.


Summary of Findings
Model				TrainTime	Train Accuracy	Test Accuracy
Logistic Regression	0.067 s		88.69%			88.35%
KNN					0.000 s		89.44%			87.30%
Decision Tree		0.312 s		95.29%			82.99%
SVM					16.23 s		88.76%			88.30%
KNN_tuned			0.002 s		88.97%			87.76%
Decision_tree_tuned	0.020 s		88.81%			88.32%
Log_tuned			0.149 s		88.70%			88.36%
SVC_tuned			3.270 s		88.66%			88.28%


Key Insights:
High Train Accuracy: 
	The Decision Tree model showed the highest train accuracy (95.29%), indicating overfitting, as it performed significantly better on the training data than on the test data (82.99%).
Consistent Performance: 
	Logistic Regression and SVM models displayed stable test accuracies (88.35% and 88.30%, respectively), suggesting they generalize well to unseen data.
Effect of Hyperparameter Tuning: 
	Tuning the models showed minimal improvements in accuracy, particularly for KNN and SVM, indicating that the base models were already performing well.
	It was noticed that adding in additional parameter choices for the models started to make the run time to long to create the models.  


Actionable Items
	Optimize Marketing Targeting: Use the Logistic Regression and SVM models to identify and target customers likely to subscribe, increasing efficiency in marketing efforts.
	Model Deployment: Consider deploying the Logistic Regression model for real-time predictions due to its robust performance and low training time.
	Future Model Development: Investigate additional models or feature engineering to enhance predictive capabilities.

Next Steps and Recommendations
	Further Feature Analysis: Conduct exploratory data analysis to understand feature importance and interactions better.
	Ensemble Methods: Experiment with ensemble methods like Random Forest or Gradient Boosting to improve prediction accuracy.
	Periodic Model Updates: Regularly update models with new data to adapt to changing customer behaviors and marketing strategies.
	Business Integration: Collaborate with marketing teams to integrate model predictions into campaign strategies for effective resource allocation.