# stroke-prediction
This project aims to build a predictive model to predict the likelihood of a patient having stroke based on some health parameters.
# Overview:
Stroke is one of the leading causes of death around the world today, and early prediction is very importantfor timely medical intervention. This project leverages machine learning techniques to predict the likelihood of a stroke based on a dataset that includes various health metrics like age, hypertension, heart disease, and more.
The objective is to provide a tool that can help healthcare professionals and researchers understand the key risk factors associated with strokes and predict the risk effectively.
# Data
the data set used for this project was collected from Kaggle https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset. it includes the following features:
1. id: unique identifier
2. gender: "Male", "Female" or "Other"
3. age: age of the patient
4. hypertension: 0 if the patient doesn't have hypertension, 1 if the patient has hypertension
5. heart_disease: 0 if the patient doesn't have any heart diseases, 1 if the patient has a heart disease
6. ever_married: "No" or "Yes"
7. work_type: "children", "Govt_jov", "Never_worked", "Private" or "Self-employed"
8. Residence_type: "Rural" or "Urban"
9. avg_glucose_level: average glucose level in blood
10. bmi: body mass index
11. smoking_status: "formerly smoked", "never smoked", "smokes" or "Unknown"*
12. stroke: 1 if the patient had a stroke or 0 if not
*Note: "Unknown" in smoking_status means that the information is unavailable for this patient
# Data Preprocessing
### Data cleaning
the bmi column contains null values, the fillna techniques was used to replace missing values with the mean.
convert the categorical column to category and find the statistics of the numerical features.
# Exploratory Data Analysis
age was further grouped into:
Adolescence 15-19
Young Adult 20-39
Adult 40-64
middle Age 65-74
older 75..
from the grouping individuals who are grouped into adolescence do not have stroke both male and female while individuals who fall into the group of older adults have high number of stroke patients
the correlation between avg_glucose, bmi and age was plotted using scatterplot to discover the relationship between this numerical features and i discovered that there is more people in middle age and older have high glucose level

# Feature Engineering
### Label Encoding
Label Encoder is used to convert categorical data in the dataset to numerical values that can be undserstood by machine learning algorithms, the labels include:
1. gender: "Male", "Female" or "Other"
2. ever_married: "No" or "Yes"
3. work_type: "children", "Govt_jov", "Never_worked", "Private" or "Self-employed"
3. Residence_type: "Rural" or "Urban"
3. smoking_status: "formerly smoked", "never smoked", "smokes" or "Unknown"*
## Feature selection
the best features are selected using the selectKbest library in sklearn, the chi2 was passed as the score function to determine the best features

# Modelling
the data was split into train and test data with 20% for test and a randomstate of 42
## models:
1. Random Forest Classifier: achieved a accuracy of 94 precent
2. Logistic Regression achived a accuracy of 94 percent
3. K nearest Neighbor: achieved a accuracy of 94 percent
4. Support vector machine: achieved a accuracy of 94 percent
## overfitting:
i used the learning curve to check for overfitting in each model
from the learning curve for random forest classifier the is overfitiing as the train score is higher than the test score

# Results
I choose the Logistic Regression model
it is fast and simple for binary classification problem
the model is able to generalize well
it is resource less intensive


