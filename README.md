# Palmora-Group-HR-Analysis
This repository presents an analysis of Palmora Group HR Data.

---

## Analysis Report
The interactive report for this analysis can be accessed [here](https://app.powerbi.com/view?r=eyJrIjoiZTAzOTU3MWUtOTIzNS00ZjhiLTk0ODEtMmVhMzdmMWUxYTk1IiwidCI6IjJjYzg3ZmM4LTY5NDQtNDUzMC1hNThlLTFjMDY0MTE4NTYzMCJ9). The report has been grouped into two pages: Gender Distribution and Salary Analysis. All pages contain slicers to allow for interactive filtering of reports by Department or Region.  

---

## Problem Statement
The Palmoria Group is a manufacturing company based in Nigeria with Mr Ayodeji Chukwuma as the CEO. The Group is embroiled in issues bordering on gender inequality in its 3 regions. Unfortunately, the media recently published the news with the headline “Palmoria, the Manufacturing Patriarchy”. This doesn’t look good for the owners of the business, based on their ambition to scale the business to other regions and even overseas. Cases like this can only spiral downwards, revealing other issues like the gender pay gap, amongst other possible issues.  

---

## Aim  
This analysis provides a comprehensive evaluation of gender representation, performance, salary structure, and regulatory compliance within Palmora Group. The aim is to identify areas of gender disparity, uncover underlying trends, and propose data-driven, actionable recommendations to foster inclusivity, improve employee performance, and ensure regulatory compliance.

---

## 📁 Table of Contents
- [Problem Statement](#problem-statement)
- [Aim](#aim)
- [Data Overview](#data-overview)  
- [Methodology](#methodology)
- [Technologies Used](#technologies-used)
- [Data Cleaning](#data-cleaning)
- [Analysis and Recommendations](#analysis-and-recommendations)
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

## Technologies Used
- Power BI  
- DAX  
- Git & GitHub  

---

## Data Cleaning  
- Replaced null values in the Gender column with “Undisclosed Gender”
- Using filter in Power Query, removed records of staff that has left the company i.e., with no salary (43 records) and staff with NULL Departments (26 records).

---

## Analysis and Recommendations
### 1. Gender Distribution by Region
The gender composition across Palmora Group reveals a modest gender imbalance. Out of the total workforce, 430 are males and 406 are females, indicating approximately 51% male dominance. Regionally:
* Kaduna and Lagos exhibit noticeable male dominance.
* Abuja displays a commendable gender balance, serving as a positive outlier.

Such imbalances may limit diversity-driven innovation and may indicate barriers to female recruitment or retention in specific regions.

**Recommendations:**
* Launch targeted female recruitment campaigns, prioritising Kaduna and Lagos.
* Conduct exit interviews and employee feedback sessions to understand regional gender-specific challenges.
* Utilise Abuja as a benchmark for gender inclusivity practices to be replicated across other locations.

---

### 2. Gender Distribution by Department
Gender distribution within departments is disproportionate, with the males dominating most departments, especially Legal, Support, and Accounting departments. However, there was a strong female representation in Services, Business Development, Human Resource, and Research and Development. The analysis also show near gender parity in Engineering and Marketing departments. However, a portion of the workforce still has an undisclosed gender, potentially masking deeper gaps.

**Recommendations**:  
- Improve female representation in most departments, especially in the **Accounting** department.  
- Engineering department shows good gender balance, however, the undisclosed gender data should be clarified. Review and improve data collection processes to minimise undisclosed gender records.
- Recognise and reward departments like Marketing and Engineering for maintaining gender balance, reinforcing these as internal best practices.

---

### 3. Performance Ratings by Gender
Analysis of performance ratings uncovers encouraging patterns: A higher proportion of Females are represented within the top-performing groups ("Good" and "Very Good" ratings). However, the majority of both Male and Female employees are clustered within the "Average" rating band, suggesting organisational performance stagnation.

**Recommendations**:  
- Establish mentorship and leadership pathways to retain and promote high-performing females.
- Strengthen performance review processes to ensure objectivity and eliminate potential unconscious bias.
- Introduce targeted training and development programs to uplift average performers and support underperforming staff with tailored improvement plans.
- Identify the poor performing staff and provide support tailored to their needs. 

---
### 4. Salary Structure and Gender Pay Gap
A notable, albeit modest, gender pay gap persists: Average salary for Males ($74.5K) is slightly higher than that of Females ($72.6K). This was distilled across all regions, showing that Males had higher pay advantage than Females in these regions. Suprisingly, staff (Male and Female) in Lagos had the highest average salary, even though this region had the least number of staff compared to the other regions. This disparity may be a reflection of the high cost of living in Lagos.  

Department-wise, Males had higher average salaries in 9 out of the 12 departments, except in **Marketing, Training and Engineering** departments where Females had slightly higher pay than their Male counterparts. 

**Recommendations**:  
- Commission an independent, data-driven salary equity audit across regions and departments.
- Design structured, transparent pay frameworks linked to objective performance metrics.
- Address unjustified gender-based pay gaps while considering regional economic factors, such as Lagos' higher living costs. 

---

### 5. Regulatory Compliance Check
Given the new regulation that mandates all manufacturing companies to pay their staff a minimum annual salary of **$90,000**, the analysis reveals that Palmora is non-compliant. A total of 599 staff (213 in Abuja, 232 in Kaduna, and 154 in Lagos) earn less than $90k.

**Recommendation**:
- Immediately identify affected employees across all regions.
- Develop a phased salary adjustment plan to achieve full compliance within stipulated timelines.
- Engage with legal and regulatory experts to ensure all future compensation structures align with evolving policy requirements.  

---

## Overall Recommendations
- **Diversity & Inclusion:** Implement a comprehensive gender diversity and inclusion strategy targeting both recruitment and retention, especially in underrepresented regions and departments.
- **Data Quality:** Improve employee data collection, specifically for gender disclosure, to enhance the accuracy of diversity reporting.
- **Performance Development:** Invest in performance improvement initiatives to reduce the concentration of "Average" performers, with particular attention to supporting underperformers.
- **Pay Equity:** Conduct regular salary audits, link pay to transparent performance metrics, and actively work to close unjustified gender pay gaps.
- **Regulatory Compliance:** Establish a compliance task force to monitor salary structures and ensure alignment with all current and future industry regulations.
---

## Conclusion
This analysis underscores both progress and challenges within Palmora Group's workforce structure. While the organisation demonstrates pockets of gender balance and female excellence in performance, persistent gender pay gaps and departmental disparities remain. Proactive, data-driven actions, combined with a commitment to equity and inclusivity, will position Palmora Group as a model employer, fostering a diverse, high-performing, and compliant workforce.
