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
   
# Usage

1. Install dependencies:
   pip install -r requirements.txt
2. Place your raw dataset (e.g., loan_prediction.csv) into the data/raw/ folder.
3. Run the cleaning script:
    python src/run_cleaning.py --input data/raw/loan_prediction.csv --output data/cleaned/cleaned_loan_data.csv
4. Cleaned dataset will be output to the specified folder, ready for further analysis or      modeling.

# Why This Pipeline??
  
Datasets often come with a variety of issues: missing values, inconsistent types, unstandardized text, extreme outliers. This pipeline addresses those common problems in a straightforward, reusable way — helping to reduce errors and preprocessing time in downstream tasks.


# Example

   import pandas as pd
from src.clean_pipeline import clean_loan_data

df = pd.read_csv('data/raw/loan_prediction.csv')
df_clean = clean_loan_data(df)
df_clean.to_csv('data/cleaned/cleaned_loan_data.csv', index=False)



# Notes & Extensions

1. This pipeline focuses on general preprocessing; domain-specific cleaning (e.g., feature engineering, encoding, scaling) should be handled separately.
2. Outlier capping uses a fixed upper percentile (99th) by default; adjust as appropriate for your dataset.
3. Custom cleaning steps (e.g., handling ultra-high cardinality features, merging categories) can be added into the function.
4. Ensure reproducibility by fixing random seeds and documenting versioning of dependencies.

# Requirements
1. Python3
2. Pandas

# Contributing
Contributions, suggestions or improvements are welcome. Feel free to open an issue or pull request.




