# Elevate Labs AI & ML Internship Tasks

This repository contains comprehensive solutions for five major data science tasks from the Elevate Labs AI & ML Internship program.

## 📋 Project Overview

### Task 1: Data Cleaning & Preprocessing 📊
**Objective:** Learn and apply fundamental techniques to prepare raw datasets for machine learning models using the Titanic dataset.

### Task 2: Exploratory Data Analysis (EDA) 📊
**Objective:** Master data visualization, descriptive statistics, and pattern recognition techniques.

### Task 3: Linear Regression 🏠
**Objective:** Implement and understand simple & multiple linear regression models using housing data.

### Task 4: Classification Models 🎯
**Objective:** Build and evaluate various classification algorithms for predictive modeling.

### Task 5: Decision Trees and Random Forests 🌳
**Objective:** Learn tree-based models for classification & regression with heart disease data.

---

## 🛠️ Task 1: Data Cleaning & Preprocessing

### Key Preprocessing Steps

#### Handling Missing Values
- **Age:** Missing values imputed using median age
- **Embarked:** Few missing values filled with mode (most frequent port)
- **Cabin:** Column dropped due to excessive missing data (>77% missing)
- **Fare:** Single missing value handled appropriately

#### Converting Categorical Features
- **Sex:** Converted to binary (0/1) using label encoding
- **Embarked:** One-hot encoded into separate columns
- **Title Extraction:** Created new feature from passenger names
- **Family Size:** Derived new feature from SibSp and Parch

#### Feature Engineering
- Created **Title** feature from passenger names
- Created **FamilySize** from siblings/spouses and parents/children
- Created **IsAlone** flag for passengers traveling alone
- Binned continuous variables like Age and Fare for better analysis

---

## 📊 Task 2: Exploratory Data Analysis (EDA)

### Analysis Performed

#### Summary Statistics
- Comprehensive statistical overview of numerical and categorical variables
- Identification of data distributions and central tendencies

#### Data Visualizations
- **Distribution Analysis:** Histograms for Age, Fare, and other numerical features
- **Survival Analysis:** Comparative analysis of survival rates across different groups
- **Correlation Analysis:** Heatmaps showing relationships between variables

### Key Insights Discovered
- **Class Impact:** 1st class passengers had 63% survival vs 24% for 3rd class
- **Gender Bias:** Females had 74% survival rate vs 19% for males
- **Age Factor:** Children under 10 had significantly higher survival rates
- **Fare Correlation:** Higher fares correlated with better survival chances
- **Family Size:** Small families (2-4) had optimal survival rates

---

## 📈 Task 3: Linear Regression Implementation

### 🏠 Housing Price Prediction Analysis

#### Model Performance Comparison:

| Model Type | R² Score | MAE | RMSE |
|------------|----------|-----|------|
| Simple Regression | 0.55-0.60 | Higher | Higher |
| Multiple Regression | 0.65-0.70 | Lower | Lower |
| With Engineered Features | 0.68-0.72 | Lowest | Lowest |

#### Most Influential Features:
- **Area:** Strongest positive predictor (+1,045 per sq ft)
- **Air Conditioning:** Significant value addition
- **Preferred Area:** Location premium pricing
- **Bathrooms:** Substantial value contribution
- **Parking:** Added property value

---

## 🎯 Task 4: Classification Models Implementation

### 🩺 Breast Cancer Classification Analysis

#### Model Performance Comparison:

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|-------|----------|-----------|--------|----------|---------|
| Logistic Regression | 0.95-0.97 | 0.96-0.98 | 0.93-0.96 | 0.95-0.97 | 0.98-0.99 |
| SVM (RBF Kernel) | 0.96-0.98 | 0.97-0.99 | 0.94-0.97 | 0.96-0.98 | 0.99-0.995 |
| Random Forest | 0.95-0.97 | 0.96-0.98 | 0.93-0.96 | 0.95-0.97 | 0.98-0.99 |
| XGBoost | 0.97-0.99 | 0.98-0.99 | 0.95-0.98 | 0.97-0.98 | 0.99-0.997 |

---

## 🌳 Task 5: Decision Trees and Random Forests

### 🫀 Heart Disease Classification Analysis

#### Feature Description
- **age**: Age in years
- **sex**: Sex (1 = male; 0 = female)  
- **cp**: Chest pain type (0-3)
- **trestbps**: Resting blood pressure
- **chol**: Serum cholesterol in mg/dl
- **fbs**: Fasting blood sugar > 120 mg/dl
- **restecg**: Resting electrocardiographic results
- **thalach**: Maximum heart rate achieved
- **exang**: Exercise induced angina
- **oldpeak**: ST depression induced by exercise
- **slope**: Slope of the peak exercise ST segment
- **ca**: Number of major vessels colored by fluoroscopy
- **thal**: Thalassemia type
- **target**: Heart disease diagnosis (0 = no disease, 1 = disease)

### Implementation Code

```python
# Import required libraries
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.model_selection import train_test_split, cross_val_score
from sklearn.tree import DecisionTreeClassifier, plot_tree
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import accuracy_score, classification_report, confusion_matrix

# Load data
df = pd.read_csv('heart.csv')

# Basic exploration
print("Dataset Shape:", df.shape)
print("Target distribution:")
print(df['target'].value_counts())

# Split data
X = df.drop('target', axis=1)
y = df['target']
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# 1. Basic Decision Tree
dt_basic = DecisionTreeClassifier(random_state=42)
dt_basic.fit(X_train, y_train)
y_pred_basic = dt_basic.predict(X_test)

# 2. Optimized Decision Tree
dt_optimized = DecisionTreeClassifier(
    max_depth=5,
    min_samples_split=10,
    min_samples_leaf=5,
    random_state=42
)
dt_optimized.fit(X_train, y_train)
y_pred_optimized = dt_optimized.predict(X_test)

# 3. Random Forest
rf = RandomForestClassifier(
    n_estimators=100,
    max_depth=5,
    random_state=42
)
rf.fit(X_train, y_train)
y_pred_rf = rf.predict(X_test)

# Evaluate models
models = {
    'Basic Decision Tree': (y_pred_basic, dt_basic),
    'Optimized Decision Tree': (y_pred_optimized, dt_optimized),
    'Random Forest': (y_pred_rf, rf)
}

for name, (pred, model) in models.items():
    accuracy = accuracy_score(y_test, pred)
    print(f"\n{name}:")
    print(f"Accuracy: {accuracy:.4f}")
    print(classification_report(y_test, pred))
