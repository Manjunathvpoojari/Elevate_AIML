
# Task 1: Data Cleaning & Preprocessing 📊
# Task 2: Exploratory Data Analysis (EDA)📊
This repository contains the solution for 

Task 1: Data Cleaning & Preprocessing from the Elevate Labs AI & ML Internship. The objective of this task was to learn and apply fundamental techniques to prepare a raw dataset for machine learning models.

Task 2: Exploratory Data Analysis (EDA) from the Elevate Labs AI & ML Internship. The objective of this task was to learn Data visualization, descriptive statistics, pattern recognition.


# 📋 Project Overview
The Titanic dataset contains information about passengers aboard the RMS Titanic, with the goal of predicting survival based on various features. This project demonstrates comprehensive data preprocessing and exploratory analysis techniques.


# 🛠️ Task 1: Data Cleaning & Preprocessing
Key Preprocessing Steps
1. Handling Missing Values
- Age: Missing values imputed using median age

- Embarked: Few missing values filled with mode (most frequent port)

- Cabin: Column dropped due to excessive missing data (>77% missing)

- Fare: Single missing value handled appropriately

2. Converting Categorical Features
- Sex: Converted to binary (0/1) using label encoding

- Embarked: One-hot encoded into separate columns

- Title Extraction: Created new feature from passenger names

- Family Size: Derived new feature from SibSp and Parch

3. Feature Engineering
- Created Title feature from passenger names

- Created FamilySize from siblings/spouses and parents/children

- Created IsAlone flag for passengers traveling alone

- Binned continuous variables like Age and Fare for better analysis

4. Data Type Corrections
- Ensured proper data types for all columns

- Handled numerical and categorical variables appropriately

---

# 📊 Task 2: Exploratory Data Analysis (EDA)
Analysis Performed
1. Summary Statistics
- Comprehensive statistical overview of numerical and categorical variables

- Identification of data distributions and central tendencies

2. Data Visualizations
- Distribution Analysis: Histograms for Age, Fare, and other numerical features

- Survival Analysis: Comparative analysis of survival rates across different groups

- Correlation Analysis: Heatmaps showing relationships between variables

3. Key Insights Discovered
- Class Impact: 1st class passengers had 63% survival vs 24% for 3rd class

- Gender Bias: Females had 74% survival rate vs 19% for males

- Age Factor: Children under 10 had significantly higher survival rates

- Fare Correlation: Higher fares correlated with better survival chances

- Family Size: Small families (2-4) had optimal survival rates

4. Advanced Analysis
- Survival rates by multiple factors (class × gender × age)

- Family structure impact on survival

- Embarkation port analysis

.
# 📈 Key Findings
Data Quality Issues Identified:
- 177 missing values in Age column (20% of data)

- 687 missing values in Cabin column (77% of data)

- 2 missing values in Embarked column

- Survival Patterns:
- Overall survival rate: 38.4%

- Strong "women and children first" protocol evidence

- Significant class-based survival disparities

Feature Correlations:
+ Strong negative correlation between Pclass and Survival (-0.34)

+ Positive correlation between Fare and Survival (0.26)

+ Weak correlation between Age and Survival (-0.08)


📚 Lessons Learned
* Data Quality Assessment: Importance of thorough missing value analysis

* Feature Engineering: Creating meaningful features from raw data

* Visual Storytelling: Using plots to uncover hidden patterns

* Statistical Insights: Correlation analysis and hypothesis testing

* Documentation: Maintaining clear documentation throughout the process

# Repository Contents 📂
Titanic-Dataset.csv: The original, raw dataset.

Elevate_labs(AIML task1)\data_preprocessing.ipynb: The Python code used for the data cleaning and preprocessing steps.
Elevate_labs(AIML task2)\EDA_titanic.ipynb:  Exploratory Data Analysis

