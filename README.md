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




---

### 2. Key Descriptive Insights

- **Tenure Distribution:**  
  **75% of customers have tenure less than 55 months**, indicating a **short average service duration** and highlighting higher churn risk during early and mid-stage customer lifecycles.

- **Monthly Charges:**  
  - **Average Monthly Charges:** **$64.7**  
  - **Top 25% of customers pay more than $89.8 per month**, suggesting potential price sensitivity among high-paying customers.
  <img width="798" height="562" alt="kde_monthly_charges" src="https://github.com/user-attachments/assets/bd464b8d-c7b5-48d7-a559-ecafeec8ce74" />



- **Overall Churn Rate:**  
  The overall churn rate is approximately **26%**, indicating that **nearly one in four customers** discontinue services.

  <img width="498" height="405" alt="churn_distribution" src="https://github.com/user-attachments/assets/58a582ab-3c70-4de4-b77b-09443e08ad14" />

- **Gender-Based Churn:**  
  - **Male churn rate:** ~26%  
  - **Female churn rate:** ~26%  

  Churn rates are **almost identical across genders**, suggesting gender is **not a significant churn driver**.

  <img width="419" height="291" alt="gender vs churn" src="https://github.com/user-attachments/assets/99f6ab1c-aa88-4904-a4dd-c91646b32c05" />


- **Senior Citizen Impact:**  
  - **Senior citizens:** **41% churn rate**  
  - **Non-senior citizens:** **23% churn rate**  

  Senior citizens exhibit a **significantly higher churn rate**, indicating the need for targeted retention strategies for this segment.

  

- **Partner Status:**  
  - **Customers without a partner:** **32% churn rate**  
  - **Customers with a partner:** **19% churn rate**  

  Customers without partners show **higher churn tendencies**, possibly due to lower switching resistance.

  <img width="812" height="287" alt="senior and partner" src="https://github.com/user-attachments/assets/8b90f966-54a5-4899-b8e3-cac183e44226" />


- **Dependents:**  
  - **No dependents:** **31% churn rate**  
  - **With dependents:** **15% churn rate**  

  Customers with dependents are **more likely to stay**, suggesting stronger service dependency and loyalty.

  <img width="376" height="251" alt="Dependents" src="https://github.com/user-attachments/assets/f957ddd9-50bf-4d80-a7c6-aec1ecb8bc59" />

### 3. Service & Contract-Based Insights

- **Multiple Lines:**  
  Customers with multiple lines show a **slightly higher churn rate (~29%)**, which may indicate **higher plan complexity or increased cost sensitivity**.

  <img width="349" height="286" alt="multiple lines" src="https://github.com/user-attachments/assets/f4478e65-59bd-4f7e-919a-e82a179ff27d" />


- **Internet Service Type:**  
  - **Fiber Optic users:** Highest churn at approximately **42%**, possibly due to **premium pricing expectations**  
  - **DSL users:** More stable churn behavior  
  - **No internet service:** Very low churn at **7%**

  This indicates that **service type and pricing tiers** strongly influence churn behavior.

- **Online Security:**  
  Customers **without online security churn nearly 3× more** than those with security services, highlighting the importance of **value-added protection offerings**.

  <img width="727" height="287" alt="internet and online security" src="https://github.com/user-attachments/assets/5f1eb646-f49b-4d35-aba3-1a466bb67e76" />

- **Device Protection & Tech Support:**  
  - Customers with **device protection and tech support** show lower churn (~**22%**)  
  - Availability of tech support acts as a **strong retention factor**

  <img width="365" height="285" alt="device protection" src="https://github.com/user-attachments/assets/bcce5eaa-a6ae-493b-92e8-2f3c2d73f610" />

- **Streaming Services:**  
  Customers **not streaming movies** show a **slightly higher churn rate (34%)** compared to those who do (**30%**), suggesting that **service engagement may reduce churn**.

  <img width="366" height="285" alt="streaming movies" src="https://github.com/user-attachments/assets/a28dbc3b-7910-49bd-ba7b-146207acb1bb" />


- **Contract Type:**  
  - **Month-to-month contracts:** Highest churn at **43%**  
  - **One-year contracts:** Moderate churn at **~11%**  
  - **Two-year contracts:** Lowest churn at **~3%**

  Longer contract commitments clearly result in **higher customer retention**.


- **Billing Type:**  
  - **Paperless billing:** **34% churn**  
  - **Paper billing:** **16% churn**

  Traditional billing users tend to **stay longer**, indicating potential behavioral differences.

  <img width="707" height="281" alt="contract nd biling" src="https://github.com/user-attachments/assets/4e438fc6-9729-42eb-9396-ed620e2cb567" />


- **Payment Method:**  
  - **Electronic check users:** Highest churn at approximately **45%**  
  - **Automatic payments (bank transfer / credit card):** Lowest churn ranging between **15%–17%**

  Automatic payment methods are associated with **stronger customer retention**.


- **Tenure Group:**  
  **New customers (1–12 months)** are **8× more likely to churn** compared to **long-term customers (61–72 months)**, reinforcing the importance of **early-stage retention efforts**.

  <img width="729" height="294" alt="payment nd  tenure" src="https://github.com/user-attachments/assets/0f6de74d-df77-4e01-b064-94da51ee8eb8" />

