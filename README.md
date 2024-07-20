# Human-Resource-Dashboard


### Table of Content
- [Project Overview](#project-overview)
- [Data Source](#data-source)
- [Tools](#tools)
- [Data Cleaning / Preparation](#data-cleaning-/-preparation)
- [Data Modelling](#data-modelling)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Dax, Functions and Formulas](#dax,-functions-and-formulas)
- [Results / Findings](#results-/-findings)
- [Recommendations](#recommendations)

### Project Overview

This project shows the trend of hires and exits in an organization. It also breaks down the payment structure of each department in the company including basic pay, allowances, tax, and cost to the employer. 
It tracks employees' performance, period of hire and cause of exit for every gender. 
This helps the HR department have an holistic access to the performance of a staff and can easily decide on promotion based or other compensations.

### Data Source

Human Resource Data: Finex skills provided this data “HR Dashboard.csv”. 
The document contains the monthly payroll, employee information(Register), Tracker. We have payroll for 6 months in the workbook but can still be updated in future dates.

### Tools

 - Microsoft Excel (Data cleaning, Data analysis, and Data visualization)

### Data Cleaning / Preparation

Power Pivot helps me model my data by creating a connection between my Fact and dimension tables. This will allow me to query my data correctly and answer any question that the stakeholders would want to see. 
The diagram view of the Power Pivot page shows me the schema, and all I did was drag and drop the columns I wanted to connect.

### Exploratory Data Analysis

 - What is the total number of employees currently in the organization in terms of gender?
 - What are the most causes for exits in the organization?
 - Which department had the best appraisal in the past month?
 - Which department has the highest expense for the employer?

### DAX, Functions and Formulas

While working on this project I used some Excel functions and formulas in getting my result. I also used some DAX functions to filter my formula for accurate results.
 - DAX CALCULATE(COUNTROWS(Tracker),Tracker[Event] = "Hired",FILTER('Calendar','Calendar'[Date] <= MAX('Calendar'[Date]))) - CALCULATE(COUNTROWS(Tracker),Tracker[Event] = "Exit",FILTER('Calendar','Calendar'[Date] <= MAX('Calendar'[Date])))
 - Function (=IF(N5>0,N5,NA()))
 - Function (=XLOOKUP($C$3,Register[Name],Register[Picture Link]))

### Results / Findings

 - Currently the organization has 23% active staff 15 males and 8 females.
 - Since 2018 till date we’ve had 7 exits with 4 resignation and 3 terminations
 - The staff of finance department had the best appraisal with an average of 3.5/5



