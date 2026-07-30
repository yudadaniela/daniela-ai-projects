# Exploratory Data Analysis — Diabetes Progression

## Problem
Performed a full exploratory data analysis on a clinical diabetes 
dataset (442 patients) to identify which health indicators most 
strongly relate to disease progression, including comparisons across 
gender and age groups.

## Tools & Approach
- Python: Pandas for data manipulation and descriptive statistics
- Matplotlib & Seaborn for visualization
- Statistical techniques: central tendency (mean, median, mode), 
  dispersion (std dev, variance, IQR), skewness & kurtosis, 
  frequency distribution by category, correlation analysis
- Visualizations: histograms, bar/pie charts, boxplots, line plots 
  by group, correlation heatmap

## My Contribution
Individual project — full pipeline from data loading through 
statistical analysis and visualization.

## Key Findings
- **BMI is the strongest predictor of disease progression** in this 
  dataset (correlation of 0.59), followed by blood pressure (0.44) — 
  both more determinant than age (0.19)
- Blood pressure and BMI are also moderately correlated with each 
  other (0.40)
- Women in the dataset showed higher average blood pressure (98.2 vs 
  91.5) and higher disease progression (155.7 vs 149.0) than men
- Disease progression is the most dispersed variable by far (std dev 
  of 77.09), meaning patients vary widely in how the disease advances 
  — some barely progress, others progress severely
- ~22% of patients fall into the obesity category by BMI, and the 
  distribution is right-skewed (more high outliers than low ones)

## What I'd Do Differently
Apply formal hypothesis testing (e.g., a t-test) to confirm whether 
the gender differences in blood pressure and disease progression are 
statistically significant, rather than relying on descriptive averages 
alone.

## Course
Fundamentos de Inteligencia Artificial
