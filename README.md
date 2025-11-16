# Data-Cleaning-Pipeline


The use of Machine Learning Algorithms is not required for every dataset, but every dataset does require some data cleaning steps. So, building a data cleaning pipeline using Pandas is one of those bread-and-butter tasks every Data Scientist should master early on.

A reusable pipeline for cleaning tabular data using Python’s Pandas library.
# Project Overview
This project implements a standardized cleaning pipeline built with Pandas that can be applied to datasets (for example, loan-approval data) to ready them for analysis or modeling. The pipeline handles tasks such as missing value imputation, data-type corrections, text standardization, and outlier capping.
# Repository Structure
<img width="773" height="401" alt="image" src="https://github.com/user-attachments/assets/9d150f76-6d0c-4caa-9997-28c5b09d265f" />
# Features
1.Fill missing values:
   a.For categorical variables: replace with mode
   b.For numeric variables: replace with median
2. Convert data types and optimize:
   a.Cast object columns to category where appropriate
   b.Standardize text (strip whitespace, convert to lower case)
3.Outlier handling:
   a. Cap numeric columns (e.g., ApplicantIncome, LoanAmount) at the 99th percentile
4. Modular function:
      clean_loan_data(df) which encapsulates the above steps
