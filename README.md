# 📘 Machine Learning Project Tasks & Outcomes

## 🛠️ Task 1: Data Cleaning & Preprocessing
**Dataset:** Titanic  

### 🔑 Key Preprocessing Steps
- **Handling Missing Values**  
  - Age → median imputation  
  - Embarked → mode (most frequent port)  
  - Cabin → dropped (>77% missing)  
  - Fare → single missing value handled  

- **Converting Categorical Features**  
  - Sex → label encoded (0/1)  
  - Embarked → one-hot encoded  
  - Title → extracted from passenger names  
  - Family Size → derived from SibSp + Parch  

- **Feature Engineering**  
  - `Title` feature  
  - `FamilySize` feature  
  - `IsAlone` flag  
  - Binned Age & Fare  

---

## 📊 Task 2: Exploratory Data Analysis (EDA)
**Dataset:** Titanic  

### 🔎 Analysis Performed
- Summary statistics (numerical + categorical)  
- Distribution analysis (histograms, boxplots)  
- Survival analysis across groups  
- Correlation heatmaps  

### 📈 Key Insights
- Class Impact: 1st class survival ~ **63%** vs 3rd class **24%**  
- Gender Bias: Females **74%** vs Males **19%**  
- Age Factor: Children (<10) survived more  
- Fare Correlation: Higher fares → better survival  
- Family Size: 2–4 members = best survival rate  

---

## 📈 Task 3: Linear Regression
**Dataset:** Housing Prices  

### 🏠 Model Performance
| Model Type              | R² Score | MAE   | RMSE  |
|--------------------------|----------|-------|-------|
| Simple Regression        | 0.55–0.60 | High  | High  |
| Multiple Regression      | 0.65–0.70 | Low   | Low   |
| With Engineered Features | 0.68–0.72 | Lowest| Lowest|

### 🔑 Key Features
- Area (+1,045 per sq ft)  
- Air Conditioning  
- Preferred Area (location premium)  
- Bathrooms  
- Parking  

---

## 🎯 Task 4: Classification Models
**Dataset:** Breast Cancer  

### 📊 Model Comparison
| Model                | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|-----------------------|----------|-----------|--------|----------|---------|
| Logistic Regression   | 0.95–0.97 | 0.96–0.98 | 0.93–0.96 | 0.95–0.97 | 0.98–0.99 |
| SVM (RBF Kernel)      | 0.96–0.98 | 0.97–0.99 | 0.94–0.97 | 0.96–0.98 | 0.99–0.995 |
| Random Forest         | 0.95–0.97 | 0.96–0.98 | 0.93–0.96 | 0.95–0.97 | 0.98–0.99 |
| XGBoost               | 0.97–0.99 | 0.98–0.99 | 0.95–0.98 | 0.97–0.98 | 0.99–0.997 |

---

## 🌳 Task 5: Decision Trees & Random Forests
**Dataset:** Heart Disease  

### 📋 Features
`age, sex, cp, trestbps, chol, fbs, restecg, thalach, exang, oldpeak, slope, ca, thal, target`

### 📊 Model Performance
| Model                | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|-----------------------|----------|-----------|--------|----------|---------|
| Basic Decision Tree   | 0.75–0.80 | 0.76–0.82 | 0.74–0.79 | 0.75–0.80 | 0.82–0.85 |
| Optimized Decision Tree | 0.80–0.85 | 0.81–0.86 | 0.79–0.84 | 0.80–0.85 | 0.87–0.90 |
| Random Forest         | 0.85–0.90 | 0.86–0.91 | 0.84–0.89 | 0.85–0.90 | 0.92–0.95 |

### 🔑 Key Features
- Chest Pain Type (cp)  
- Maximum Heart Rate (thalach)  
- Oldpeak (ST depression)  
- CA (major vessels)  
- Thalassemia (thal)  

---

## 🔍 Task 6: Clustering Algorithms
**Analysis:** Customer Segmentation  

### ⚙️ Algorithms
- K-Means (centroid-based)  
- Hierarchical (dendrograms)  
- DBSCAN (density-based, noise handling)  

### 📊 Techniques
- Elbow Method (WCSS)  
- Silhouette Score  
- PCA visualization  

### 📌 Applications
- Customer segmentation  
- Fraud detection  
- Image segmentation  
- Document clustering  

---

## ⚡ Task 7: Support Vector Machines (SVM)
**Dataset:** Breast Cancer  

### 🔧 Key Implementation
- Linear SVM (margin maximization)  
- RBF Kernel for non-linear separation  
- Polynomial Kernel alternative  
- Hyperparameter tuning (`C`, `gamma`)  
- Cross-validation & GridSearch  
- Decision boundary visualization  

### 📊 Model Performance
| Model        | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|--------------|----------|-----------|--------|----------|---------|
| Linear SVM   | 0.95–0.97 | 0.96–0.98 | 0.93–0.96 | 0.95–0.97 | 0.98–0.99 |
| RBF SVM      | 0.96–0.98 | 0.97–0.99 | 0.94–0.97 | 0.96–0.98 | 0.99–0.995 |
| Tuned RBF SVM| 0.97–0.99 | 0.98–0.99 | 0.96–0.98 | 0.97–0.98 | 0.99–0.997 |

---

## 🎯 Overall Learning Outcomes

### 🔧 Technical Skills
- Data preprocessing & feature engineering  
- Regression, classification, clustering, SVMs  
- Hyperparameter tuning & evaluation  
- Data visualization & interpretation  

### 📊 Analytical Skills
- Pattern recognition  
- Feature importance analysis  
- Model selection & comparison  
- Statistical reasoning & hypothesis testing  

### 🛠️ Practical Implementation
- End-to-end ML pipelines  
- Real-world problem solving  
- Code optimization & reproducibility  
- Result interpretation & communication  
