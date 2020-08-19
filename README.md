**Introduction**

Customer Defection or Churn is the loss of a client or customers. Telephone service companies, ISPs, insurance firms, etc, often use customer defection analysis and rates as one of their key business metrics because the cost of retaining an existing customer is far less than acquiring a new one.

Retention Rate is an indication of how good your product market fit (PMF). If your PMF is not satisfactory, you should see your customers churning very soon. One of the powerful tools to improve Retention Rate (hence the PMF) is Churn Prediction. By using this technique, you can easily find out who is likely to churn in the given period. In this article, we will use a Telco dataset and go over the following steps to develop a Churn Prediction model:

- Exploratory data analysis
- Feature Engineering
- Investigating how the feature affects Retention by using Logistic Regression.
- Building a classification model with XGBoost

**Objective Of The Project**

This project is aimed at solving a problem in the Telecommunication industry. Specifically to leverage Data in predicting customers retention rate and churning rate. By the end of this project, we would have gathered enough insights that can help decision makers to reduce the churn rate of the business in-turn increasing retention rate.

**Problem Statement**

_Companies usually make a distinction between voluntary defection (churn) and involuntary defection (churn). Voluntary defection occurs due to a decision by the customer to switch to another company or service provider, involuntary defection occurs due to circumstances such as a customer&#39;s relocation to a long-term care facility, death, or the relocation to a distant location. In most applications, involuntary reasons for churn are excluded from the analytical models. Analysts tend to concentrate on voluntary defection, because it typically occurs due to factors of the company-customer relationship which companies control, such as how billing interactions are handled or how after-sales help is provided. To solve this problem, We are tasked with the responsibility of building a predictive model that can help in identifying patterns and in-turn predicting whether a customer will churn or not._

It is a classification problem where we have to predict whether a customer will defect (churn) or Not. In a classification problem, we have to predict discrete values based on a given set of independent variable(s). Classification can be of two types:

- **Binary Classification** : In this classification we have to predict either of the two given classes. For example: classifying the gender as male or female, predicting the result as win or loss, etc

**Hypothesis Generation**

### What is hypothesis generation?

This is a very important stage in any data science/machine learning pipeline. It involves understanding the problem in detail by brainstorming as many factors as possible which can impact the outcome. It is done by understanding the problem statement thoroughly and before looking at the data.

Below are some of the factors which I think can affect the Churn rate (dependent variable for this churn prediction problem):

- Total Charges: The total amount a customer is charged over a period of service consumption.
- Monthly Charges: Month-on-month charges of a customer with respect to a service consumption.
- Tenure: The period which a customer has consistently patronised the business.
- Payment Method: The payment method the customer has enabled In paying for services being consumed.

These are some of the factors which i think can affect the target variable.

### Getting the system ready and loading the data

We will be using Python for this project along with the below listed libraries. The version of these libraries is mentioned below:

### **Specifications**

- Python 3
- pandas
- seaborn
- sklearn
- plotly


**Loading Packages**

import pandas as pd

import numpy as np # For mathematical calculations

import seaborn as sns # For data visualization

import matplotlib.pyplot as plt # For plotting graphs

%matplotlib inline

 **Data**

For this practice problem, we have been provided with a CSV file: which after the EDA was splitted into Train and Test sets

- Training set will be used for training the model, i.e. our model will learn from this set. It contains all the independent variables and the target variable.
- Test set contains all the independent variables, but not the target variable. We will apply the model to predict the target variable for the test data

**References**

1. Baris Karaman [https://towardsdatascience.com/churn-prediction-3a4a36c2129a](https://towardsdatascience.com/churn-prediction-3a4a36c2129a)
