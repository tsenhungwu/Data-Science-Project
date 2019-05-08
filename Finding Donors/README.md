
<p align="middle">
  <img width="450" height="380" src="https://github.com/tsenhungwu/Data-Science-Project/blob/master/Finding%20Donors/Images/fundonor.png" />
  
# Introduction
In this project, I used several supervised algorithms to accurately model individuals' income using data collected from the 1994 U.S. Census. I then chose the best candidate algorithm from preliminary results and further optimize this algorithm to best model the data. 

This sort of task can arise in a non-profit setting, where organizations survive on donations. Understanding an individual's income can help a non-profit better understand how large of a donation to request, or whether or not they should reach out to begin with.


# Objectives
Throughout this project, I have achieved the following tasks:

- Explored Data through visualizations.
- Data transformation on features having skew distribution.
- Constructed a model that accurately predicts whether an individual makes more than $50,000.
- Optimized model by Bayesian Optimization.
- Feature importance report


# Technology
<p align="middle">
  <img height="210" width="510" src="https://github.com/tsenhungwu/Data-Engineer-Project/blob/master/Isongs/Images/Python.png" />
</p>


# Raw Data Exploration

Below, I took the first record from census.csv as an illustration:

<img src="https://github.com/tsenhungwu/Data-Science-Project/blob/master/Finding%20Donors/Images/raw_data.png"/>  

Feature Exploration:
  - age: **continuous.**
  - workclass: **categorical with 7 levels.** Private, Self-emp-not-inc, Self-emp-inc, Federal-gov, Local-gov, State-gov, Without-pay.
  - education: **categorical with 16 levels.** Bachelors, Some-college, 11th, HS-grad, Prof-school, Assoc-acdm, Assoc-voc, 9th, 7th-8th, 12th, Masters, 1st-4th, 10th, Doctorate, 5th-6th, Preschool.
  - education-num: continuous.
  - marital-status: **categorical with 7 levels.** Married-civ-spouse, Divorced, Never-married, Separated, Widowed, Married-spouse-absent, Married-AF-spouse.
  - occupation: **categorical with 14 levels.** Tech-support, Craft-repair, Other-service, Sales, Exec-managerial, Prof-specialty, Handlers-cleaners, Machine-op-inspct, Adm-clerical, Farming-fishing, Transport-moving, Priv-house-serv, Protective-serv, Armed-Forces.
  - relationship: **categorical with 6 levels.** Wife, Own-child, Husband, Not-in-family, Other-relative, Unmarried.
  - race: **categorical with 5 levels.** Black, White, Asian-Pac-Islander, Amer-Indian-Eskimo, Other.
  - sex: **categorical with 2 levels. Female, Male.
  - capital-gain: continuous.
  - capital-loss: continuous.
  - hours-per-week: continuous.
  - native-country: **categorical with 41 levels.** United-States, Cambodia, England, Puerto-Rico, Canada, Germany, Outlying-US(Guam-USVI-etc), India, Japan, Greece, South, China, Cuba, Iran, Honduras, Philippines, Italy, Poland, Jamaica, Vietnam, Mexico, Portugal, Ireland, France, Dominican-Republic, Laos, Ecuador, Taiwan, Haiti, Columbia, Hungary, Guatemala, Nicaragua, Scotland, Thailand, Yugoslavia, El-Salvador, Trinadad&Tobago, Peru, Hong, Holand-Netherlands.


# Key Methodology

## Machine Learning - Classification


# How does this project work?
To run the project successfully on a local machine, we need to have the following preparations:



