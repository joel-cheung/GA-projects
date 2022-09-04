<img src="http://imgur.com/1ZcRyrc.png" style="float: left; margin: 20px; height: 55px">

# Project 4: West Nile Virus Prediction Project

# Information
This project is based on a kaggle challenge: https://www.kaggle.com/c/predict-west-nile-virus/

# Background
The West Nile virus (WNV) first appeared in the Americas in 1999, and has since become the **leading** mosquito-borne disease in the country ([source](https://www.nejm.org/doi/full/10.1056/NEJM200106143442401)). It is a virus transmitted to humans by mosquitoes that feed on infected birds. Around 20% of people who become infected with the virus develop symptoms ranging from fever, and headaches, to serious neurological illnesses that can result in death. The first WNV case was identified in Illinois in September 2001 when laboratory tests confirmed its presence in two crows found dead in the Chicago area. By the end of 2002, Illinois accounted for more human cases and deaths than any other state ([source](https://dph.illinois.gov/topics-services/diseases-and-conditions/west-nile-virus)). Since there is no vaccine or medication to prevent or treat WNV in people, the most effective way to prevent this virus is to reduce the number of mosquitoes and to take precautions to avoid mosquito bites ([source](https://www.cdc.gov/westnile/index.html#:~:text=There%20are%20no%20vaccines%20to,a%20fever%20and%20other%20symptoms.)). 

Following the outbreak of WNV in Chicago, the City of Chicago and Chicago Department of Public Health (CDPH) put in place a comprehensive surveillance and control program to trap and test mosquitos for WNV. This program is still in place today.

# Problem Statement
In light of the potential outbreak of WNV in Chicago, the CDPH has asked its data scientist team to develop a predictive model based on past data on weather conditions and virus detection locations.

Given the use of public funds to finance the spraying of pesticide in order to  reduce the number of WNV cases, coupled with the pontentially high cost of spraying pesticide over large areas, it is imperative for this project to bring focus to where and when pesticides should be sprayed that would effectively combat the WNV problem.

A model that accurately predicts the outbreak of the virus using information about the locations of mosquito traps and weather information ensures that the targeted spraying will be informed and well-justified.

# Data Dictionary
 
The Kaggle datasets provided are as follows:
 
|Dataset| Description|
|---|---|
|spray| Contains details of past sprays from 2011 and 2013|
|weather| Contains meteorological data from 2007-2014|
|train| Contains data relating to mosquito traps, number of mosquitos and presence of WNV from 2007-2013|
|test| Contains data relating to mosquito traps and number of mosquitos from 2008-2014|

# Files
There are 2 notebooks used for this project:

1.  Notebook 1: Exploratory Data Analysis (EDA) and Data Cleaning
2.  Notebook 2: Modelling, Evaluation, and Cost-Benefit Analysis

# Model Evaluation
The best model is the XGBoost model with a cross validation ROC AUC of 0.8805.

### Summary
| Method | Cross Validation ROC AUC | Ranking|
|---|---|---|
| Logistic Regression | 85.74% | 7th |
| Random Forest | 87.81%  | 2nd/3rd |
| AdaBoost | 87.81%  | 2nd/3rd | 
| Gradient Boost | 87.37% | 5th |
| XGBoost | 88.05% | 1st |
| Support Vector Machine | 87.67% | 4th |
| k-Nearest Neighbours | 85.50% | 6th |

# Conclusion and Recommendations

### Recommended Model
The XGBoost model will be used for future predictions, given its highest cross validation ROC AUC score.

###  Targeted Mosquito Abatement Recommendations
-   Increase larviciding initiation at the location which has a high risk of West Nile Virus emergence (WnV case > 5). Current allocated resource is only for 190 acres which translates to 1 neighborhood. An additional 800 acres will cost approximately USD77,920.
-   Lowering the threshold of adulticiding for the month of June and July, which is the month with high population growth, it will speed up on handling adult mosquitoes findings and ultimately will suppress the population of mosquitoes. An additional 100 miles costs USD12,060 is approximately needed.
-   Conducting awareness roadshow within the neighborhood to make the residents more aware on the virus information and they can help in reducing potential breeding location. Estimated Cost: USD 15,000


### Cost-Benefit Analysis
Since the potentially benefits derived from alleviating this economic burden caused by the West Nile Virus of up to USD 3,003,756 far outweighs the costs of our Mosquito Abatement Program's efforts for 2023 of USD 520,698 by ~5.8 times ( = 3,003,756 / 520,698 ), we strongly recommend continuing with our Mosquito Abatement Program's efforts for 2023 and beyond.

### Estimated Cost of Recommended Mosquito Abatement Plan
USD 625,000 annually. This value includes the increased larviciding, additional areas sprayed, and conducting awareness roadshows.
