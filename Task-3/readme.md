Task 3 - Heart Disease Dataset Analysis
# Heart Disease Dataset Analysis Report
##  Problem Statement

Heart disease is a leading cause of death worldwide. Identifying risk factors and patterns early can help in diagnosis and prevention.
This project explores a clinical dataset of 3,069 patient records with 17 features (demographic, lifestyle, and medical parameters) to understand the factors associated with heart disease.

## Overview

Dataset size: 3,069 rows × 17 columns

Target variable: heart_disease (0 = No, 1 = Yes)

Positive cases: ~40.4%

Features include: age, sex, chest pain type (cp), blood pressure (trestbps), cholesterol (chol), fasting blood sugar (fbs), maximum heart rate (thalach), ST depression (oldpeak), smoking, diabetes, BMI, etc.

Key insights from EDA:

Age: Higher risk in older patients.

Sex: Males more frequently affected.

Cholesterol, trestbps, oldpeak, thalach: Strongly associated with heart disease.

Lifestyle factors: Smoking and diabetes show higher prevalence in the positive class.

Correlation Heatmap: Identifies clinical predictors most correlated with heart disease.

## Tools & Frameworks Used

Python: Data analysis & preprocessing

pandas, numpy: Data handling

matplotlib, seaborn: Data visualization

## Visualizations

Heart disease distribution

Age vs heart disease (violin plot)

Sex vs heart disease (countplot)

Chest pain type vs heart disease (countplot)

Resting BP, Cholesterol, BMI distributions by target (boxplots)

Maximum heart rate & ST depression vs target (boxplots)

Smoking, diabetes, fasting blood sugar vs heart disease (countplots)

Correlation heatmap

## Next Steps

Data preprocessing: One-hot encoding, scaling, outlier handling

Model building: Logistic Regression, Random Forest, XGBoost

Model evaluation: Accuracy, Precision, Recall, F1, ROC-AUC

Explainability: SHAP feature importance plots

Deployment: Save model (joblib/pickle), simple Flask API or Streamlit app

## Conclusion

Dataset is clean (no missing values, no duplicates).

Key predictors observed: thalach, oldpeak, age, chol, ca.

Both demographic (age, sex) and lifestyle factors (smoking, diabetes) influence heart disease risk.

With proper preprocessing and classification models, predictive performance can be optimized.

# Questions & answers 

### What is the prevalence of heart disease in this dataset?
  The heart_disease column mean is ~0.4037, so ~40.4% of the records indicate presence of heart disease and ~59.6% indicate absence. This shows a substantial positive class, not a tiny minority.

### Does age appear related to heart disease?
  Yes — the violin plot you made (Age vs heart_disease) shows older patients tend to appear more often in the heart_disease = 1 group. The dataset’s overall mean age is ~52.5 years and the distribution’s upper quartile (75%) is 64 years, which aligns with higher risk with increasing age.

### Is sex (male/female) associated with heart disease in this dataset?
  The dataset has ~55.6% males (sex mean ≈ 0.5556). Your countplot (Sex vs Heart Disease) shows more males overall and more males with heart disease. This suggests sex is a relevant demographic factor — but you should quantify via group means or a chi-square test before concluding causality.

### Which clinical features stand out as important or correlated with heart disease from the EDA?
  From the boxplots, heatmap and domain knowledge the features that stand out are: thalach (max heart rate), oldpeak (ST depression), chol (cholesterol), ca (number of major vessels), and age. smoking and diabetes show noticeable class differences in the countplots (smoking ~34.9% and diabetes ~19.4% in dataset). These are strong candidates for predictors in a model.

### Any obvious data quality issues or preprocessing needs before modeling?
  The dataset has no nulls and zero duplicate rows (good!). However, many features are categorical encoded as integers (cp, restecg, slope, thal, etc.) and should be handled appropriately (one-hot or ordinal depending on semantics). Also check and possibly scale numerical features (trestbps, chol, thalach, oldpeak, bmi) and inspect outliers (boxplots show some spread). Finally, verify thal/ca coding (there are values like 3,7 etc.) to ensure they map to real categories.
