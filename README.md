# Google-Advanced-Data-Analytics-Capstone-Project
This is my capstone project for Google's Advanced Data Analytics Course, utilizing a Linear Regression model and a Tree-based Machine Learning Model.

- The Executive Summary document is a one-page deliverable meant to be proposed to client stakeholders

- The Colab Code Notebook contains all the model and data visualization, and walks you through the project

# Table of Contents

1. [Introduction](#1-introduction)
2. [Scenario](#2-scenario)
3. [PACE stages](#3-pace-stages)
4. [Data Analysis](#4-data-analysis)
5. [Result](#5-result)

# 1. Introduction
This is my capstone project for completing [Google Advanced Data Analytics Professional Certificate](https://www.coursera.org/professional-certificates/google-advanced-data-analytics). In this project scope, I'm a data professional working for a fictional company, Salifort Motors. I've been tasked with analyzing survey data that employees provided to answer the question: what’s likely to make the employee leave the company?

# 2. Scenario
Salifort Motors is facing a high rate of employee turnovers. The senior leadership team asks you (the data professional) to analyze the survey data and come up with data-driven ideas for how to increase employee retention. 

To help with this, they suggest you design a model that predicts whether an employee will leave the company based on their job title, department, number of projects, average monthly hours, and any other relevant data points. A good model will help the company increase retention and job satisfaction for current employees, and save money and time training new employees. 

The dataset that you'll be using contains 15,000 rows and 10 columns for the variables listed below, refer to its source on [Kaggle](https://www.kaggle.com/datasets/mfaisalqureshi/hr-analytics-and-job-prediction?select=HR_comma_sep.csv).

Variable  |Description |
-----|-----|
satisfaction_level|Employee-reported job satisfaction level [0&ndash;1]|
last_evaluation|Score of employee's last performance review [0&ndash;1]|
number_project|Number of projects employee contributes to|
average_monthly_hours|Average number of hours employee worked per month|
time_spend_company|How long the employee has been with the company (years)
Work_accident|Whether or not the employee experienced an accident while at work
left|Whether or not the employee left the company
promotion_last_5years|Whether or not the employee was promoted in the last 5 years
Department|The employee's department
salary|The employee's salary (U.S. dollars)

# 3. PACE stages
![pace stage](Pace-Stages.png)
Detailed process in the Jupyter Notebook [Here].

# 4. Data Analysis

**Tools used:**
- Data Manipulation
  - NumPy
  - Pandas
- Data Visualization
  - Matplotlib
  - Seaborn
- Data Modeling
  - XGBoost (Extreme Gradient Boosting)
  - Scikit-learn (sklearn)
- Metrics and Helpful Functions
  - More scikit-learn
- Saving Models
  - Pickle


# 5. Result
[Executive Summary](https://github.com/Jeremy-Kwok/Google-Advanced-Data-Analytics-Capstone-Project/blob/main/Executive%20Summary.pdf)

### Summary of model results

**Logistic Regression**

The logistic regression model achieved:
- Precision: 79%
- Recall: 82%
- f1-score: 80% (all weighted average)
- Accuracy of 82%

**Tree-based Machine Learning Model**

The decision tree model achieved on the test set:
- AUC: 93.8%
- Precision: 87.0%
- Recall: 90.4%
- f1-score: 88.7%
- Accuracy: 96.2%

**Feature Importance**

From all of the models, we see that the most important features are (from most important to least important) `last_evaluation`, `number_project`, `tenure`, `overworked`. These variables are most helpful in predicting the outcome variable `left` (whether or not an employee left Salifort Motors)

### Conclusion and Recommendations
**Conclusion:** All models suggest that employees are being overworked.

**Recommendations:** To retain employees, the following recommendations could be presented to the stakeholders:

- Cap the number of projects that employees can work on.
- Consider promoting employees who have been with the company for atleast four years, or conduct further investigation about why four-year tenured employees are so dissatisfied.
- Either reward employees for working longer hours, or don't require them to do so.
- If employees aren't familiar with the company's overtime pay policies, inform them about this. If the expectations around workload and time off aren't explicit, make them clear.
- Hold company-wide and within-team discussions to understand and address the company work culture, across the board and in specific contexts.
- High evaluation scores should not be reserved for employees who work 200+ hours per month. Consider a proportionate scale for rewarding employees who contribute more/put in more effort.
