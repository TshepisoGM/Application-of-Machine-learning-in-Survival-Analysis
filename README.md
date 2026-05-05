
#Survival Analysis & Machine Learning in Lung Cancer
 Overview

This project applies advanced survival analysis and machine learning techniques to predict outcomes in patients with advanced lung cancer. Using clinical and demographic variables, multiple models are developed and compared to evaluate predictive performance and risk stratification.

 Objectives
Model time-to-event (survival) outcomes
Compare traditional statistical models with machine learning approaches
Evaluate model performance using discrimination, calibration, and accuracy metrics
Identify key predictors of mortality
 Tools & Technologies
R Programming
Packages: survival, glmnet, xgboost, randomForestSRC, caret, timeROC, pec, riskRegression
Statistical & ML Methods: Cox models, penalized regression, Random Survival Forests, Gradient Boosting
 Dataset

The dataset includes patient-level survival data with:

Outcome: Survival time (days) and event status (alive/deceased)
Demographics: Age, sex
Clinical variables: ECOG score, Karnofsky scores (physician & patient)
Other factors: Caloric intake and weight loss
 Methodology
1. Data Preparation
Data cleaning and transformation
Normality assessment (Shapiro-Wilk, QQ plots)
Feature selection and encoding
2. Model Development

Nested cross-validation (5 outer, 3 inner folds) used for robust evaluation:

Lasso Cox
Ridge Cox
Elastic Net Cox
Random Survival Forest (RSF)
XGBoost (Cox objective)
3. Model Evaluation

Performance assessed using:

C-index (discrimination)
Time-dependent AUC
Brier Score (prediction error)
Calibration plots (agreement between predicted and observed risk)

Bootstrap resampling was applied to estimate confidence intervals
