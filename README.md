# Elevate Labs AI & ML Internship Tasks

This repository contains comprehensive solutions for four major data science tasks from the Elevate Labs AI & ML Internship program.

## 📋 Project Overview

### Task 1: Data Cleaning & Preprocessing 📊
**Objective:** Learn and apply fundamental techniques to prepare raw datasets for machine learning models using the Titanic dataset.

### Task 2: Exploratory Data Analysis (EDA) 📊
**Objective:** Master data visualization, descriptive statistics, and pattern recognition techniques.

### Task 3: Linear Regression 🏠
**Objective:** Implement and understand simple & multiple linear regression models using housing data.

### Task 4: Classification Models 🎯
**Objective:** Build and evaluate various classification algorithms for predictive modeling.

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

#### Data Type Corrections
- Ensured proper data types for all columns
- Handled numerical and categorical variables appropriately

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

### Advanced Analysis
- Survival rates by multiple factors (class × gender × age)
- Family structure impact on survival
- Embarkation port analysis

---

## 📈 Task 3: Linear Regression Implementation

### 🏠 Housing Price Prediction Analysis
**Dataset:** Housing.csv containing property features and prices

### Key Implementation Steps

#### Data Preprocessing
- Converted categorical variables (yes/no) to binary encoding (1/0)
- Label encoding for furnishing status
- Feature correlation analysis

#### Simple Linear Regression
- **Model:** Price vs Area only
- **Equation:** Price = β₀ + β₁ × Area
- **Performance:** R² ~0.55-0.60

#### Multiple Linear Regression
- **Model:** Price vs 12 features including area, bedrooms, bathrooms, amenities
- **Performance:** R² ~0.65-0.70 (significant improvement)

#### Feature Engineering
- Created `area_per_bedroom` and `luxury_score` features
- Further improved model performance

### Key Findings

#### Most Influential Features (by coefficient magnitude):
- **Area:** Strongest positive predictor (+1,045 per sq ft)
- **Air Conditioning:** Significant value addition
- **Preferred Area:** Location premium pricing
- **Bathrooms:** Substantial value contribution
- **Parking:** Added property value

#### Model Performance Comparison:

| Model Type | R² Score | MAE | RMSE |
|------------|----------|-----|------|
| Simple Regression | 0.55-0.60 | Higher | Higher |
| Multiple Regression | 0.65-0.70 | Lower | Lower |
| With Engineered Features | 0.68-0.72 | Lowest | Lowest |

### Technical Implementation
**Evaluation Metrics Used:**
- R² Score (Coefficient of Determination)
- Mean Absolute Error (MAE)
- Root Mean Square Error (RMSE)
- Residual Analysis

**Visualizations Created:**
- Correlation heatmaps
- Actual vs Predicted scatter plots
- Residual plots for error analysis
- Feature coefficient comparisons

---

## 🎯 Task 4: Classification Models Implementation

### 🩺 Breast Cancer Classification Analysis
**Dataset:** Wisconsin Breast Cancer Diagnostic dataset with 30+ medical features

### Key Implementation Steps

#### Data Preprocessing & Feature Engineering
- **Missing Value Handling:** Comprehensive NaN detection and imputation strategies
- **Feature Selection:** SelectKBest with ANOVA F-value for top feature identification
- **Data Scaling:** StandardScaler for feature normalization
- **Class Balance Analysis:** Stratified sampling for training/test splits

#### Classification Algorithms Implemented

##### 1. Logistic Regression
- **Baseline Model:** High interpretability with coefficient analysis
- **Regularization:** L2 penalty to prevent overfitting
- **Performance Metrics:** Accuracy, Precision, Recall, F1-score, ROC-AUC

##### 2. Support Vector Machines (SVM)
- **Kernel Selection:** Linear and RBF kernel comparison
- **Hyperparameter Tuning:** GridSearchCV for optimal C and gamma parameters
- **Decision Boundary Analysis:** Margin maximization visualization

##### 3. Random Forest Classifier
- **Ensemble Method:** Bagging with multiple decision trees
- **Feature Importance:** Gini importance for medical feature ranking
- **Out-of-Bag Error:** Internal validation metric

##### 4. Gradient Boosting (XGBoost)
- **Advanced Ensemble:** Sequential tree building with gradient optimization
- **Early Stopping:** Prevention of overfitting during training
- **Cross-Validation:** Robust performance evaluation

### Model Evaluation Framework

#### Performance Metrics
- **Accuracy:** Overall classification correctness
- **Precision:** Malignant prediction reliability
- **Recall:** Sensitivity in detecting actual malignancies
- **F1-Score:** Harmonic mean of precision and recall
- **ROC-AUC:** Overall model discrimination ability

#### Validation Techniques
- **Stratified K-Fold Cross-Validation:** 5-fold CV with class balance preservation
- **Confusion Matrix Analysis:** Detailed error type examination
- **Learning Curves:** Bias-variance tradeoff assessment

### Key Findings & Medical Insights

#### Top Predictive Features Identified:
1. **Worst Area:** Strongest predictor of malignancy
2. **Mean Perimeter:** Significant morphological indicator
3. **Worst Concavity:** Critical shape characteristic
4. **Mean Concave Points:** Important texture feature
5. **Worst Radius:** Size-related malignancy indicator

#### Model Performance Comparison:

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|-------|----------|-----------|--------|----------|---------|
| Logistic Regression | 0.95-0.97 | 0.96-0.98 | 0.93-0.96 | 0.95-0.97 | 0.98-0.99 |
| SVM (RBF Kernel) | 0.96-0.98 | 0.97-0.99 | 0.94-0.97 | 0.96-0.98 | 0.99-0.995 |
| Random Forest | 0.95-0.97 | 0.96-0.98 | 0.93-0.96 | 0.95-0.97 | 0.98-0.99 |
| XGBoost | 0.97-0.99 | 0.98-0.99 | 0.95-0.98 | 0.97-0.98 | 0.99-0.997 |

### Advanced Analysis Techniques

#### Feature Importance Interpretation
- **Medical Relevance:** Correlation of top features with clinical indicators
- **Multicollinearity Analysis:** Handling correlated medical measurements
- **Dimensionality Reduction:** PCA for feature space visualization

#### Model Interpretability
- **SHAP Values:** Game-theoretic approach to feature contribution
- **Partial Dependence Plots:** Individual feature effect visualization
- **Decision Boundary Visualization:** 2D projection of classification regions

#### Clinical Application Insights
- **Early Detection:** Model's ability to identify malignancies with high precision
- **False Negative Reduction:** Recall optimization for medical safety
- **Feature Thresholds:** Clinical decision support based on key measurements

### Technical Implementation Details

#### Code Architecture
```python
# Modular pipeline structure
preprocessor = Pipeline([
    ('imputer', SimpleImputer(strategy='mean')),
    ('scaler', StandardScaler()),
    ('selector', SelectKBest(score_func=f_classif, k=15))
])

classifiers = {
    'logistic': LogisticRegression(),
    'svm': SVC(probability=True),
    'rf': RandomForestClassifier(),
    'xgb': XGBClassifier()
}
