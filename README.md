# Health Care Insurance Fraud Detection
Aljawhara Alsultan
# Abstract  

The spark came from interview on last April for HRH MBS, mentioned that one of goals in Health Sector Transformation giving insurance policy for each employees in the Kingdome. This will be a gate for many frauds to occur in the health insurance domain. From that point, It is necessary to maintain and monitor the patient’s  insurance without any ambiguity. 

There are a list of fraud cases that provided by National Health Care Anti-Fraud Association , ”Guidelines to HealthCare Fraud: Factsheet,” 2002. which includes: 

-  False Patient Diagnoses.
-  Treatment and Medical Histories.
- Theft of Patients’ Finite Health Insurance Benefits. 
- Claiming insurance from multiple insurance companies.

In this project,  I will provide a solution for Theft of Patients’ Finite Health Insurance Benefits. which will be adde value for Council of Health Insurance in Nphies project. 

# Data
The dataset contains 59,400 waterpoints with 40 features for each, 32 of which are categorical. A few feature highlights include measurements of water quantity and quality, pump types, and latitude/longitude coordinates. Nearly a third of the individual features could be grouped into more general categories, and an in-depth analysis of 20 of them was undertaken to inform baseline models and feature engineering.

# Algorithms
Feature Engineering

Mapping latitude and longitude to 3-dimensional coordinates so nearby continuous values would also be close in reality
Converting categorical features to binary dummy variables
Combining particular dummies and ranges of numeric features to highlight strong signals and illogical values for waterpoint status identified during EDA
Selecting subsets of the total unique values for categorical features that were converted to dummies, according to the number of samples they were associated with and their contribution to certain statuses
Models

Logistic regression, k-nearest neighbors, and random forest classifiers were used before settling on random forest as the model with strongest cross-validation performance. Random forest feature importance ranking was used directly to guide the choice and order of variables to be included as the model underwent refinement.

Model Evaluation and Selection

The entire training dataset of 59,400 records was split into 80/20 train vs. holdout, and all scores reported below were calculated with 5-fold cross validation on the training portion only. Predictions on the 20% holdout were limited to the very end, so this split was only used and scores seen just once.

The official metric for DrivenData was classification rate (accuracy); however, class weights were included to improve performance against F1 score and provide a more useful real-world application where classification of the minority class (functional needs repair) would be essential.

Final random forest 5-fold CV scores: 99 features (7 numeric) with class weights

Accuracy 0.797
F1 0.791 micro, 0.679 macro
precision 0.792 micro, 0.722 macro
recall 0.797 micro, 0.658 macro
Holdout

Accuracy: 0.802
F1: 0.795 micro, 0.685 macro
Precision: 0.796 micro, 0.725 macro
Recall: 0.802 micro, 0.664 macro

# Tools 
- Numpy and Pandas for data manipulation
- Scikit-learn for modeling
- Matplotlib and Seaborn for plotting

# Communication
In addition to the slides and visuals presented, LINKED IN ACCOUNT.


This repo is one of the T5 Bootcamp requirements.
The health care industry is one of the important service providers that improves people lives. 


Question/need:

How many Insurance company do we have?
Is theier any Fraud Detection?

What is the framing question of your analysis, or the purpose of the model/system you plan to build?
Who benefits from exploring this question or building this model/system?
Data Description:
What dataset(s) do you plan to use, and how will you obtain the data?
What is an individual sample/unit of analysis in this project? What characteristics/features do you expect to work with?
If modeling, what will you predict as your target?
Tools:
How do you intend to meet the tools requirement of the project?
Are you planning in advance to need or use additional tools beyond those required?
