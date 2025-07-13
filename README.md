# Heart Disease Prediction Project

## Overview

This project aims to predict the presence of cardiovascular disease in patients using clinical and lifestyle data. The workflow covers data cleaning, feature engineering, model building, and evaluation to ensure reliable and interpretable results.

---

## 1. Dataset Description

The dataset contains patient records with features grouped as:
- **Objective:** Factual information (e.g., age, height, weight, gender)
- **Examination:** Results from medical tests (e.g., blood pressure, cholesterol, glucose)
- **Subjective:** Patient-reported lifestyle factors (e.g., smoking, alcohol, physical activity)

The target variable, `cardio`, indicates the presence (1) or absence (0) of cardiovascular disease.

---

## 2. Data Preparation

### a. Data Loading & Cleaning
- Loaded the dataset from a CSV file.
- Split a combined column into individual features.
- Converted data types for consistency (e.g., integers, floats).
- Transformed age from days to years for better interpretability.
- Removed duplicate records and filtered out unrealistic blood pressure values based on medical guidelines.

### b. Exploratory Data Analysis (EDA)
- Used descriptive statistics and `.info()` to understand data types and distributions.
- Visualized distributions and outliers using histograms and boxplots.

---

## 3. Feature Engineering

- Created new continuous features for cholesterol (`chol`) and glucose (`glucose`) by mapping categorical levels to realistic value ranges.
- Encoded gender as a binary variable for modeling.

---

## 4. Preprocessing

- Selected relevant features for modeling.
- Standardized features using `StandardScaler` to ensure equal contribution to the model.
- Combined scaled features into a new DataFrame and included the target variable.

---

## 5. Model Development

### a. Data Splitting
- Split the data into training and testing sets to evaluate model performance on unseen data.

### b. Baseline Model
- Built a logistic regression model as a baseline to set a performance benchmark.

### c. Feature Selection
- Used `SelectKBest` to identify the most important features for prediction.
- Visualized feature importance scores.

### d. Model Building
- Trained a Random Forest classifier using the selected features for improved accuracy and robustness.

---

## 6. Model Evaluation

- Evaluated model performance using:
  - **Classification report:** Precision, recall, F1-score, and accuracy.
  - **Confusion matrix:** Visualized true/false positives and negatives.
  - **ROC curve:** Assessed the model’s ability to distinguish between classes.

---

## 7. Results & Conclusion

- The workflow ensures clean, high-quality data and meaningful features.
- The Random Forest model, after feature selection and tuning, provides reliable predictions for heart disease risk.
- Evaluation metrics and visualizations confirm the model’s effectiveness and interpretability.

---

## 8. Key Takeaways

- **Data cleaning and feature engineering** are crucial for building accurate models.
- **Feature selection** helps focus on the most informative variables.
- **Model evaluation** using multiple metrics ensures robust and trustworthy results.

---

This project demonstrates a complete machine learning pipeline for medical risk prediction, from raw data to actionable insights.
