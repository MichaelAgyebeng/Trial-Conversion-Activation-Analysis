# 🚀 Trial-Conversion-Activation-Analysis

An end-to-end analytics project designed to identify behavioral drivers of product conversion, define trial success, and build scalable data models for tracking user activation.

---

## 📌 Overview
This project analyzes behavioral event data from organizations that started a product trial between January and March. By combining **Python (analytics)** and **SQL (data modeling)**, we transform raw event logs into actionable insights that empower product and growth teams to optimize onboarding and increase conversion rates.

---

## 🎯 Objectives
* **Clean & Explore:** Process raw behavioral event data.
* **Correlate:** Identify activities that strongly drive conversion.
* **Define:** Establish data-backed trial success criteria (goals).
* **Model:** Build scalable SQL marts for Trial Goals and Activation classification.
* **Deliver:** Provide product metrics and insights to support data-driven decision-making.

---

## 🧱 Dataset Description
The dataset contains event-level behavioral logs:

| Column | Description |
| :--- | :--- |
| `organization_id` | Unique organization identifier |
| `activity_name` | Name of the product activity performed |
| `timestamp` | Event timestamp |
| `converted` | Boolean flag (Target variable) |
| `converted_at` | Conversion timestamp |
| `trial_start` | Trial start date |
| `trial_end` | Trial end date |

---

## ⚙️ Tech Stack
* **Python:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
* **SQL:** Data modeling & warehouse marts
* **Environment:** Jupyter Notebook (Analysis & Visualization)

---

## 🔍 Key Processes & Analysis

### 🧹 Data Cleaning
* Standardized date/time formats.
* Removed duplicates and noise.
* Filtered events to the valid trial window.
* **Feature Engineering:** Created `days_since_trial_start` and activity frequency counts.

### 🧠 Identifying Conversion Drivers
By performing **Correlation Analysis** and **Logistic Regression**, we identified that specific "value-realization" activities serve as lead indicators for conversion.

### 🎯 Trial Goals Definition
Based on behavioral analysis, we defined the "Activated" state as an organization that completes these four core actions:
1. Create a project
2. Invite team members
3. Upload data
4. View dashboard

---

## 📊 Data Models (SQL)

We implemented two primary models in SQL:

1. **Trial Goals:** A feature-store style table tracking the completion status of each goal per organization.
2. **Trial Activation:** A binary classification table where `trial_activated = TRUE` only if all four goals are met.

---

## 📈 Funnel Overview
A clear view of the user journey from entry to revenue:

`Trial Started` ➡️ `Key Activity Performed` ➡️ `Activated` ➡️ `Converted`

*Key Insight:* Early engagement (within the first 72 hours) is the strongest predictor of long-term conversion.

---

## 📁 Project Structure
```text
trial-conversion-analysis/
├── data/           # Raw events.csv
├── notebooks/      # Analysis & modeling .ipynb
├── sql/            # DDL & transformation scripts
├── src/            # Preprocessing utilities
└── README.md
```

🚀 Business Impact
PQL Identification: Precise identification of Product Qualified Leads.

Strategy: Improved onboarding flows based on high-impact activities.

Scalability: Production-ready SQL models for warehouse integration.

📌 Next Steps
[ ] Migrate SQL models to dbt for production readiness.

[ ] Build a real-time activation dashboard in Tableau/Power BI.

[ ] Implement Cohort Analysis to track long-term retention.

[ ] Deploy a Predictive Lead Scoring model.

👤 Author
Michael Agyebeng Data Analyst | Data Officer | Financial Engineering
