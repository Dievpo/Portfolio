# 01_Data_preprocessing

## Project description
Client - bank credit department.
Input data - customers solvency statistics.

Target - determine whether the marital status and number of children of the customer affects the fact of repayment of the loan on time.
## Data Description
- children - number of children in the family
- days_employed - total work experience in days
- dob_years - client's age in years
- education — the level of client's education
- education_id — education level identifier
- family_status
- family_status_id
- gender
- income_type - type of employment
- debt - whether he had debt to repay loans
- total_income - monthly income
- purpose - the purpose of obtaining a loan

## What's done:
-  data preprocessing:  
    -  detection, correction and removal of missing values  
    -  data types correction  
    -  duplicates detection and removal  
    -  strings features lemmatization  
    -  category features obtention from other features  
-  4 hypotheses were tested and rejected:  
    -  about the relationship between the presence of children and loan repayment on time  
    -  about the relationship between marital status and loan repayment on time  
    -  about the relationship between income level and loan repayment on time 
    -  about the relationship between the purpose of obtaining a loan and its repayment on time 

## Used tool stack
- python
- pandas
