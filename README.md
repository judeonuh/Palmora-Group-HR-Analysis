# Palmora-Group-HR-Analysis
This repository presents an analysis of Palmora Group HR Data.

---

## Dashboard
The analysis dashboard can be accessed [here]()  


## Company Overview
The Palmoria Group is a manufacturing company based in Nigeria with Mr Ayodeji Chukwuma as the CEO.

---

## Problem Statement
Palmora Group is embroiled in issues bordering on gender inequality in its 3 regions. Unfortunately, the media recently published the news with the headline “Palmoria, the Manufacturing Patriarchy”. This doesn’t look good for the owners of the business, based on their ambition to scale the business to other regions and even overseas. Cases like this can only spiral downwards, revealing other issues like the gender pay gap, amongst other possible issues.  

---

## Aim  
To analyse Palmora Group HR Data to identify key areas within the business that could give rise to issues, and suggest recommendations for management’s attention.  

---

## 📁 Table of Contents
- [Company Overview](#company-overview)
- [Problem Statement](#problem-statement)
- [Aim](#aim)
- [Data Overview](#data-overview)  
- [Methodology](#methodology)
- [Data Cleaning](#data-cleaning)
- [Analysis and Recommendations](#analysis-and-recommendations)  
  - [1. Highest Sales Product Category](#1-highest-sales-product-category)  
- [Overall Recommendations](#overall-recommendations)  
- [Conclusion](#conclusion)  

---

## Data Overview
- **Source:** [Palmora Group emp-data](https://github.com/judeonuh/Palmora-Group-HR-Analysis/blob/main/Palmoria%20Group%20emp-data.csv) and [Palmora Group Bonus Rules](https://github.com/judeonuh/Palmora-Group-HR-Analysis/blob/main/Palmoria%20Group%20Bonus%20Rules.xlsx)  
- **Data Points:** Name,	Gender,	Department,	Salary,	Location,	Rating, Bonus rules  

---

## Methodology
- Datasets were imported into and cleaned in Microsoft PowerBI as detailed in [Data Cleaning](#data-cleaning).
- On the emp data, add a conditional column to sort the rating column. Assign number 6 to "Very Good", 5 to "Good", 4 to "Average", 3 to "Poor", 2 to "Very Poor" and 1 to "Not Rated".
- On the Bonus Rules Dataset, keep the Department column, and unpivot the other columns.
- On the data model, connect both tables on the Department column.
- Write several DAX measures to calculate each of the following:
  * Total Males
  * Total Females
  * Total Undisclosed Gender
  * Average Salary for Males
  * Average Salary for Females
  * Employee Bonus (by multiplying their Salaries with the department-rating multipliers in Bonus rules table)
  * Group Salaries into Bands: those earning less than $90k; $90k - $99,999; $100k - $109,999; and $110k - $120k
- On the PowerBI Desktop, group analysis into two pages: One showing gender distributions by location, department, etc.; and the other analysing staff salary

---

## Data Cleaning  
- Replaced null values in the Gender column with “Undisclosed Gender”
- Using filter in Power Query, removed records of staff that has left the company i.e., with no salary (43 records) and staff with NULL Departments (26 records).


---

## Analysis and Recommendations

### 1. Highest Sales Product Category

---

## Overall Recommendations
- Expand focus on technology products.  
- Address underperformance in specific regions.  
- Strengthen relationships with top customers.  
- Improve shipping efficiency based on order priority.  
- Investigate product returns and enhance quality control.  

---

## Conclusion
This analysis highlights key areas where KMS can improve operational efficiency, revenue generation, and customer satisfaction. By implementing the outlined recommendations, KMS Abuja can strengthen market presence and optimize business processes.
