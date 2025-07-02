# 🧠 Stroke Dataset Analysis

## 📊 Project Overview

This project presents a comprehensive statistical, machine learning, and clustering analysis on a stroke prediction dataset. The analysis follows a structured pipeline starting from data understanding to deploying various predictive models to identify stroke risks based on features such as age, BMI, glucose levels, and other health indicators.

## 📂 Table of Contents

- [1. Descriptive Analytics](#1-descriptive-analytics)
- [2. Data Preparation](#2-data-preparation)
- [3. Classification Models](#3-classification-models)
- [4. Regression Models](#4-regression-models)
- [5. Clustering Analysis](#5-clustering-analysis)
- [6. Key Findings](#6-key-findings)
- [7. Technologies Used](#7-technologies-used)
---

## 1. Descriptive Analytics

- Computation of basic statistics for each feature (`age`, `gender`, `bmi`, `avg_glucose_level`, etc.)
- Visualizations:
  - Boxplots
  - Violinplots
  - Scatterplots
  - Grouped bar charts
- Insights on stroke correlation with age, hypertension, heart disease, etc.

---

## 2. Data Preparation

- **Removed:** Non-informative ID column
- **Encoding:** Label Encoding for categorical attributes
- **Outlier Handling:** IQR clipping for `bmi` and `avg_glucose_level`
- **Imputation:** Missing BMI values filled using age-based group means
- **Normalization:** MinMaxScaler for regression, classification, and clustering
- **Class Imbalance Handling:** SMOTE for the minority class in stroke prediction

---

## 3. Classification Models

- **Algorithms Applied:**
  - Random Forest
  - Bagging
  - K-Nearest Neighbors (KNN)
  - AdaBoost (Extra)
- **Evaluation:**
  - Accuracy
  - F1-score (per class)
  - Confusion Matrix
  - ROC-AUC

> ✅ Best Classifier: **Bagging** with ~96.87% accuracy

---

## 4. Regression Models

- **Target:** BMI prediction
- **Models:**
  - Gradient Boosting Regressor
  - Random Forest Regressor
- **Metrics:**
  - MAE, MSE, RMSE
  - R² and Adjusted R²

> 📌 Performance: Both models performed similarly; Gradient Boosting had slightly better R².

---

## 5. Clustering Analysis

- **Techniques:**
  - KMeans
  - KMedoids (Extra)
- **Evaluation:**
  - Elbow Method
  - Silhouette Score
- **Insights:**
  - Two optimal clusters identified: younger vs. older with different health risk profiles
  - Denormalized and decoded clusters for interpretation

---

## 6. Key Findings

- Stroke risk is significantly higher in older individuals, especially with high BMI and glucose levels
- Random Forest and Bagging classifiers showed high F1-scores across both classes
- Regression models explained ~31% variance in BMI
- Clustering highlighted distinct demographic-health segments

---

## 7. Technologies Used

- Python 3.x
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
- imbalanced-learn (SMOTE)
- Yellowbrick (for clustering visuals)

