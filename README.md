# Telco Customer Churn – Exploratory Data Analysis (EDA)

## Overview

Customer churn is a **critical challenge in the telecom industry**, as retaining existing customers is significantly more cost-effective than acquiring new ones. High churn rates directly impact **revenue, profitability, and long-term customer lifetime value**.

This project focuses on performing an **in-depth Exploratory Data Analysis (EDA)** to understand customer churn behavior and identify the **key factors influencing customer attrition**. The analysis is conducted entirely using **Python**, leveraging data visualization and statistical techniques to uncover meaningful patterns and trends.

By analyzing customer demographics, service subscriptions, contract details, and billing information, this EDA aims to provide **actionable insights** that can help telecom companies improve **customer retention strategies** and reduce churn.

---

## Business Problem

Telecom companies often struggle to clearly understand:

- **Why customers churn**
- **Which customer segments are more likely to leave**
- **What service-related or behavioral factors drive churn decisions**

Without data-driven insights, churn prevention strategies tend to be **reactive rather than proactive**, resulting in inefficient retention efforts and increased customer acquisition costs.

The objective of this project is to address these challenges by using **exploratory data analysis** to examine relationships between customer attributes and churn outcomes. The insights derived from this analysis can support **informed decision-making**, enable **early churn detection**, and help businesses design **targeted, data-backed retention strategies**.

---

## 🎯 Objectives
- Understand the distribution of customer demographics and services.
- Identify factors contributing to customer churn.
- Analyze numerical relationships such as tenure, monthly charges, and total charges.
- Visualize key insights using Seaborn and Matplotlib.

---

## 🧰 Tools & Libraries Used
- **Language:** Python  
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn  
- **Environment:** Jupyter Notebook  

---
## Key Insights and Findings from the EDA

### 1. Data Overview

- **Dataset Shape:** 7043 rows × 21 columns  
- **Dataset:** Cleaned Telco Customer Churn dataset  
- **Target Variable:**  
  - Churn (Yes = 1, No = 0)

**Data Preparation Steps:**
- Converted the categorical **Churn** variable into binary format using `LabelEncoder`
- Created dummy variables for categorical features using `pd.get_dummies()`
- Ensured consistent data types and removed null values to maintain data quality

<img width="311" height="386" alt="info_image" src="https://github.com/user-attachments/assets/6b367a93-cf92-4547-a344-801955abe03b" />
<img width="498" height="405" alt="churn_distribution" src="https://github.com/user-attachments/assets/58a582ab-3c70-4de4-b77b-09443e08ad14" />



---

### 2. Key Descriptive Insights

- **Tenure Distribution:**  
  **75% of customers have tenure less than 55 months**, indicating a **short average service duration** and highlighting higher churn risk during early and mid-stage customer lifecycles.

  *(Visual to attach: Tenure distribution / KDE plot)*

- **Monthly Charges:**  
  - **Average Monthly Charges:** **$64.7**  
  - **Top 25% of customers pay more than $89.8 per month**, suggesting potential price sensitivity among high-paying customers.

  *(Visual to attach: Monthly Charges distribution / Boxplot)*

- **Overall Churn Rate:**  
  The overall churn rate is approximately **26%**, indicating that **nearly one in four customers** discontinue services.

  *(Visual to attach: Churn distribution bar chart)*

- **Gender-Based Churn:**  
  - **Male churn rate:** ~26%  
  - **Female churn rate:** ~26%  

  Churn rates are **almost identical across genders**, suggesting gender is **not a significant churn driver**.

  *(Visual to attach: Gender vs Churn bar chart)*

- **Senior Citizen Impact:**  
  - **Senior citizens:** **41% churn rate**  
  - **Non-senior citizens:** **23% churn rate**  

  Senior citizens exhibit a **significantly higher churn rate**, indicating the need for targeted retention strategies for this segment.

  *(Visual to attach: Senior Citizen vs Churn bar chart)*

- **Partner Status:**  
  - **Customers without a partner:** **32% churn rate**  
  - **Customers with a partner:** **19% churn rate**  

  Customers without partners show **higher churn tendencies**, possibly due to lower switching resistance.

  *(Visual to attach: Partner status vs Churn bar chart)*

- **Dependents:**  
  - **No dependents:** **31% churn rate**  
  - **With dependents:** **15% churn rate**  

  Customers with dependents are **more likely to stay**, suggesting stronger service dependency and loyalty.

  *(Visual to attach: Dependents vs Churn bar chart)*

