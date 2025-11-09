Świetnie, dziękuję za te wyjaśnienia! Teraz mogę uzupełnić sekcję **"Data & File Structure"** w Twoim `README.md`.

Oto zaktualizowany plik `README.md` z dodaną sekcją:

---

# Credit Risk Assessment & Strategic Recommendations

## 📌 Project Overview

This project focuses on **advanced credit risk analysis** and **dashboard creation** for a consumer credit portfolio.
The main goal was to transform raw behavioral and demographic data into **actionable risk intelligence** by identifying, measuring, and visualizing key factors that lead to **Default** (failure to pay).

The core output is a set of **Strategic Recommendations** for optimizing collections processes and modifying lending policy based on quantified Default Rates.

---

## 📂 Data & File Structure

This repository contains all the necessary files to understand and replicate the project:

* **`UCI_Credit_Card.csv`**: The **raw, original dataset** used for the analysis, sourced from the UCI Machine Learning Repository.
* **`Banking.xlsx`**: An Excel file containing the **cleaned and pre-processed data**. This file is ready for direct use in analytical tools after initial data preparation.
* **`data_cleaning_script.sql`**: The SQL script used for **initial data cleaning, transformation, and feature engineering** steps applied to the raw dataset.
* **`Dashboard.pbix`**: The **Power BI Desktop file** containing the interactive analytical dashboard, including all data models, DAX measures, and visualizations.
* **`Credit_Risk_Report_Document_PL.docx`**: The **full analytical report in Polish**, detailing the methodology, findings, and strategic business recommendations.
* **`Credit_Risk_Report_Document_EN.docx`**: The **full analytical report in English**, detailing the methodology, findings, and strategic business recommendations.
* **`Page 1.png`, `Page 2.png`, `Page 3.png`**: Screenshots or exports of key dashboard pages for quick preview.
* **`README.md`**: This file, providing an overview of the project.

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
* **SQL** – For initial data cleaning and transformation processes.

---

## 📈 Key Outcomes & Strategic Recommendations

The project successfully transformed raw data into actionable risk mitigation strategies:

* **Collections Efficiency:** Recommended **prioritizing windykacji (collections)** solely on **"Risk" and "Critical"** segments to maximize recovery ROI, as they generate virtually all losses.
* **Proactive Intervention:** Recommended implementing **automatic alert systems** for clients whose $Util\_Ratio\_Avg$ exceeds $\mathbf{60\%}$ to intervene before Default.
* **Policy Modification:** Recommended introducing **stricter lending criteria** for segments identified with high proportional risk, such as *Young Adult* and clients with *Lower Education*.

---