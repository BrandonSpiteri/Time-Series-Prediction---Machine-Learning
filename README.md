# Data Scientist - Technical Test

Technical Test which uses machine learning modelling to perform time-series forecasting in Python 3.6. 

The dataset consists of 2 features:
1. Date
2. Value

# Feature Engineering 
Seanality Features are modelled by extracting the Month, Day of Month, Day of Week and Year for each instance as features. This captures any trends in 'value' in relation to the date.

The preceeding 20 day values are used as input features, to capture price history memory in each row. 

The rolling 10 day mean and standard deviation are calculated and used as input features. The latter captures the variance of the rolling 10 day window. 

# Model Training
A moving window mechanicsm is used, which 200 instances are used as training set, and the next day (d) is predicted. The window moves by one day, and predicts the following day (d+1). 

# Models Trained
1. Linear Regression
2. ElasticNet
3. SGDRegressor

# Results
| Model  | R2_Score(%) | RMSE | Note |
| ------------- | ------------- | ------------- | ------------- |
| Linear Regression	  | 36.01  | 28874.251778	| Basic Dataframe | 
| Linear Regression	| 75.56	| 17845.382889	| Enhanced Dataframe |
| Elastic Net	| 74.15	| 18353.240225	| Enhanced Dataframe |
| SGD Regressor	| 74.29	| 18301.823954 |	Enhanced Dataframe |

# Libraries
matplotlib==3.2.1 

seaborn==0.11.1

scikit-learn==0.24.1

pandas==1.1.5

numpy==1.19.2

python==3.6.0
