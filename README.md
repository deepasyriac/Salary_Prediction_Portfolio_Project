# Predict the salaries of new job postings

## Introduction

In this project I am analysing a  dataset of job postings with salaries and then predict salaries for a new set of job postings. After analysing the given data the predicted salary will be depend on different features like Job type, company name, degree type, major specialization, Industry type, Year of Experience and miles from metropolis of each job posting. For this project I have developed predictive models for finding the target variable salary for new job postings. The language which I used is Python and the libraries are Pandas, numpy, matplotlib ,sklearn, seaborn.
</br>
## Data Cleaning

###### Load and clean the data

Pandas library has been used to read the dataset from the given .csv files and stored to data frames and cleaned the data (Check for duplicate and null values).
</br>
## Exploratory Data Analysis (EDA)

The given data can be divided into categorical features and numerical features. 
###### Categorical features
- companyID :The company which the job has been posted
- jobType :Depends on the level of their jobs like CEO,Manager and Junior.
- degree :The educational qualification of the employee
- major :The main subject in their educational qualification
- industry :The industry whic company belongs to such as Oil or Finance
###### Numerical features
- yearsExperience :The number of year of experience required for the job posting.
- milesFromMetropolis :The distance from the major city which company is located to the place which employee stay
- salary :Salary for the job posting(Target variable)
