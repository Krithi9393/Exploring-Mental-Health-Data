# Exploring-Mental-Health-Data

### Goal is to use data from a mental health survey to explore factors that may cause individuals to experience depression.

This repository focuses on analyzing and predicting mental health outcomes using machine learning techniques.  

## Overview  
- **Objective**: Predict mental health indicators using features like age, dietary habits, job satisfaction, and stress levels.  
- **Accuracy Achieved**: **93.723%** using a **stacking classifier** (Ranked 1878 on the leaderboard).
- **Highest Accuracy in Competition**: **94.128%**.  

## Dataset  
The dataset explores various factors influencing mental health, including:  
- **Age** (log-transformed for normalization)  
- **Dietary Habits** (categorized as Healthy, Moderate, Unhealthy)  
- **Stress Levels** (engineered from multiple features like Work Pressure, Financial Stress)  
- **Job/Study Satisfaction**  

## Methodology  
### Feature Engineering  
1. **Log Transformation**: Applied to `Age` to handle skewness.  
2. **Derived Features**:  
   - `Stress Point`: Combined work-study pressure and financial stress.  
   - `Age-Diet Combination`: Engineered feature combining age group and dietary habits.  

### Model Architecture  
- **Stacking Classifier** with the following base models:  
  - **XGBoost**  
  - **Random Forest**  
  - **AdaBoost**  
- **Meta-Model**: XGBoost for final predictions.  

### Preprocessing  
- **Scaling**: Used **MinMaxScaler** for feature scaling.  
- **Categorical Encoding**: One-hot and mapping for features like dietary habits and age group.  

## Results  
- **Final Accuracy**: **93.723%**  
- **Error Analysis**: Misclassification primarily influenced by stress and job satisfaction levels.  

