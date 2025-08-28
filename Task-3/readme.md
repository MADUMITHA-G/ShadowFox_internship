# Questions & answers 

## What is the prevalence of heart disease in this dataset?
  The heart_disease column mean is ~0.4037, so ~40.4% of the records indicate presence of heart disease and ~59.6% indicate absence. This shows a substantial positive class, not a tiny minority.

## Does age appear related to heart disease?
  Yes — the violin plot you made (Age vs heart_disease) shows older patients tend to appear more often in the heart_disease = 1 group. The dataset’s overall mean age is ~52.5 years and the distribution’s upper quartile (75%) is 64 years, which aligns with higher risk with increasing age.

## Is sex (male/female) associated with heart disease in this dataset?
  The dataset has ~55.6% males (sex mean ≈ 0.5556). Your countplot (Sex vs Heart Disease) shows more males overall and more males with heart disease. This suggests sex is a relevant demographic factor — but you should quantify via group means or a chi-square test before concluding causality.

## Which clinical features stand out as important or correlated with heart disease from the EDA?
  From the boxplots, heatmap and domain knowledge the features that stand out are: thalach (max heart rate), oldpeak (ST depression), chol (cholesterol), ca (number of major vessels), and age. smoking and diabetes show noticeable class differences in the countplots (smoking ~34.9% and diabetes ~19.4% in dataset). These are strong candidates for predictors in a model.

## Any obvious data quality issues or preprocessing needs before modeling?
  The dataset has no nulls and zero duplicate rows (good!). However, many features are categorical encoded as integers (cp, restecg, slope, thal, etc.) and should be handled appropriately (one-hot or ordinal depending on semantics). Also check and possibly scale numerical features (trestbps, chol, thalach, oldpeak, bmi) and inspect outliers (boxplots show some spread). Finally, verify thal/ca coding (there are values like 3,7 etc.) to ensure they map to real categories.
