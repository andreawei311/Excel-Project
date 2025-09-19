# Data Science Job Market Analysis
## Overview
This project analyzes the 2023 global job market data for roles in data science and related fields. The dataset includes information about job titles, salaries, locations, employment types, and education requirements. A dashboard is included to provide interactive insights and visual summaries.

## Objectives

1. For salary benchmarking in the data industry: Analyzing salary ranges across job roles and geographies.
2. For Exploratory data analysis (EDA) for job market trends: 
    - Exploring demand for specific job titles.
    - Comparing the availabilities of full-time vs. contract roles.
3. For job seekers: Assessing the impact of degree requirements on job search.

## Book No. 1 - Dashboard and Formulas

The Excel workbook [book1_dashboard_and_formulas.xlsx](book1_dashboard_and_formulas.xlsx) contains six sheets:

1. Dashboard: A high-level summary view with interactive charts and tables, designed for easy exploration of job trends and salary distributions.
2. Data: The dataset containing detailed records of job postings; the following sheets were created based on this dataset.
3. 'job_title': A lookup of job titles, as well as aggregated salary information.
4. 'job_country': A lookup of job countries and aggregated values of counts and salaries.
5. 'job_type': A lookup/breakdown/formatting of job schedule types.
6. 'degree_or': Counts of boolean values in the 
'job_no_degree_mentioned' column in the Data sheet.

### Features Used
**Data Validation:** used in Dashboard 

### Key Functions and Formulas

#### Sheet 'job_title': 
- UNIQUE() – extracts distinct job titles. \
- MEDIAN(IF(...)) – calculates the median salary for a - specific job title, filtered by conditions like country, salary non-zero, and schedule type. \
- SORT() – sorts job titles with corresponding median salaries. \
- IF() – conditional checks for highlighting/assigning values. \
- XLOOKUP() – retrieves salary values for a given title.

#### Sheet 'job_country':
- UNIQUE() – lists all unique countries.
- MEDIAN(IF(...)) – calculates median salary for a given job title in a specific country, filtered by conditions.
- COUNT(IF(...)) – counts number of job postings meeting those conditions.
- XLOOKUP() – retrieves counts/salaries for selected countries.

#### Sheet 'job_type':
- UNIQUE() – lists unique job schedule types (full-time, contract, etc.).
- FILTER() with ANCHORARRAY() – filters out invalid or duplicate schedule types.
- SEARCH() – detects substrings (like "and" or ",") in job schedule strings.
- MEDIAN(IF(...)) – computes median salary by job type under conditions.
- IF() – separates results based on whether job type matches a selected category.

#### Sheet 'degree_or'
- COUNT(IF(...)) – counts jobs requiring or not requiring a degree, filtered by title, country, salary, and job type.
- Boolean logic with job_no_degree_mention – separates postings with and without degree requirements.

## Book No. 2 - Pivot Tables

The Excel workbook [book2_pivot_tables.xlsx](book2_pivot_tables.xlsx) contains three pivot tables:
1. Pivot Table 1 - Average Annual Salary v. Job Count.
2. Pivot Table 2 - Number of Job Postings by Month. 
3. Pivot Table 3 - Global Overview.

This workbook provides similar analysis to Book No. 1, but the results are presented in Pivot Tables and Pivot Charts.