# Data Analysis Machine Learning Repository

Welcome to the Data Analysis Machine Learning Repository 🧠

This is my inaugural machine learning project, showcasing my journey into the world of data and algorithms.
As a beginner in this field, I'm eagerly learning and striving to cultivate my skills further, with the aspiration to contribute meaningfully to the realm of machine learning.


## Table of Contents
- [Introduction]
- [Projects]
- [Resources]
- [Exploratory Data Analysis]
- [Data Preprocessing]
- [Modeling]


## Introduction

Did you know... 80% Heart strokes are preventable?
According to the World Health Organization (WHO) stroke is the 2nd leading cause of death globally, responsible for approximately 11% of total deaths. 
This dataset is used to predict whether a patient is likely to get stroke based on the input parameters like gender, age, various diseases, and smoking status. 
Each row in the data provides relavant information about the patient.


## Projects

Here are list of the data analysis machine learning projects included in this repository:

- Stroke_prediction

project contains the following:

- **Notebooks:** Jupyter notebooks with the code used for DAML
- **Results:** Visualizations, charts, and any other outputs generated from the analysis.


## Resources


- **Languages:** Python 🐍
- **Libraries:** Pandas🐼, Numpy🧮, Matplotlib📊, Seaborn🌈, Scikit-learn🤖, Imbalanced-learn ⚖️ etc.
- **Machine Learning Model:** Random Forest Classifier 🌳🌲
- **Tools:** Jupyter Notebook 📓 


## Exploratory Data Analysis

- **Problem:**
Binary classification problem.
Make prection on the target variable STROKE

- **Attribute Information:**

  Categorical variables: gender, ever_married	work_type,	Residence_type, smoking_status

  
  Numerical variables: hypertension,	heart_disease, avg_glucose_level,	bmi, stroke



After reading a CSV file into a DataFrame, I searched for missing values by plotting graph. As the 'BMI' column had the most missing values,
I decided to use the "mean imputation" method. 'Age' column contain float numbers, using the round() function I rounded off the values to become an int64 Dtype. 
I also removed record from the 'Sex' column for other gender as I strongly believe one position wont effect predictions.

- **Data Visualization:**

-Gender distribution via pie chart


It's noticeable that females are more likely to experience strokes with ratio of 58,6% compared to males 41.4%.


-Smoking status distribution via pie chart


When it comes to stroke & smoking_status, people that have never smoked 37% are most susceptible. Surprisingly, people that smokes 15.4% have the lowest chances of suffering from stroke. 30.2% hasnt given answer on this question.


-Stroke distribution via pie chart


This is a highly unbalanced data distribution, indicates that every 5 people out of 100 are having strokes, before using any modeling this should be solve as most of the machine learning algorithm do not work well with the imbalanced data.


-Heart_disease & Hypertension distribution via barplot


Hypertension and heart disease features are slightly correlated to stroke.


## Data Preprocessing



Converting the Categorical Columns into Numerical by Mapping each category to an integer value using map() on pandas series object
Checking if data is balanced, as mentioned earlier  data is imbalanced  which will result in a bad model. To resolve this issue I use 
SMOTE to balance it, then spliting the Data in Training and Testing Samples. 


## Modeling

I decided to create a model for stroke prediction using Random Forest Classifier because is effective in handling complex datasets and provide accurate predictions. 
Random forest is also less prone to overfitting and can handle imbalanced data more effectively by giving equal importance to both classes during tree construction.


