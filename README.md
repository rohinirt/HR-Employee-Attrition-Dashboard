# HR Employee Attrition Dashboard – Google Looker Studio

Dashboard Link: https://lookerstudio.google.com/reporting/f193c501-d56b-41e1-8c03-4a6c7df4ed82/page/p_gc4ab9skvd


## Project Objective
The objective of this project was to **analyze employee attrition trends** within a company's workforce and build an **interactive dashboard** to help HR teams identify patterns and insights.  
The dashboard provides **data-driven insights** to support decision-making in areas like **employee retention, workforce planning, and engagement strategies**.

---

## Tech Stack & Tools
- **Google Looker Studio** –  Visualization  
- **Google Sheets** – Data source for cleaning and transformation
- **Figma** – Background Design    

---

## Dataset Overview
The dataset contains employee information, including **demographics, job roles, compensation, performance, and experience details**.  

| Column | Description |
|---------|-------------|
| `Attrition` | Whether the employee has left the organization (`Yes`/`No`) |
| `Gender` | Gender of the employee |
| `Department` | Department in which the employee works |
| `JobRole` | Specific job role of the employee |
| `JobLevel` | Level of the employee in the organization hierarchy |
| `MonthlyIncome` | Monthly salary of the employee |
| `PercentSalaryHike` | Percentage salary hike received |
| `TotalWorkingYears` | Total years of professional experience |
| `YearsAtCompany` | Tenure in the current company |
| `YearsInCurrentRole` | Experience in the current role |
| `YearsWithCurrManager` | Years reporting to the current manager |
| `YearsSinceLastPromotion` | Time since last promotion |
| `TrainingTimesLastYear` | Training frequency in the last year |
| `DistanceFromHome` | Distance between home and workplace |
| `EnvironmentSatisfaction`, `JobSatisfaction`, `RelationshipSatisfaction`, `WorkLifeBalance` | Survey ratings (1–4) indicating employee satisfaction levels |

---

## Key Features of the Dashboard
- **📈 Executive KPIs**
  - Attrition Rate  
  - Total Employees  
  - Active Employees  
  - Average Monthly Income  
  - Average Years at Company  

- **Interactive Filters**
  - Department  
  - Job Role  
  - Gender  
  - Survey Selector (for switching between different survey metrics dynamically)


##  Calculated Fields
- **Attrition Rate**:
  ```sql
  COUNT(CASE WHEN Attrition = 'Yes' THEN 1 END) / COUNT(EmployeeID)
  ```
- **Total Attrition Rate**:
  ```sql
  COUNT(CASE WHEN Attrition = 'Yes' THEN 1 END)  
  ```
- **Visual Insights**
  - **Demographics:** Attrition by age group, gender, and education  
  - **Job Info:** Department-wise and role-wise attrition  
  - **Benefits:** Attrition trends based on salary, hikes, and training  
  - **Experience:** Line chart and bracketed analysis for tenure insights  
  - **Work Environment:** Attrition by overtime and survey satisfaction ratings  
  - **Travel:** Attrition patterns by business travel and distance from home  

---

## Insights Derived
- **High Early Attrition:** Employees with **0–1 years** of tenure show the highest attrition rate.  
- **Overtime Impact:** Employees working overtime are **3x more likely** to leave.  
- **Travel Stress:** Frequent business travelers show **significantly higher attrition**.  
- **Role-Specific Trends:** Roles like **Sales Executives and Laboratory Technicians** have higher attrition percentages compared to senior-level roles.  
- **Survey Ratings:** Low satisfaction scores correlate strongly with higher attrition rates.
