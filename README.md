# 📊 Customer Churn Analysis

## 📌 Project Overview

Customer churn is an important business problem for telecom companies because losing existing customers can directly affect revenue and growth.

This project analyzes telecom customer data to understand customer churn behavior, identify high-risk customer segments, and generate actionable business insights using Python and Power BI.

---

## 🎯 Project Objectives

- Analyze overall customer churn.
- Identify factors associated with customer churn.
- Compare churn across different contract types.
- Analyze churn based on internet and additional services.
- Study payment methods and customer demographics.
- Analyze customer tenure and monthly charges.
- Identify high-risk customer segments.
- Build an interactive Power BI dashboard.
- Provide business recommendations to reduce customer churn.

---

## 🛠️ Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook
- Power BI
- DAX
- CSV

---

## 📂 Dataset

The dataset contains telecom customer information including:

- Customer ID
- Gender
- Senior Citizen
- Partner
- Dependents
- Tenure
- Phone Service
- Multiple Lines
- Internet Service
- Online Security
- Online Backup
- Device Protection
- Tech Support
- Streaming TV
- Streaming Movies
- Contract
- Paperless Billing
- Payment Method
- Monthly Charges
- Total Charges
- Churn

---

## 🧹 Data Cleaning & Preparation

The following data preparation steps were performed using Python and Pandas:

- Loaded the dataset using Pandas.
- Checked the dataset structure and dimensions.
- Checked column names and data types.
- Checked missing values.
- Checked duplicate records.
- Converted `TotalCharges` from text to numeric format.
- Converted invalid/blank `TotalCharges` values into missing values.
- Removed records with missing `TotalCharges`.
- Created `TenureGroup` for customer segmentation.

---

## 📊 Exploratory Data Analysis

The project analyzes customer churn across multiple dimensions.

### Customer Churn Distribution

The overall churn distribution was analyzed to understand the percentage of customers who stayed and those who left the company.

### Gender

Customer churn was compared between male and female customers.

### Senior Citizen

Churn was analyzed based on senior citizen status.

### Contract Type

Churn was analyzed across:

- Month-to-month
- One year
- Two year

Month-to-month customers showed significantly higher churn compared with customers having one-year and two-year contracts.

### Tenure

Customer tenure was analyzed using different groups:

- 0-12 Months
- 13-24 Months
- 25-48 Months
- 49-72 Months

Customers with shorter tenure showed higher churn.

### Internet Service

Churn was compared across:

- DSL
- Fiber optic
- No internet service

Fiber optic customers showed relatively high churn.

### Payment Method

Churn was analyzed across different payment methods.

Electronic check customers showed a high churn rate.

### Tech Support

Customers without Tech Support showed higher churn compared with customers having Tech Support.

### Online Security

Customers without Online Security showed higher churn compared with customers having Online Security.

### Online Backup

Churn was analyzed based on Online Backup services.

### Device Protection

Customer churn was analyzed based on Device Protection services.

### Paperless Billing

Paperless billing customers showed higher churn compared with non-paperless billing customers.

### Monthly Charges

Monthly charges were compared between churned and non-churned customers.

Churned customers had higher average monthly charges.

### Total Charges

Total charges were also analyzed based on customer churn.

### Partner and Dependents

Customer churn was analyzed based on Partner and Dependents status.

---

## 📈 Key Insights

- Overall customer churn rate was **26.58%**.
- Month-to-month contract customers had the highest churn rate at **42.71%**.
- Two-year contract customers had a very low churn rate of approximately **2.85%**.
- Customers with **0-12 months tenure** had the highest churn rate at **47.68%**.
- Fiber optic customers showed relatively high churn.
- Electronic check users showed a high churn rate.
- Customers without Tech Support showed higher churn.
- Customers without Online Security showed higher churn.
- Paperless billing customers had higher churn compared with non-paperless billing customers.
- Churned customers had higher average monthly charges of approximately **$74.44**.
- Non-churned customers had average monthly charges of approximately **$61.31**.

---

## 🔎 High-Risk Customer Segment

One of the most important segments identified in the analysis was:

**Month-to-month + Fiber Optic customers**

- Total Customers: **2,128**
- Churned Customers: **1,162**
- Churn Rate: **54.61%**

This segment represents a high-risk group and can be targeted with personalized customer retention strategies.

### Payment Risk in High-Risk Segment

Among the high-risk Month-to-month + Fiber Optic segment:

- Electronic Check showed approximately **60.37%** churn.
- Mailed Check showed approximately **50.75%** churn.
- Bank Transfer showed approximately **45.57%** churn.
- Credit Card showed approximately **41.64%** churn.

---

## 📊 Top Customer Churn Factors

The analysis identified several important churn-related factors:

| Factor | Churn Rate |
|---|---:|
| Electronic Check | 45.29% |
| Month-to-month Contract | 42.71% |
| Fiber Optic Internet | 41.89% |
| No Online Security | 41.77% |
| No Tech Support | 41.64% |
| Paperless Billing | 33.57% |

These factors can help the company identify customers who may be at higher risk of churn.

---

## 📊 Power BI Dashboard

An interactive Power BI dashboard was created to present the customer churn analysis.

### Page 1 — Customer Churn Analysis Dashboard

The dashboard includes:

- Total Customers
- Churn Rate
- Average Monthly Charges
- Average Tenure
- Churn Rate by Contract
- Churn Rate by Payment Method
- Churn Rate by Internet Service
- Churn Rate by Gender

### Page 2 — Customer Churn – Service Analysis

The dashboard includes churn analysis for:

- Tech Support
- Online Security
- Online Backup
- Device Protection
- Streaming TV
- Streaming Movies
- Phone Service

### Page 3 — Customer Churn – Customer Demographics & Services

The dashboard includes:

- Paperless Billing
- Phone Service
- Partner
- Dependents
- Senior Citizen

---

## 📐 DAX Measures

### Total Customers

```DAX
Total Customers =
DISTINCTCOUNT('Customer Churn'[customerID])
```

### Churned Customers

```DAX
Churned Customers =
CALCULATE(
    COUNTROWS('Customer Churn'),
    'Customer Churn'[Churn] = "Yes"
)
```

### Churn Rate %

```DAX
Churn Rate % =
DIVIDE(
    [Churned Customers],
    [Total Customers],
    0
)
```

### Average Monthly Charges

```DAX
Average Monthly Charges =
AVERAGE('Customer Churn'[MonthlyCharges])
```

### Average Tenure

```DAX
Average Tenure =
AVERAGE('Customer Churn'[tenure])
```

---

## 💡 Business Recommendations

Based on the analysis, the following recommendations can help reduce customer churn:

1. Encourage month-to-month customers to switch to one-year or two-year contracts through suitable offers and discounts.

2. Provide special retention offers for new customers, especially those with 0-12 months of tenure.

3. Target high-risk month-to-month and Fiber Optic customers with personalized retention campaigns.

4. Review customers using Electronic Check and encourage more convenient automatic payment options.

5. Promote Tech Support and Online Security services to customers who do not currently use them.

6. Review pricing plans for customers with high monthly charges.

7. Use customer data to identify high-risk customers early and take proactive retention actions.

---

## 🚀 Project Outcome

This project demonstrates how raw customer data can be transformed into meaningful business insights using Python and Power BI.

The analysis helped identify:

- Overall customer churn rate.
- Customer segments with higher churn.
- Contract types associated with higher churn.
- Services associated with higher churn.
- Payment methods associated with higher churn.
- Customer tenure and monthly charge patterns.
- High-risk customer segments.
- Potential strategies to improve customer retention.

---

## 📁 Project Structure

```text
Customer-Churn-Analysis/
│
├── Customer_Churn_Analysis.ipynb
├── customer_churn_final.csv
├── Customer_Churn_Dashboard.pbix
├── README.md
│
└── images/
    ├── dashboard_page1.png
    ├── dashboard_page2.png
    └── dashboard_page3.png
```

---

## 👨‍💻 Author

**Rohit Gayke**

Aspiring Data Analyst

### Skills

Python | SQL | Pandas | NumPy | Matplotlib | Seaborn | Power BI | DAX
