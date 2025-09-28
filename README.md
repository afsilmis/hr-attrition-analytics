# Predicting Employee Attrition to Improve Retention

This repository contains the code and resources for a data-driven project aimed at predicting employee attrition. The primary goal is to develop a machine learning model that can proactively identify employees at risk of leaving, enabling targeted intervention strategies to improve retention. This project was completed by Az-Zukhrufu Fi Silmi Suwondo for Rakamin Academy.

## Problem Statement

The organization is facing high employee turnover, which results in significant recruitment costs, loss of productivity, and a negative impact on team morale. The existing retention efforts are primarily reactive due to a lack of data-driven insights into the root causes of attrition.

## Project Objectives

The main goal is to decrease the overall employee turnover rate by 15% within the next 18 months. This will be achieved by implementing a predictive retention framework with the following objectives:

  * **Analyze Key Variables**: Identify the top predictors of employee attrition.
  * **Build a Predictive Model**: Develop a machine learning model to assign attrition risk scores to employees.
  * **Generate Actionable Insights**: Translate model insights into HR recommendations to enhance company culture, employee growth, and job satisfaction.

## Success Metrics

The success of this project will be measured by:

  * A **15% reduction** in the attrition rate compared to the previous period.
  * A **15% increase** in the Employee Engagement Score from the previous period.

## Dataset Overview

  * **Total Employees**: 287 
  * **Resigned Employees**: 89
  * **Hiring Period**: January 2006 - July 2018 
  * **Resignation Period**: May 2013 - September 2020 

The dataset includes the following features:

  * **Demographics**: Gender, Marital Status, Region.
  * **Employment Info**: Job Role, Career Track, Hiring Platform.
  * **Scores**: Engagement Score, Satisfaction Score, Project Count.
  * **Behavioral Data**: Absences, Late Arrivals, Resignation Reason.

## Methodology

### Data Preprocessing

1.  **Data Splitting**: The data was separated into features (X) and the target variable (y), followed by a stratified train-test split (80/20).
2.  **Handling Missing Values & Outliers**: Numerical columns with missing values were filled with the median, while categorical columns were filled with the mode. Outliers were also imputed with the median.
3.  **Feature Scaling & Encoding**: Numerical features were scaled using `RobustScaler`. Ordinal and frequency encoding were applied to categorical variables.

### Feature Engineering

To enhance the model's predictive power, several new features were created, including:

  * Time-Based Features
  * Performance & Engagement Metrics 
  * Attendance Patterns 
  * Career Signals 
  * Advanced Demographic Features 
  * Clustering & Risk Scores 

### Model Selection and Optimization

Different classification models were evaluated, and the **Support Vector Classifier (SVC)** was selected as the best-performing model due to its high F1-Score of 0.723.

The SVC model was further optimized through:

  * **Hyperparameter Tuning**: Using Optuna (30 trials, 5-fold CV), the best parameters were identified as $C=3.069$, a `linear` kernel, and `auto` for gamma.
  * **Threshold Tuning**: A threshold of **0.49** was chosen to balance the trade-off between precision, recall, and F1-score.

## Model Performance

The final model achieved the following evaluation metrics:

  * **F1-Score**: 0.72 
  * **Precision**: 0.58 
  * **Recall**: 0.97 
  * **AUC**: 0.638

The model demonstrates a strong ability to identify at-risk employees, with a high recall of 97%.

## Key Findings & Feature Importance

The analysis of feature importance revealed that turnover is influenced by a combination of factors:

  * **Performance & Engagement**: The highest attrition risk is associated with senior, low-performing employees. The gap between engagement and satisfaction is also a strong predictor.
  * **Talent Mismatch**: Employees who are overqualified for their roles show a higher tendency to leave.
  * **Hiring & Onboarding**: The recruitment platform and the timing of hiring (quarter) have a significant impact on retention.

A deeper analysis of resignation reasons showed that the top five are:

1.  Working Hours (Jam Kerja) 
2.  Career Change (Ganti Karir)
3.  Lack of Career Clarity (Kejelasan Karir)
4.  Inability to Work Remotely (Tidak Bisa Remote)
5.  Toxic Culture (Toxic Culture) 

## Strategic Recommendations

Based on the model's insights, the following strategic recommendations are proposed:

  * **Proactive Intervention**: Utilize the predictive model to identify and support at-risk employees.
  * **Revamp Flexibility & Working Hours**:
      * Implement hybrid/remote work options, especially for technical roles like Front-End Engineers who cited this as a major reason for leaving.
      * Conduct a workload audit to address issues of long working hours.
  * **Strengthen Work Culture & Team Environment**:
      * Address the "toxic culture" reported by Data Analysts by launching cultural interventions, such as anonymous surveys and focus group discussions.
      * Create safe and anonymous feedback channels for all employees.
  * **Create Career Clarity & Growth Opportunities**:
      * Develop and clearly communicate career paths for each role.
      * Launch mentorship and skill development programs to support employee growth.

## Contact

For any questions or collaboration, please feel free to reach out:

  * **Email**: afsilmis@gmail.com 
  * **LinkedIn**: https://www.linkedin.com/in/az-zukhrufu-fi-silmi-suwondo
  * **Source Code**: https://github.com/afsilmis/hr-attrition-analytics
