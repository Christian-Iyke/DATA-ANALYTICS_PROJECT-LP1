# DATA ANALYSIS PROJECT -- INDIAN STARTUP FUNDING

## Data Analysis is the process of inspecting, cleaning, processing, and modeling data to extract meaningful information to make decisions.

## Ideas, creativity, and execution are essential for a start-up to flourish. But are they enough? Investors provide start-ups and other entrepreneurial ventures with the capital---popularly known as "funding"---to think big, grow rich, and leave a lasting impact. In this project, I am going to analyse funding received by start-ups in India from 2018 to 2021.

## This project uses a dataset about the Indian start-up companies and their information such as:

## Company/Brand: Name of the company/start-up

## Founded: Year start-up was founded

## Sector: Sector of service

## What it does: Description about Company

## Founders: Founders of the Company

## Investor: Investors

## Amount($): Raised fund

## Stage: Round of funding reached.

## To perform exploratory data analysis and draw insights from useful information found. One of the great ways for a good analysis to work is to understand the business problem you are trying to solve. For a better understanding of the problem, create an objective or a scenario to work around.

## EDA is a data analysis technique used to understand all aspects of data. In this project, the CRISP–DM framework was adopted as a guide. This framework includes:

## Business Understanding: Understanding the needs of the company and the solutions requested from the data.

## Data Understanding information this involves exploring the data to understand what the dataset is about and all the information in the data.

## Data Cleaning or data preprocessing involves manipulating the data to draw insights and conclusions. It is also the cleaning of the data set by removing null values, and duplicate values, formatting the data types, removing inconsistent values, etc.

## PROJECT SCENARIO
## Your team is trying to venture into the Indian start-up ecosystem. As the data expert of the team you are to investigate the ecosystem and propose the best course of action.

## Your task is to develop a unique story from this dataset by stating and testing a hypothesis, asking questions, perform analysis and share insights with appropriate visualisations.

## So as part of the project you are to:

## Ask questions

## Develop hypothesis

## Process the data

## Analyse the data

## Visualise the data

## Let us start with the following:

# ASKING ANALYTICAL QUESTIONS

## 1) What is the total amount raised by all the investors
## 2) Which sector has the highest amount invested.
## 3) Which year has the most start up founded.¶
## 4) Which Headquarters has the highest funding.
## 5) Which Company has the highest amount invested.

# DEVELOPING THE HYPOTHESIS

## HO (Null): Sector of service is not dependent on the amount raised.¶
## H1(Alternative): Sector of service is dependent on the amount raised.

## BUSINESS UNDERSTANDING

### Your team is trying to venture into the Indian start-up ecosystem. As the data expert of the team you are to investigate the ecosystem and propose the best course of action.

## DATA UNDERSTANDING

### This involves exploring the data to understand what the dataset is about and all the information in the data. The 2018 to 2021 datasets are to be analysed to get better understanding of the data.


## This is done by first importing all the liberies as shown below: 

### import pandas as pd
### import numpy as np
### import matplotlib.pyplot as plt

### import plotly.express as px
### import plotly.graph_objs as go

### import seaborn as sns

### from scipy import stats
### import statistics as stat

### from sklearn.impute import SimpleImputer

## Datasets loading as shown below:

### startup_2018= pd.read_csv(r'C:\Users\User\Desktop\AZUBI AFRICA\Projects\LP 1\startup_funding2018.csv')

### startup_2019 = pd.read_csv(r'C:\Users\User\Desktop\AZUBI AFRICA\Projects\LP 1\startup_funding2019.csv')

### startup_2020 = pd.read_csv(r'C:\Users\User\Desktop\AZUBI AFRICA\Projects\LP 1\startup_funding2020.csv')

### startup_2021 = pd.read_csv(r'C:\Users\User\Desktop\AZUBI AFRICA\Projects\LP 1\startup_funding2021.csv')


## After loading the datasets, the following were done to help have a better understanding of the data:

### 1) checking the datatypes with .dtype and .info() methods. Example: startup_2018.info() or .dtype

### 2) Checking for missing values with .isna().sum() method. Example; startup_2018.isna().sum()

### 3) Checking for duplicate values with .duplicated() method. Example; startup_2018.duplicated()

### 4) checking the shape of the dataset with .shape method. Example; startup_2018.shape

### 5) Checking the head and  tail of the data with .head() and .tail() methods. Example; startup_2018.head() or .tail()



# DATA PROCESSING

### This involves manipulating the datasets to enable us draw insight and make dicisions. Here, all the null values were treated using simpleImputer and applying transformation which took care of both numerical values and the categorical values.

### Also, duplicated rows were removed and every other anomalis were taken care off. The colums that the datatype were supposed to be int, float or objects were changed to their supposed datatypes.

### Note: this is done on the individual datasets.

### also, Columns which are not needed were removed.

### at this point, all dataset cleaned is been saved and will be called up in the next stage of Analying and Visualising the data.


# ANALYSING AND VISUALISING THE DATA.

## At this stage, all the four datasets that have been cleaned were read and concatinated as one single data as shown below:

### Combining the datasets as one dataset

### new_data = pd.concat([cleaned_2018,cleaned_2019,cleaned_2020,cleaned_2021], ignore_index=True)

### with this, we now have a single data that we can analyse.

### from here, we recall or Analytical Questions and Hypothesis Statement and try to do justice to them.



# HYPOTHESIS

## HO (Null): Year of Funding is not dependent on the amount raised.¶
## H1(Alternative): Year of Funding is dependent on the amount raised.


# HYPOTHESIS TESTING

## OUR SIGNIFICANCE LEVEL IS 5%

## WE ARE USING T TEST

## performing two sample t-test

## yr = cleaned_new_data['Year of Funding']

## amt = cleaned_new_data['Amount($)']

## t,p = stats.ttest_ind(a=yr, b=amt) 

## print(f't-value: {t}')
## print(f'p-value: {p}')

## Output: 
## t-value: -1.9259817260698
## p-value: 0.05415588405118259

## Using this function, we were able to either accept or reject our result.

### print("p-value for significance is: ", p)

### if p<0.05:
###        print("reject null hypothesis")
### else:
###        print("accept null hypothesis")

### p-value for significance is:  0.05415588405118259
### accept null hypothesis

## So, from the above result, Since the p-value of the test (0.0541) is equal to or greater than .05, we accept the null hypothesis.

## This means we have sufficient evidence to say that the Year of Funding is not dependant on the Amount raised.¶



# ANALYTICAL QUESTIONS

## 1) What is the total amount raised by all the investors
## 2) Which sector has the highest amount invested.
## 3) Which year has the most start up founded.¶
## 4) Which Headquarters has the highest funding.
## 5) Which Company has the highest amount invested.
