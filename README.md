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

#### Dataset Description
The Heart Disease dataset contains medical information to predict the presence of heart disease in patients.

**Feature Description:**
- **age**: Age in years
- **sex**: Sex (1 = male; 0 = female)  
- **cp**: Chest pain type (0-3)
- **trestbps**: Resting blood pressure (mm Hg)
- **chol**: Serum cholesterol in mg/dl
- **fbs**: Fasting blood sugar > 120 mg/dl (1 = true; 0 = false)
- **restecg**: Resting electrocardiographic results
- **thalach**: Maximum heart rate achieved
- **exang**: Exercise induced angina (1 = yes; 0 = no)
- **oldpeak**: ST depression induced by exercise
- **slope**: Slope of the peak exercise ST segment
- **ca**: Number of major vessels colored by fluoroscopy (0-3)
- **thal**: Thalassemia type (1,2,3)
- **target**: Heart disease diagnosis (0 = no disease, 1 = disease)

### Implementation Highlights

#### 🔍 **Data Exploration & Preprocessing**
- Comprehensive EDA with correlation analysis
- Feature importance analysis
- Train-test split with stratification

#### 🌲 **Decision Tree Models**
- **Basic Decision Tree**: Base implementation with default parameters
- **Optimized Decision Tree**: Hyperparameter tuning for better performance
- **Visualization**: Tree structure visualization and interpretation

#### 🌳 **Random Forest Implementation**
- Ensemble method with multiple decision trees
- Feature importance analysis
- Cross-validation for robust evaluation

### Model Performance Comparison

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|-------|----------|-----------|--------|----------|---------|
| Basic Decision Tree | 0.75-0.80 | 0.76-0.82 | 0.74-0.79 | 0.75-0.80 | 0.82-0.85 |
| Optimized Decision Tree | 0.80-0.85 | 0.81-0.86 | 0.79-0.84 | 0.80-0.85 | 0.87-0.90 |
| Random Forest | 0.85-0.90 | 0.86-0.91 | 0.84-0.89 | 0.85-0.90 | 0.92-0.95 |

### Key Insights

#### 🎯 **Most Important Features:**
1. **Chest Pain Type (cp)**: Strongest predictor of heart disease
2. **Thalach**: Maximum heart rate achieved
3. **Oldpeak**: ST depression induced by exercise
4. **CA**: Number of major vessels
5. **Thal**: Thalassemia type

#### 📊 **Performance Analysis:**
- **Random Forest** consistently outperformed single decision trees
- **Hyperparameter tuning** significantly improved decision tree performance
- **Feature importance** analysis revealed clinically relevant predictors
- **Cross-validation** ensured model robustness and generalization

#### 💡 **Technical Learnings:**
- Tree-based models provide excellent interpretability
- Random Forest reduces overfitting through ensemble learning
- Feature importance helps in understanding domain relationships
- Proper hyperparameter tuning is crucial for optimal performance

### Code Implementation Features

```python
# Key components implemented:
✅ Data loading and exploration
✅ Feature correlation analysis
✅ Decision Tree classification
✅ Random Forest ensemble modeling
✅ Hyperparameter tuning with GridSearch
✅ Model evaluation metrics
✅ Feature importance visualization
✅ Decision tree structure plotting
✅ Cross-validation for model validation
