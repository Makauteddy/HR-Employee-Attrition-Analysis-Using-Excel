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

# 4. Data Description
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

# 5. Objectives and Research Questions
            
            Measure overall employee attrition rate.
            Identify departments with the highest employee turnover.
            Analyze the relationship between overtime and attrition.
            Determine whether salary influences employee retention.
            Understand how satisfaction and career growth affect employee decisions.
            Identify employee groups with higher attrition risk.

# 6. Methodology
### Step 1: Data Cleaning
      
The dataset was prepared by:
      Checking missing values
      Removing duplicates
      Validating data types
      Standardizing categorical fields
      Ensuring consistency in employee records
### Step 2: Feature Creation

2.1 Additional analysis fields were created:
      Attrition Flag
      =IF([@Attrition]="Yes",1,0)
      Employee Risk Category
      =IF(AND([@OverTime]="Yes",
      [@JobSatisfaction]<=2),
      "High Risk","Low Risk")
2.2 Tenure Groups
      Employees were grouped into:
      0–2 Years
      3–5 Years
      6–10 Years
      10+ Years
### Step 3: Exploratory Data Analysis
      Analysis was performed using:
      Summary statistics
      Pivot Tables
      Conditional formatting
      KPI calculations
### Step 4: Dashboard Development
An interactive Excel dashboard was created using Tableau

# 7. Answering the research Questions
## 7.1 What is the overall employee attrition rate?
####  7.1.1 Total Employees
<img width="259" height="73" alt="image" src="https://github.com/user-attachments/assets/8da8c1a5-4e84-40bb-851f-86f840f5dd76" />
<img width="152" height="77" alt="image" src="https://github.com/user-attachments/assets/0c1f78c4-de72-44e9-abe6-7b2e94712448" />

There are 1,473 employees found in this dataset.
#### 7.1.2	Employees who left
<img width="313" height="72" alt="image" src="https://github.com/user-attachments/assets/9016a9f0-bd8d-46a1-81ea-0d90314d7830" />
<img width="134" height="86" alt="image" src="https://github.com/user-attachments/assets/b6c5fe09-23d7-484e-bfc9-4f5bef0729b8" />

There are 237 employees who left  which indicates  that 237 of employees in the dataset have ended their association with the company.

#### 7.1.3	Attrition Rate
<img width="584" height="86" alt="image" src="https://github.com/user-attachments/assets/fc3ebcd8-a5bb-424d-8c63-d052c4ffcd33" />
<img width="130" height="67" alt="image" src="https://github.com/user-attachments/assets/14501368-8ed0-42a9-91b2-cf9a10b72355" />

The attrition rate indicates that  16.09% of employees in the dataset have ended their association with the company.

## 7.2 How many Employees work in each department?

<img width="561" height="75" alt="image" src="https://github.com/user-attachments/assets/5f3edd69-51b7-4aa5-90e0-e9ae35d65296" />
<img width="331" height="156" alt="image" src="https://github.com/user-attachments/assets/532c7f03-2618-464a-9c33-59faaff180e0" />

There are 447 employees in Sales, 63 in Human Resources, and 963 in Research & Development found in this dataset.

## 7.3 Which department has the highest attrition?
<img width="864" height="92" alt="image" src="https://github.com/user-attachments/assets/7253474e-6313-4003-b5ee-f38d21de6dbf" />
<img width="375" height="158" alt="image" src="https://github.com/user-attachments/assets/8a560ea6-eb25-4ba8-8eaf-d4129606174f" />

There are 92 attritions in Sales, 12 in Human Resources, and 133 in Research & Development found in this dataset.
The total attrition of 133 indicates that a significant portion of employees in the Research & Development department have ended their association with the company, making it the department with the highest overall volume of departures. 

## 7.4 Does overtime contribute to attrition?
### 7.4.1 Employees who left and worked overtime
<img width="514" height="88" alt="image" src="https://github.com/user-attachments/assets/f82e12a1-be5e-4a78-a567-5d87cd356f17" />
<img width="159" height="89" alt="image" src="https://github.com/user-attachments/assets/9c83487b-2ae8-44a7-8f73-39ed62f49679" />

The count of 127 employees who left and worked overtime indicates that a significant portion of employees who left the company were working overtime, suggesting that workload pressures may contribute to attrition.

### 7.4.2 Attrition rate for overtime employees
<img width="538" height="120" alt="image" src="https://github.com/user-attachments/assets/ca9ec942-27a3-44c5-b62b-31c54f67ccde" />
<img width="138" height="81" alt="image" src="https://github.com/user-attachments/assets/de004cb8-efc0-47d3-89b2-a86d18f8148d" />

The attrition rate of 53.59% indicates that a significant portion of employees who work overtime have ended their association with the company, highlighting workload as a potential driver of turnover.

## 7.5 Which employees age group are leaving most often?

<img width="644" height="97" alt="image" src="https://github.com/user-attachments/assets/f68ae9a0-1414-4de7-89e8-f449fa802153" />
<img width="308" height="213" alt="image" src="https://github.com/user-attachments/assets/a73a2d7c-5caa-4873-a477-fa01b284f980" />

The total attrition of 116 indicates that a significant portion of employees in the 26-35 age group have ended their association with the company, making it the age bracket with the highest overall volume of departures.

## 7.6 Does Salary influence attrition?
<img width="731" height="86" alt="image" src="https://github.com/user-attachments/assets/74b9a3ed-90dd-49cf-91f8-feb79379d1ec" />
<img width="286" height="159" alt="image" src="https://github.com/user-attachments/assets/9f7dc6ce-5cfd-42b1-9bc3-3b3a21e409c0" />

There are 192 attritions in the Low income category, 38 in the Medium income category, and 7 in the High income category found in this dataset. This indicates that  employees in the Low income category have ended their association with the company, demonstrating that compensation level strongly influences employee retention.

## 7.7 Average income of employees who stayed?
<img width="630" height="109" alt="image" src="https://github.com/user-attachments/assets/db3567dd-62b6-4424-88d8-c64c072fdbcb" />
<img width="159" height="84" alt="image" src="https://github.com/user-attachments/assets/7b2c68ab-e22f-4c02-9388-5a5f5590ed24" />

An average monthly income of $6,828.72 for employees who stayed which indicates that a significant portion of employees who remain with the company enjoy higher stable compensation, contrasting with those in lower salary brackets who are more prone to attrition.

## 7.8 Does job satisfaction affect attrition?
### 8.1 Employees with job satisfaction =1 who left
<img width="555" height="88" alt="image" src="https://github.com/user-attachments/assets/cda4dfa5-4fee-40ca-a494-352ce8cd9628" />
<img width="158" height="77" alt="image" src="https://github.com/user-attachments/assets/667dc91c-6209-4d32-bd04-a7bf61843ebb" />

There are 66 employees with a job satisfaction score of 1 found in this dataset, indicating that low job satisfaction is a key driver of workforce turnover since a significant portion of those who departed reported the lowest level of satisfaction.

### 8.2 Average job satisfaction of employees who left
<img width="592" height="69" alt="image" src="https://github.com/user-attachments/assets/716fdfeb-386e-4af0-8ba3-71c89e56b391" />
<img width="148" height="83" alt="image" src="https://github.com/user-attachments/assets/8f54b8fa-1d92-4754-b783-8c79a1c401da" />
There are 1,473 total employees analyzed in this dataset, and the average job satisfaction score of 2.47 for those who left indicates that departing employees generally experienced lower overall satisfaction before ending their association with the company.

##  9.Does work-life balance influence employee retention?
### 9.1  Employees who left with poor work-life balance
<img width="541" height="92" alt="image" src="https://github.com/user-attachments/assets/c78f9401-7fc9-44a1-94e0-25b9801d8a43" />
<img width="150" height="86" alt="image" src="https://github.com/user-attachments/assets/84b88822-b4e3-43fa-8521-5cfd06955804" />

There are 25 employees who left the company with a poor work-life balance found in this dataset, indicating that personal-professional equilibrium significantly influences employee retention since a notable portion of departures reported the lowest level of work-life balance.

### 9.2. Average work-life balance of employees who left
<img width="588" height="103" alt="image" src="https://github.com/user-attachments/assets/be9cfaf0-6f7d-4a5b-b205-24b7d6173dd6" />
<img width="166" height="86" alt="image" src="https://github.com/user-attachments/assets/ca27404b-ab47-412b-bd68-7d5be00d8bd3" />

The average work-life balance score for employees who left was 2.66, which highlights that difficulty balancing work and personal life is a major reason why people decide to quit.

## 10. Does environment satisfaction impact attrition?
<img width="669" height="123" alt="image" src="https://github.com/user-attachments/assets/f3b33f07-a846-444b-8244-dc8580abf59b" />
<img width="155" height="83" alt="image" src="https://github.com/user-attachments/assets/78f0079f-3908-480e-8168-9049d339d850" />

The average workplace environment satisfaction score for employees who left was 2.46, which shows that being unhappy with the actual work environment is a significant factor in why employees choose to leave the company.

























