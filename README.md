# Palmora-Group-HR-Analysis
This repository presents an analysis of Palmora Group HR Data.

---

## Dashboard
The analysis dashboard can be accessed [here]()  

![Gender Distr img](https://github.com/judeonuh/Palmora-Group-HR-Analysis/blob/main/Palmora%20Group%20Gender.png)  ![Salary Analysis img](https://github.com/judeonuh/Palmora-Group-HR-Analysis/blob/main/Palmora%20Group%20Salary%20Analysis.png)

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
### 1. Gender Distribution by Region
The Gender distribution in the organisation shows a strong male representation (**430** Males) compared to **406** Females. Furthermore, this was reflected by most regions with higher male dominance observed in Kaduna and Lagos, and an equal distribution in Abuja.

**Recommendations**:  
- Focus recruitment efforts on increasing female representation in all regions, especially in Kaduna.  
- Leverage Abuja as a model for promoting gender equality across other regions.  

---

### 2. Gender Distribution by Department
Gender distribution within departments is disproportionate, with the males dominating most departments, especially Legal, Support, and Accounting departments. However, there was a strong female representation in Services, Business Development, Human Resource, and Research and Development. The analysis also show gender equality in Engineering and Marketing departments.

**Recommendations**:  
- Improve female representation in most departments, especially in the **Accounting** department.  
- Engineering department shows good gender balance, however, the undisclosed gender data should be clarified.  

---

### 3. Performance Ratings by Gender
Females seem to outperform males across top rating categories (i.e. "Good" and "Very Good"). Majority of the staff (Males and Females) in the organisation are rated "Average".

**Recommendations**:  
- Strengthen female retention and promotion programs.  
- Ensure unbiased recognition and reward processes.
- Introduce programs, trainings, and resources to improve the general performance of all staff, especially the average ones.
- Identify the poor performing staff and provide support tailored to their needs.  

---
# START HERE
### 4. Salary Structure & Gender Pay Gap

#### Overall Avg. Salary  
- **Male**: £79.25K  
- **Female**: £74.51K  
- **Undisclosed**: £72.61K  

**Departments with Pay Gaps Favoring Males**:
- Business Development: £6K gap  
- Services: £6K gap  
- Accounting: £4K gap  

**Departments Where Females Earn More**:
- Marketing: £6K advantage  
- Training: £4K advantage  

#### By Region  
- Lagos: £1K gap  
- Kaduna: £1K gap  
- Abuja: £3K gap  

**Recommendations**:  
- Conduct salary audits for **Business Development**, **Services**, **Accounting**, and **Abuja region**.  
- Align pay with performance to close unjustified gaps.  

---

### 5. Regulatory Compliance Check ✅

New manufacturing regulation requires a minimum annual salary of **$90,000**.  

💡 **Exchange Rate Consideration**:  
£90,000 ≈ **$114,300**  

**Current Findings**:
- Large number of employees earn less than £90,000, suggesting non-compliance if they belong to Manufacturing.

**Action Required**:
- Identify employees under £90K within Manufacturing.  
- Adjust salaries to meet or exceed $90,000 equivalent.  
- Continuously monitor for currency fluctuations to maintain compliance.  

---

## 📂 Repository Contents

- Power BI PBIX File  
- Screenshots of HR Dashboard  
- README with insights and recommendations  

---

## 📢 Next Steps

✅ Develop additional dashboards to track:  
- Gender pay gap by job level  
- Regional salary trends  
- Regulatory compliance in real-time  

---

## 🛠 Technologies Used

- Power BI  
- DAX  
- Git & GitHub  

---


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
