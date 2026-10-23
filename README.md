# Healthcare Admissions, Billing & Length of Stay Analysis

Healthcare operational analytics project using Power Query, Power BI and DAX to analyze admission patterns, patient demographics, medical conditions, hospital activity, billing and length of stay.

## Project Overview

Healthcare organizations generate large volumes of patient and admission data, but raw records do not immediately provide a clear view of admission patterns, billing variation, hospital activity or length of stay.

This project transforms a healthcare admissions dataset into an interactive Power BI report designed to identify meaningful patterns across demographics, medical conditions, hospitals, admission types, billing and length of stay.

## Business Problem

The analysis explores how healthcare admission records can be used to understand:

- Admission patterns across patient demographics and medical conditions
- Hospital and admission activity
- Billing variation across conditions, hospitals and admission types
- Length-of-stay patterns
- Differences in billing across admission duration

## Objectives

- Analyze admission patterns across demographics, medical conditions, admission types and recorded years.
- Examine billing patterns across medical conditions, admission types, hospitals and other relevant characteristics.
- Analyze length-of-stay patterns and assess how billing varies across different lengths of stay.
- Develop an interactive Power BI report that communicates the findings clearly.

## Business Questions

1. What are the overall patterns in admissions, billing, length of stay, patient demographics and admission activity over time?
2. Which demographic groups and medical conditions account for the largest share of recorded admissions?
3. How do hospitals and admission types differ in terms of admission volume, length of stay and billing?
4. How does billing vary across medical conditions, admission types, hospitals and different lengths of stay?
5. What are the most significant patterns and differences identified in the data?

## Dataset

- Dataset: Healthcare Dataset
- Source: Kaggle
- Original records: 55,500
- Final analytical records: 49,904
- Structure: Single-table dataset

The dataset contains patient demographics, medical conditions, hospital information, admission and discharge dates, billing information, admission types, medications and test results.

## Data Preparation

The raw dataset was prepared in Power Query.

Key preparation steps included:

- Correcting relevant data types
- Standardizing text fields such as patient names
- Converting admission and discharge dates into appropriate date formats
- Identifying and removing duplicate observations
- Creating age groups for demographic analysis
- Calculating length of stay
- Identifying and excluding records with negative billing amounts
- Validating the final analytical dataset

The dataset was reduced from 55,500 original records to 49,904 records retained for analysis.

A separate Data Cleaning Log documents the major cleaning decisions and record-count changes.

## Data Model & Analysis

The project uses a single-table analytical model. Calculated fields and DAX measures were created in Power BI to support KPIs, comparisons and dashboard visuals.

Key analytical fields include:

- Age Group
- Year
- Length of Stay
- Admission Type
- Medical Condition
- Hospital
- Billing Amount
- Patient Demographics

## Dashboard

The Power BI report contains five analytical pages:

1. Healthcare Overview
2. Patient Demographics & Conditions
3. Hospital & Clinical Performance
4. Billing & Length of Stay
5. Key Insights

The dashboard provides an interactive view of admissions, demographics, clinical activity, hospital performance, billing and length-of-stay patterns.

## Key Findings

- Admissions Are Spread Almost Evenly Across Adult Age Groups. Each group from 20 to 79 accounts for 14.5% to 15.1% of admissions. The 50-59 group is highest (15.1%) but leads by less than one point, so age alone does not explain admission volume. 
- Admissions Are Split Evenly By Gender. Female patients account for 50.01% and male patients 49.99%, so gender does not separate admission volume. 
- Admissions Were Stable From 2020 to 2023. They stayed between 9.86K and 10.14K per year. The lower counts in 2019 (6.62K) and 2024 (3.45K) are consistent with partial coverage, since the data runs from May 2019 to May 2024. Year-over-Year comparisons that include those two years would be misleading. 
- Billing Is Nearly Uniform Across Conditions, Admission Types and Length of Stay. Average billing ranges only from $25.28K (cancer) to $25.84K (obesity). Elective ($25.67K) and emergency ($25.57K) admissions are almost identical. None of these is a meaningful cost driver. 
- Hospital Rankings Are Not Reliable In This Dataset. There are about 39,800 distinct hospital names across 49,904 admissions, so most hospitals have one or two records. The "top" hospital by total billing mainly reflects having more admissions, not higher costs.


## Limitations

- The dataset is a single-table healthcare admissions dataset and does not represent a complete clinical or financial information system.
- Duplicate records were identified using the available encounter-related fields because the source did not provide a dedicated encounter identifier.
- Negative billing amounts were excluded because the analysis treats Billing Amount as a positive charge associated with an admission; the source did not establish whether negative values represented legitimate refunds, reversals or credits.
- Findings describe patterns in the available dataset and should not automatically be generalized to all healthcare organizations.

## Tools

- Power Query
- Power BI
- DAX
- Excel

## Project Files

- Power BI report
- Healthcare dataset
- Data Cleaning Log
- Project Documentation
- Dashboard/exported report

## Outcome

The project demonstrates an end-to-end healthcare analytics workflow:

Data preparation → Transformation → DAX analysis → Interactive dashboard → Business insights

## Author

Sofeeyah Adekunle
Data Analyst
