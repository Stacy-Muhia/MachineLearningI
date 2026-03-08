# Toxicity Prediction Using Machine Learning

## Project Overview
This project explores the use of machine learning to classify chemical compounds as toxic or non toxic using molecular descriptor data. The dataset contains many numerical features that describe the structural and chemical properties of molecules. The goal is to train models that can learn patterns in these descriptors and accurately predict toxicity.

## Dataset
The dataset contains records of chemical compounds and their molecular descriptors. Each row represents a compound and each column represents a descriptor describing a specific chemical property.

The target variable is Class which indicates whether the compound is Toxic or NonToxic.

## Project Steps

### Data Loading
The dataset was loaded using pandas and the structure of the data was examined to understand the number of records and features.

### Exploratory Data Analysis
Exploratory analysis was performed to understand the distribution of features and the target variable. Missing values, variance of features, and correlations between features were examined.

### Data Preprocessing
Several preprocessing steps were applied to prepare the data for machine learning.

Column names were cleaned to remove extra spaces.  
The target variable was encoded into binary format.  
Highly correlated features were removed to reduce redundancy.  
Low variance features were removed because they do not provide useful information.  
Feature scaling and imputation were applied where necessary.

### Feature Selection
Because the dataset contains a large number of features, feature selection was performed using mutual information to identify the most informative features for prediction.

### Model Training
Two machine learning models were trained for this task.

Random Forest  
XGBoost

These models are suitable for high dimensional datasets and are able to capture complex relationships between features.

### Model Evaluation
Nested cross validation was used to evaluate model performance. The outer loop was used to estimate generalization performance while the inner loop performed hyperparameter tuning using grid search.

The models were evaluated using accuracy and weighted F1 score.

## Results
Both models were able to learn patterns in the molecular descriptors and classify compounds based on toxicity. The evaluation metrics across cross validation folds provide an estimate of how well the models generalize to unseen data.

## Technologies Used
Python  
Pandas  
NumPy  
Matplotlib  
Seaborn  
Scikit learn  
XGBoost  
Google Colab

## Author
Stacy Muhia
