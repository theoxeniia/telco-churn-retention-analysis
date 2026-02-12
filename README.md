# Telco Customer Churn & Retention Analysis

## 📌 Project Overview
This project provides a comprehensive analysis of customer attrition for a telecommunications company. By combining **Python (EDA & Visualization)** and **Excel (Statistical Testing & Financial Modeling)**, I identified key churn drivers and developed a data-driven retention strategy.

**Dataset:** [Telco Customer Churn (Hugging Face)](https://huggingface.co/datasets/aai510-group1/telco-customer-churn)

---

## 🛠️ Phase 1: Python Exploratory Data Analysis (EDA)
In this phase, I performed data cleaning and uncovered the behavioral patterns of churning customers.

### 1. Data Preprocessing
*   Handled missing values for `Churn Category`, `Churn Reason`, and `Internet Type`.
*   Verified data integrity (no duplicates found).
*   **Key Findings:**
    *   **Average Churn Rate:** 27%
    *   **Revenue Lost:** $2,181,556.11 (17% of total revenue).

### 2. Visual Insights & Drivers of Churn
I created a series of visualizations to identify high-risk segments (stored in the `/images` folder):

*   **Demographics:** High churn is observed in the 20-30 and 45-55 age brackets. Single customers without dependents are 8x more likely to churn than those with families.
    *   [View: Age Distribution](images/Age.png) | [View: Family Impact](images/Family.png)
*   **Contract & Payment:** Customers on **Month-to-Month** contracts and those using **Mailed Checks** represent the highest risk (>40% churn).
    *   [View: Contract Type](images/Contract.png) | [View: Payment Method](images/Payment_Method.png)
*   **Service Quality:** Fiber Optic users have a 40% churn rate, suggesting potential technical or pricing dissatisfaction.
    *   [View: Internet Type](images/Internet.png)
*   **Customer Experience:** There is a 100% correlation between low satisfaction scores (1-2) and churn.
    *   [View: Satisfaction Score](images/Satisfaction.png)
*   **Ecosystem Lock-in:** Churn drops to near zero for customers with 4+ additional services.
    *   [View: Services Count](images/Additional_serv.png)

---

## 📊 Phase 2: Excel Statistical & Financial Analysis
I used Excel to validate marketing hypotheses and calculate the ROI of potential retention programs.

**Files:**
*   [Download Excel Workbook (Calculations & Pivots)](reports/analysis_cleaned_churn_data.xlsx)
*   [View Full PDF Report](reports/Customer_Churn_&_Retention_Analysis_report.pdf)

### 1. A/B Testing (Statistical Significance)
I conducted a **t-Test** to compare the performance of two marketing offers based on Monthly Charges (ARPU):
*   **Offer A ARPU:** $77.53 vs. **Offer B ARPU:** $70.30.
*   **Result:** P-value = 0.0011. Offer A is statistically superior for high-value segments.

### 2. Financial Modeling (What-If Analysis)
I simulated a retention program offering a $10 incentive to high-risk customers:
*   **Target:** 5% churn reduction.
*   **Projected Net ROI:** **$246,606.06** saved in Customer Lifetime Value (CLTV).

---

## 💡 Strategic Recommendations

1.  **Contract Migration:** Incentivize "Month-to-Month" users to switch to Annual plans after 6 months of tenure.
2.  **Optimize Marketing:** Phase out "Offer E" (50% failure rate) and scale "Offer A" across all digital channels.
3.  **Technical Audit:** Investigate Fiber Optic service stability in high-churn regions (e.g., San Diego, Los Angeles).
4.  **Proactive Retention:** Deploy automated $10 retention triggers for customers with a **Churn Score > 85** or a **Satisfaction Score < 3**.

---
**Author:** Kseniia Serova
**Tools:** Python (Pandas, Seaborn, Matplotlib), Excel (Pivot Tables, t-Test, What-If Analysis).
