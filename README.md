# stroke-prediction
This project aims to build a predictive model to predict the likelihood of a patient having stroke based on some health parameters.
# Overview:
Stroke is one of the leading causes of death around the world today, and early prediction is very importantfor timely medical intervention. This project leverages machine learning techniques to predict the likelihood of a stroke based on a dataset that includes various health metrics like age, hypertension, heart disease, and more.
The objective is to provide a tool that can help healthcare professionals and researchers understand the key risk factors associated with strokes and predict the risk effectively.
# Data
the data set used for this project was collected from Kaggle https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset. it includes the following features:


# Features
gender, age, hypertension, heart_disease, ever_married, work_type, Residence_type, avg_glucose, BMI(body mass index), smoking status
# Methods
I used the logistic Regression machine learning algorithm to develop the prediction model. The algorithm was trained on 80% of the dataset and tested on 20%.
Feature selection was performed on the dataset to get the best features which are the new features is 'age', 'hypertension', 'heart_disease', 'ever_married', 'avg_glucose_level' on which the dataset was trained
# Results
the model achieved an accuracy score of 93.93%
