# Credit Risk Assessment & Strategic Recommendations

## 📌 Project Overview

This project focuses on **advanced credit risk analysis** and **dashboard creation** for a consumer credit portfolio.
The main goal was to transform raw behavioral and demographic data into **actionable risk intelligence** by identifying, measuring, and visualizing key factors that lead to **Default** (failure to pay).

The core output is a set of **Strategic Recommendations** for optimizing collections processes and modifying lending policy based on quantified Default Rates.

---

## 📂 Data Source

* **Source Data:** Real-world anonymized credit client data, including demographics, credit limit, billing statements, and detailed payment history.
* **Data Fields:** Key fields analyzed include `LIMIT_BAL`, `AGE`, `EDUCATION`, and a set of six historical payment status columns (`PAY_X`).

---

## 🛠️ Data Preparation & Risk Engineering

This was the most crucial phase, focusing on transforming raw history columns into usable risk metrics. The following steps were taken:

* **Risk Definition (Target Variable):** I redefined the target variable, setting the **TRUE\_DEFAULT\_STATUS** to $1$ if a client reported an **arrear of 2 or more months** ($PAY\_X \ge 2$). This is the basis for all Default Rate calculations.
* **Feature Engineering:** Created aggregated, predictive metrics:
    * **$MAX\_LATE\_DELAY$**: Maximum severity of arrears observed.
    * **$UTIL\_RATIO\_AVG$**: Average credit utilization (key behavioral stress indicator).
    * **$PAYMENT\_SEVERITY$**: Categorical risk grouping (e.g., *Perfect*, *Warning*, *Risk*, *Critical*).
* **Data Standardization:** Cleaned and standardized demographic and limit data into categorical groups (e.g., $AGE\_GROUP$, $LIMIT\_BAL\_GROUP$).

---

## 🔎 Key Analyses & Risk Insights

The following analyses were performed to answer key business questions regarding client behavior and risk exposure:

* **Threshold Analysis:** Quantified the increase in Default Rate as a function of **Credit Utilization ($Util\_Ratio\_Avg$)**, pinpointing the critical threshold at **$\mathbf{60\%}$**.
* **Risk Matrix Construction (Heatmap):** Measured and visualized **Default Rate (%)** across high-risk segments (e.g., *Severity* vs. *Limit Group*).
* **Behavioral Deep Dive:** Determined that **$\approx 100\%$ of the loss volume** originates from the **"Risk" and "Critical"** behavioral categories.
* **Risk Profile Identification:** Identified key segments with **disproportionately high Default Rates** (e.g., *Young Adult*, clients with *Lower Education*).
* **Intervention Point Analysis:** Determined that the **critical point of no return** for collections occurs after **2-3 months of arrears**.

---

## 📊 Dashboard in Power BI

An interactive dashboard was built in **Power BI** to visualize the strategic risk matrix and behavioral trends. The dashboard allows users to:

* Analyze **Default Rate** across all demographic and behavioral segments.
* Identify segments requiring **immediate collections priority** (red zones on the Risk Matrix).
* Monitor **early warning indicators** (e.g., high $Util\_Ratio\_Avg$).

---

## 🚀 Tools & Technologies

* **Power BI** – Data modeling, advanced DAX (for Default Rate calculations and risk metrics), and dashboard creation.
* **DAX** – Crucial for creating key performance metrics and complex conditional risk classifications.
* **Excel/Power Query** – Data cleaning, feature engineering, and standardization of categorical variables.

---

## 📈 Key Outcomes & Strategic Recommendations

The project successfully transformed raw data into actionable risk mitigation strategies:

* **Collections Efficiency:** Recommended **prioritizing windykacji (collections)** solely on **"Risk" and "Critical"** segments to maximize recovery ROI, as they generate virtually all losses.
* **Proactive Intervention:** Recommended implementing **automatic alert systems** for clients whose $Util\_Ratio\_Avg$ exceeds $\mathbf{60\%}$ to intervene before Default.
* **Policy Modification:** Recommended introducing **stricter lending criteria** for segments identified with high proportional risk, such as *Young Adult* and clients with *Lower Education*.

---
<img width="1278" height="717" alt="Page 1" src="https://github.com/user-attachments/assets/5782f86f-805e-4ee4-bc36-4685c84ae663" />

<img width="1280" height="716" alt="Page 2" src="https://github.com/user-attachments/assets/0cc98bae-a35d-4ae1-bb81-b188d96fb982" />

<img width="1276" height="720" alt="Page 3" src="https://github.com/user-attachments/assets/3457a75b-b86b-4e0a-bbab-6f69ff610798" />

