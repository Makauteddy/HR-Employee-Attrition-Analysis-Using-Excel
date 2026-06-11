## HR Employee Attrition Analysis Using Microsoft Excel
# 1. Introduction

Employee retention is a critical factor for organizational success. High employee turnover increases recruitment costs, reduces productivity, and affects workforce stability. Organizations need data-driven approaches to understand why employees leave and what strategies can improve retention.

This project analyzes employee attrition patterns using HR workforce data to identify key factors influencing employee turnover. The analysis was conducted using Microsoft Excel by applying data cleaning techniques, Excel formulas, Pivot Tables, Pivot Charts, and dashboard development.
# 2. Project Description

This project focuses on analyzing employee data to understand workforce trends, employee satisfaction levels, compensation factors, and possible reasons behind employee attrition.

The analysis transforms raw HR data into meaningful business insights that support decision-making in areas such as:

      1. Employee retention strategies
      2. Workforce planning
      3. Compensation management
      4. Employee engagement improvement

# 3. Business Problem

Employee turnover is a major challenge for organizations because it affects operational efficiency, employee morale, and financial performance.

The HR department wants to understand:

1. Which employees are most likely to leave?
2. What factors contribute to employee turnover?
3. Which departments have the highest attrition?
4. Does compensation influence employee retention?
5. Does overtime and workload contribute to employees leaving?

The goal is to identify attrition drivers and provide actionable insights to reduce employee turnover.

# 4. 4. Data Description
Dataset Source
https://www.kaggle.com/datasets/anshika2301/hr-analytics-dataset/data?select=HR_Analytics.csv
## Dataset Overview
# Variable	Description
EmpID- Unique employee identifier
Age	- Employee age
AgeGroup- Employee age category
Attrition - Whether employee left organization (Yes/No)
Department - Employee department
JobRole -	Employee position
JobLevel - Employee career level
MonthlyIncome - Employee salary
SalarySlab - Salary category
OverTime - Whether employee works overtime
BusinessTravel - Work travel frequency
JobSatisfaction - Employee satisfaction score
EnvironmentSatisfaction - Workplace satisfaction score
RelationshipSatisfaction - Workplace relationship score
WorkLifeBalance - 	Work-life balance rating
YearsAtCompany - Employee tenure
YearsInCurrentRole - Time in current position
YearsSinceLastPromotion	- Time since promotion
TrainingTimesLastYear - Training frequency
PerformanceRating- Performance score
# Variable	Coding
Attrition	Yes = Employee Left, No = Employee Stayed
OverTime	Yes / No
Satisfaction Scores	1 = Low, 4 = High
Performance Rating	3 = Good, 4 = Excellent

## 5. Objectives and Research Questions

Measure overall employee attrition rate.
Identify departments with the highest employee turnover.
Analyze the relationship between overtime and attrition.
Determine whether salary influences employee retention.
Understand how satisfaction and career growth affect employee decisions.
Identify employee groups with higher attrition risk.

## 6. Methodology
Step 1: Data Cleaning

The dataset was prepared by:

Checking missing values
Removing duplicates
Validating data types
Standardizing categorical fields
Ensuring consistency in employee records
Step 2: Feature Creation

Additional analysis fields were created:

Attrition Flag
=IF([@Attrition]="Yes",1,0)
Employee Risk Category
=IF(AND([@OverTime]="Yes",
[@JobSatisfaction]<=2),
"High Risk","Low Risk")
Tenure Groups

Employees were grouped into:

0–2 Years
3–5 Years
6–10 Years
10+ Years
Step 3: Exploratory Data Analysis

Analysis was performed using:

Summary statistics
Pivot Tables
Conditional formatting
KPI calculations
Step 4: Dashboard Development

An interactive Excel dashboard was created using Tableau
7. Answering the research Questions
