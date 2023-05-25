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

### 1) checking the datatypes with .datatype and .info() methods

### 2) Checking for missing values with .isna().sum() method

### 3) Checking for duplicate values with .duplicated() method

### 4) checking the shape of the dataset with .shape method

### 5) Checking the head and  tail of the data with .head() and .tail() methods




