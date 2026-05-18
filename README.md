# Credit Card Weekly Status Dashboard (Power BI)


Author: Shivani Bhatt

---

## Project Overview
This project is an end-to-end Power BI solution developed to analyze credit card customer behavior, transaction performance, and weekly revenue trends. It helps stakeholders make data-driven decisions using interactive dashboards.

---


## Objective
- Analyze customer segmentation and behavior
- Track transaction performance
- Monitor weekly revenue trends
- Generate actionable business insights

---


## Data Source
Two CSV datasets were used:
1. CreditCard.csv (Transactions, Revenue, Interest, Card Category, Dates)
2. Customer.csv (Age, Income, Job, Education, Gender, State)

Relationship:
Customer[Client_Num] → CreditCard[Client_Num]

---


## Implementation Steps

### Step 1: Data Import
- Imported CSV files into Power BI using Get Data

### Step 2: Data Cleaning
- Removed null values
- Verified data types
- Standardized date formats

### Step 3: Data Modeling
- Created relationship between Customer and CreditCard tables

---

## DAX Calculations

### Calculated Columns
Total_Revenue = Annual_Fees + Total_Trans_Amt + Interest_Earned  
Week_Num_2 = WEEKNUM(Week_Start_Date)

### Measures
Current_Week_Revenue = CALCULATE(SUM(Total_Revenue), FILTER(ALL(CreditCard), Week_Num_2 = MAX(Week_Num_2)))  
Previous_Week_Revenue = CALCULATE(SUM(Total_Revenue), FILTER(ALL(CreditCard), Week_Num_2 = MAX(Week_Num_2)-1))  
WOW_Revenue = DIVIDE((Current - Previous), Previous)


### Customer Segmentation
Age_Group → Based on Customer_Age  
Income_Group → Low, Medium, High  


---

# Dashboard 1: Customer Report

### KPIs
- Revenue: 57M
- Total Interest: 8M
- Income: 588M
- CSS: 3.19


### Charts
- Revenue by Week → Trend analysis
- Delinquent Accounts → Risk analysis
- Gender → Revenue comparison
- Age Group → Segmentation
- Job Table → Customer profession insights
- Top States → Regional analysis

### Slicers
- Quarter
- Week Start Date
- Card Category


<img width="1276" height="707" alt="Credit_Card_Customer_Report_Screenshot_10" src="https://github.com/user-attachments/assets/23fd15d8-c2c5-4336-9494-c42a59b9cb4f" />


---

## Dashboard 2: Transaction Report

### KPIs
- Revenue: 57M
- Interest: 8M
- Transaction Amount: 46M
- Transaction Volume: 667K


### Charts
- Card Category Table → Performance comparison
- Revenue by Category → Contribution
- QTR Chart → Trend comparison
- Expenditure Type → Spending behavior
- Customer Job → Target segmentation


### Slicers
- Income Group
- Quarter


<img width="1262" height="702" alt="Credit_Card_Transaction_Report_Screenshot_11" src="https://github.com/user-attachments/assets/12456d4d-5aa2-45d8-af9a-61eb6f6f6a70" />


---

## Dashboard 3: Extra Insights

### Purpose
Provides advanced weekly insights and performance tracking

### Components
- Weekly Revenue Table (Current, Previous, WoW)
- Delinquency Analysis
- Activation Analysis
- Transaction Trend
- Credit Limit Analysis


<img width="1138" height="648" alt="Extra_Insights_Report_Screenshot_12" src="https://github.com/user-attachments/assets/0e54c664-b02b-4692-b3d9-7f9a81bf0902" />


---

## Canvas Settings
- Size: 1425 x 780
- Customer Dashboard: Pink
- Transaction Dashboard: Green
- Insights Dashboard: Purple

---

## Key Insights
- Revenue shows weekly growth trend
- Low delinquency (~6%)
- High activation (~57%)
- Blue & Silver cards dominate
- Top states contribute most revenue

---

## Challenges
- Time-based DAX calculations
- Data modeling
- Dashboard design

---

## Conclusion
This project demonstrates Power BI dashboard development, DAX calculations, and business intelligence reporting. It provides clear insights for better decision-making.

---

## Tech Stack
- Power BI
- DAX
- CSV Data

---

## How to Use
1. Open .pbix file in Power BI
2. Use slicers to filter data
3. Analyze dashboards

---

If you like this project, give it a star on GitHub!

