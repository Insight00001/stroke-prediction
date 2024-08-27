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
### Label Encoding
Label Encoder is used to convert categorical data in the dataset to numerical values that can be unserstood by machine learning algorithms, the labels include:
1. gender: "Male", "Female" or "Other"
2. ever_married: "No" or "Yes"
3. work_type: "children", "Govt_jov", "Never_worked", "Private" or "Self-employed"
3. Residence_type: "Rural" or "Urban"
3. smoking_status: "formerly smoked", "never smoked", "smokes" or "Unknown"*

# Methods
I used the logistic Regression machine learning algorithm to develop the prediction model. The algorithm was trained on 80% of the dataset and tested on 20%.
Feature selection was performed on the dataset to get the best features which are the new features is 'age', 'hypertension', 'heart_disease', 'ever_married', 'avg_glucose_level' on which the dataset was trained
# Results
the model achieved an accuracy score of 93.93%
