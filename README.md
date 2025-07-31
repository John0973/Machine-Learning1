## Machine-Learning1

## Table of Content
-[Project Objective] (#project-objective)
-[Data Source]
-[Exploratory Data Analysis] (#Exploratory-Data Analysis)
-[Feature Engineering] (#Feature-Engineering)
-[Data Preprocessing] (#Data-Preprocessing)
-[Machine Learning Model] (#Machine-Learning-Model)
-[Evaluation Metrics] (#Evaluation-metrics)
-[Key insights] (#Key-insights)
-[Conclusions] (#Conclusions)

## Project Objective
The Primary Objective of this Project is to determine whether price sensitivity is the cause of customer churn, identify the key drivers behind Churn, and recommend a strategy to reduce Churn and improve retention.

## Data Source
The Data used in this project was provided by BCG X for a company called PowerCo (A leading Power Company), with features like "date_end, date_modif_prod,	date_renewal," etc.

## Exploratory Data Analysis
EDA was performed to uncover different patterns in the datasets. The Datasets had 14606 entries in the client Data and 193002 entries in the price data. No Null and duplicate Values were recorded. Univariate, Bivariate, and Multivariate Analysis were performed to uncover different patterns in the Datasets.

## Feature Engineering
Feature engineering was performed to enhance the robustness of the Datasets in getting quality insights. Feature engineering like "Difference between off-peak prices in Dec and Jan, Difference between peak prices in Dec and Jan, Difference in Average Prices across all Regions, Maximum Price changes across periods and Months". This feature is engineered to help us better understand price sensitivity to churn and overall model building.

## Data Preprocessing
During Data Preprocessing, the Target Feature was noticed to be heavily imbalanced, with variable 0 being 13187 and variable 1 being 1419. Encoding of Categorical features was not performed at this stage as no Categorical variable was present. Scaling was performed on the Numerical variables by using a RobustScaler technique.

## Machine Learning 
A machine learning algorithm was used to train the model. The project categorically stated that a RandomForestClassifier should be used. The training and test Data were split 80:20.

## Evaluation Metrics.
Different evaluation metrics were considered before final acceptance of the Model.

-- Accuracy-- The ratio of correctly predicted observations to the total observations.

-- Precision-- The ability of the classifier not to label a negative sample as positive.

-- Recall-- The ability of the classifier to find all the positive samples.

## Key Insights
As randomForestClassifier was used as our Baseline model and the model we are using. Our recall on both classes for class 0 was 0.99847, and class 1 was 0.05574. Accuracy was 0.90007, which is a high Accuracy, but did not explain the whole scenario. The False Negative was 288, which can still be improved on. 

Class weight of {0:1, 1:6} was used to improve the minority class, while the model was retrained. We had a slight improvement in the false Negative from 288 to 286 after class_weight.

We went further by applying the SMOTE technique by oversampling the minority class to have equal class balance, and the model was retrained. Recall on both class 0, now 0.97992, and class 1, 0.92527, Accuracy at 0.95261. False Negative is now 197.

Feature Importances was done to know the features that contributed most to Customer's Churn and determine if Price is sensitive to Customer's Churn as well.

## Conclusion.
PowerCo’s churn is influenced by customer behavior and lifestyle rather than pricing as assumed, with the improved model built, customers likely to churn can be identified earlier and engage them effectively beyond pricing strategy to customer personalisation.




