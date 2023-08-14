# Data-Analysis-Machine-Learning

"Stroke_prediction" is a dataset used to predict if patient is likely to get stroke based on the informations like
gender, age, various diseases, smoking status and bmi.

Preprocessing the Data.
After reading CSV file into Pandas DataFrame, I searched for missing values by plotting graph,
as BMI column has the most missing values  I using mean imputation method. 
Using round() I round off Age to become int64 Dtype, I have removed record of other in column Sex.
I visualize the relationships between categorical variables and the target variable. 
Gender pie chart represents the distribution of genders where we can noticed female are more likely to get stroke. 
Smoking Status pie chart represents the distribution of smoking statuses. 37% of instances never smoked.

Preparing the Data for Prediction.
Converting the Categorical Columns into Numerical by Mapping each category to an integer value using map() on pandas series object
Checking if data is balanced, unfortunatelly data is imbalanced  which will result in a bad model. To resolve this issue I use 
SMOTE to balance it, then spliting the Data in Training and Testing Samples. I decided to create a model for stroke prediction
using Random Forest Classifier because is effective in handling complex datasets and provide accurate predictions. Random forest is 
also less prone to overfitting and can handle imbalanced data more effectively by giving equal importance to both classes during tree
construction.
