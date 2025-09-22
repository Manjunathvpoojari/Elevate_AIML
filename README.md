
# Task 1: Data Cleaning & Preprocessing 📊
This repository contains the solution for 

Task 1: Data Cleaning & Preprocessing from the Elevate Labs AI & ML Internship. The objective of this task was to learn and apply fundamental techniques to prepare a raw dataset for machine learning models.


The project focuses on the 

Titanic Dataset, a well-known dataset for practicing data cleaning and preprocessing.

**Key Preprocessing Steps** 🛠️
The following steps were performed to transform the raw data into a clean, model-ready format:


Handling Missing Values: Missing data was addressed in several columns. The 

Age column's missing values were imputed using the median, while the few missing values in the Embarked column were filled with the mode. The Cabin column was dropped due to a high volume of missing data.


Converting Categorical Features: Categorical features were converted into a numerical format. The 

Sex column was encoded using a simple mapping (Label Encoding), and the Embarked column was converted using One-Hot Encoding to avoid any ordinal bias.


Outlier Detection and Removal: Outliers in the Fare column were identified using a boxplot  and subsequently removed using the Interquartile Range (IQR) method.


Feature Scaling: The numerical features (Age, Fare, SibSp, Parch) were standardized using StandardScaler to ensure they were on a consistent scale for the machine learning algorithm.

Repository Contents 📂
Titanic-Dataset.csv: The original, raw dataset.

data_preprocessing.ipynb: The Python code used for the data cleaning and preprocessing steps.

