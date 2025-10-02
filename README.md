# MIS581-Capstone-Project
**Project Overview**

This repository contains the programming code and output figures from my MIS581 Capstone Project. The study analyzed loan-level data from the SBA 7(a) program covering fiscal years 2020 through 2024 to identify factors associated with early loan failure. For the purposes of this analysis, early failure was defined as a loan charged off within 24 months of approval.

The project applied descriptive statistics, hypothesis testing, and logistic regression to evaluate differences across approval cohorts, loan size, geography, and industry. The results provide insight into the risks of early charge-off and highlight important predictors that can inform SBA oversight, lender practices, and borrower decision-making.

**Repository Contents**
Data Source: Due to file size constraints, the raw SBA 7(a) loan-level datasets are not included in this repository. They are publicly available through the U.S. Small Business Administration’s official website: https://data.sba.gov/dataset/7-a-504-foia

MIS581 - Capstone Project.ipynb – Jupyter Notebook with data cleaning, descriptive statistics, hypothesis testing, and logistic regression.

Outputs (tables): 

table1_two_proportion_cohort.csv – Results of the two-proportion z-test comparing cohorts.

cohort_counts_successes.csv – Cohort counts of loans and early charge-offs.

rate_by_size.csv – Early charge-off rates by loan size group.

rate_by_state_top10.csv – Early charge-off rates by top 10 states.

rate_by_naics2_top10.csv – Early charge-off rates by top 10 industries.

rate_by_year.csv – Early charge-off rates by approval year.

model1_OR_CI.csv – Logistic regression results (odds ratios with confidence intervals).

Datasets (cleaned for analysis): 

7a_model_dataset_24m.csv – Filtered dataset with variables used in modeling (≥24 months follow-up).

7a_clean_full.csv – Cleaned dataset with final statuses, size bins, and derived fields.
figures/ – PNG figures generated from the analysis:

Figures

figure1_cohort_rates.png – Early charge-off rates by approval cohort.

figure2_size_rates.png – Early charge-off rates by loan size.

figure3_states_top10.png – Early charge-off rates by top 10 states.

figure4_naics2_top10.png – Early charge-off rates by top 10 industries.

figure5_forest_or.png – Logistic regression odds ratios with confidence intervals.

**Tools and Libraries**

The analysis was completed in Python 3.12 using the following libraries:

pandas – data cleaning and manipulation

numpy – numerical operations

statsmodels – statistical modeling and logistic regression

scipy – hypothesis testing (two-proportion z-test, chi-square)

matplotlib – visualization of descriptive and regression results

To install dependencies:

pip install pandas numpy statsmodels scipy matplotlib

**Key Findings**

Baseline Risk: About 7.5% of loans in the dataset experienced an early charge-off.

Cohort Effect: Loans approved in 2022–2024 were nearly twice as likely to fail early compared with those from 2020–2021.

Loan Size: Smaller loans had much higher risk (11.2%) compared to larger loans (2.3%).

Industry: Construction, retail trade, and food services had significantly higher odds of early charge-off, while industries such as professional services and health care performed more favorably.

Regression Analysis: Cohort, loan size, and industry were confirmed as significant predictors of early failure, even after adjusting for geography.

