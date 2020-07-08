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
<br>
To check for the potential outliers, below figure shows the disrtibution of predicted variable salary.

![salary_distplot](https://github.com/deepasyriac/Salary_Prediction_Portfolio_Project/blob/master/salary_distplot.JPG)
![salary_boxplot](https://github.com/deepasyriac/Salary_Prediction_Portfolio_Project/blob/master/salary_boxplot.JPG)
<br>
The boxplot shows there are some outliers existing. After analysing the data using IQR method the data seems to be correct .The upperlimit outliers are acceptable eventhough the jobs are highly paid because they have higher degrees or they are working in highly paid industries. The lowerlimit outliers are 5 records with zero salary and that are removed because zero salary employees are not acceptable.
<br/>
Below is the correlation matrix heatmap which shows the correlation between selected features and response
![salary_heatmap](https://github.com/deepasyriac/Salary_Prediction_Portfolio_Project/blob/master/salary_heatmap.png)
</br>
## Model Evaluation and Selection
The following three regression algorithms are used for creating models.
<br>1.Linear Regression
<br>2.Random Forest Regressor
<br>3.Gradient Boosting Regressor
The performance of the predicted models are evaluated using Mean Square Error(MSE) metrics.The MSE for each models given below: 
- Linear Regression -922.934
- Random Forest Regressor -388.097
- Gradient Boosting Regressor -359.025
<br>
Since the predictions are calculated using model with lowest MSE, I selected Gradient boosting regression algorithm as the best model (MSE=359.026).
Next I saved the predictions to a CSV file.
<br>The last step feature importance analysis was done to know which features were the most important in the model. The below graph shows the Job type, yearsexperience, milesFrommetropolis, and industry are the most important features in the model.


![feature_importance](https://github.com/deepasyriac/Salary_Prediction_Portfolio_Project/blob/master/feature_importance.JPG)
