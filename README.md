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


### 4. Numerical Analysis Insights

#### KDE Plot – Monthly Charges

- The distribution of **Monthly Charges is bimodal**, with two major peaks:
  - Around **$20–25**, representing the **low-paying customer group**
  - Around **$70–90**, representing the **high-paying customer group**

- **Mean Monthly Charges:** **$64.8**  
- **Median Monthly Charges:** **$70.3**, indicating a **slight right skew** in the distribution

- **75% of customers have Monthly Charges below $90.8**, showing that the majority fall under mid-range pricing plans.

- A small segment of customers pays **up to $118.8**, likely associated with **premium plans or multiple subscribed services**.

- This distribution helps clearly identify **low-, mid-, and high-spending customer segments**.

<img width="798" height="562" alt="kde_monthly_charges" src="https://github.com/user-attachments/assets/d849e20e-a1e0-46df-9108-1f5f3d7f505f" />

---

#### Scatter Plot – Monthly Charges vs Total Charges

- There is a **strong positive correlation** between **Monthly Charges** and **Total Charges**, indicating that customers paying more monthly generally accumulate higher total revenue.

- The **triangular pattern** observed in the scatter plot highlights that **Total Charges are dependent on customer tenure**:
  - Newer customers with high monthly charges still have lower total charges due to shorter service duration.

- This confirms that **revenue grows with customer tenure**, reinforcing the importance of long-term retention.

<img width="590" height="478" alt="total charges vs monthly charges" src="https://github.com/user-attachments/assets/b5c5a267-ec1a-4f4a-80de-a40eda1c9bf3" />


---

#### KDE Plot – Monthly Charges by Churn

- **Churn probability increases with higher Monthly Charges**, indicating strong **price sensitivity** among customers.

- **Non-churned customers** are more densely clustered around **lower monthly charge ranges**, suggesting better retention at affordable pricing levels.

- **Business Note:**  
  High-paying customers may benefit from **targeted loyalty offers or pricing flexibility** to reduce churn risk.

<img width="578" height="464" alt="monthly charges by churn" src="https://github.com/user-attachments/assets/0a422326-bc64-4785-b526-34945fb21620" />

#### KDE Plot – Total Charges by Churn

- Customers with **low Total Charges (0–2000)** exhibit the **highest churn rates**, indicating that churn is most prevalent during the **early stages of the customer lifecycle**.

- Customers with **higher Total Charges** are more likely to be **long-tenure customers**, showing **lower churn probability**.

- This emphasizes the importance of **early customer engagement and retention efforts** to prevent churn before long-term value is realized.

  <img width="584" height="466" alt="total charges by churn" src="https://github.com/user-attachments/assets/bde76496-5a01-4482-b89e-465c4b414c38" />


---

#### Correlation Bar Plot

- **Top Positive Correlation with Churn:**
  - **Month-to-month contracts**
  - **High Monthly Charges**
  - **Electronic check payment method**

  These factors are strongly associated with **increased churn risk**.

- **Top Negative Correlation with Churn:**
  - **Longer tenure**
  - **Tech support availability**
  - **Online security services**
  - **Two-year contracts**

  These features are associated with **lower churn rates** and improved retention.

- Overall, the correlation analysis suggests that **service engagement** and **longer-term commitments** play a crucial role in **reducing customer churn**.

  <img width="1072" height="539" alt="correlation" src="https://github.com/user-attachments/assets/267a1510-59f9-4c19-917b-91c8e4d1cf00" />

## Key Churn Loopholes Identified

Based on the exploratory and numerical analysis, the following **critical churn loopholes** were identified across customer lifecycle, pricing, services, and engagement:

- High churn concentration among **new customers (1–12 months tenure)** due to weak early engagement.
- Excessive churn from **month-to-month contract users**, indicating low commitment.
- **Senior citizens** exhibit significantly higher churn, suggesting unmet service or usability needs.
- Customers using **electronic check payment methods** churn the most due to payment friction.
- **High monthly charges** increase churn risk, especially among premium customers.
- Customers without **online security and tech support services** churn nearly **3× more**.
- Low engagement customers (no streaming or add-on services) show **higher churn tendencies**.
- Customers without **partners or dependents** churn more, indicating lower switching barriers.
- Early-stage customers with **low total charges (0–2000)** churn before value realization.
- Lack of incentives to move customers toward **long-term contracts** increases churn exposure.

## Business Recommendations

Based on the exploratory and numerical analysis of customer churn, the following **data-driven recommendations** are proposed to reduce churn and improve long-term customer retention.

---

### 1. Strengthen Early Customer Retention (First 6–12 Months)

Customers in the **early tenure group (1–12 months)** are **8× more likely to churn** than long-term customers, and customers with **low total charges (0–2000)** show the **highest churn rates**.

**Recommended Actions:**
- Improve onboarding experience with guided setup and early engagement
- Provide proactive customer support during the first year
- Introduce welcome offers or early loyalty rewards

**Business Impact:**  
Reducing early churn increases customer lifetime value before revenue maturity.

*(Insight reference: Tenure Group, Total Charges by Churn)*

---

### 2. Encourage Long-Term Contracts to Reduce Churn

Customers on **month-to-month contracts** have the **highest churn rate (43%)**, while **two-year contract customers churn the least (3%)**.

**Recommended Actions:**
- Offer discounts or benefits for switching from month-to-month to annual or two-year plans
- Promote contract upgrades at renewal touchpoints
- Bundle long-term plans with value-added services

**Business Impact:**  
Longer commitments directly translate into **higher retention and predictable revenue**.

*(Insight reference: Contract Type vs Churn)*

---

### 3. Promote Automatic Payment Methods

Customers using **electronic checks exhibit the highest churn (~45%)**, whereas customers using **automatic bank transfer or credit card payments churn significantly less (15–17%)**.

**Recommended Actions:**
- Provide incentives for switching to auto-pay options
- Highlight convenience and reliability of automatic payments
- Enable seamless auto-pay setup during onboarding

**Business Impact:**  
Automatic payments reduce friction and improve customer stickiness.

*(Insight reference: Payment Method vs Churn)*

---

### 4. Bundle Support & Security Services as Retention Drivers

Customers **without online security churn nearly 3× more**, while customers with **tech support and device protection churn less (~22%)**.

**Recommended Actions:**
- Bundle online security and tech support into popular plans
- Offer trial periods for support services to high-risk customers
- Position support services as value-enhancing, not optional add-ons

**Business Impact:**  
Higher service engagement leads to **lower churn and stronger customer dependency**.

*(Insight reference: Online Security, Tech Support vs Churn)*

---

### 5. Address Price Sensitivity Among High-Charge Customers

Customers with **higher monthly charges ($70–90+)** show **increased churn probability**, and churn probability rises with increasing monthly charges.

**Recommended Actions:**
- Introduce loyalty discounts for high-paying customers
- Offer plan customization or flexible pricing options
- Proactively engage premium customers before dissatisfaction occurs

**Business Impact:**  
Protects high-revenue customers and prevents churn driven by pricing dissatisfaction.

*(Insight reference: Monthly Charges KDE, Monthly Charges by Churn)*

---

### 6. Launch Targeted Retention Campaigns for At-Risk Segments

Certain demographic segments show **significantly higher churn**:
- **Senior citizens:** 41% churn
- **Customers without partners:** 32% churn
- **Customers without dependents:** 31% churn

**Recommended Actions:**
- Design personalized communication and retention offers
- Provide simplified plans or dedicated support for senior citizens
- Use targeted campaigns instead of generic retention strategies

**Business Impact:**  
Segment-based interventions improve retention efficiency and customer satisfaction.

*(Insight reference: Demographics vs Churn)*

---

### 7. Increase Engagement Through Value-Added Services

Customers **not using streaming services churn more (34%)** compared to those who do (**30%**), indicating engagement reduces churn.

**Recommended Actions:**
- Promote bundled entertainment or engagement-based services
- Offer limited-time access to value-added features
- Encourage deeper service usage to increase switching costs

**Business Impact:**  
Higher engagement leads to **lower churn and stronger customer relationships**.

*(Insight reference: Streaming Services vs Churn)*

---

