# Trial-Conversion-Activation-Analysis

📌 Overview

This project analyzes behavioral event data from organizations that started a product trial between January and March. The goal is to identify key product activities that drive conversion, define trial success criteria (goals), and build scalable data models for tracking activation.

The project combines Python (analytics) and SQL (data modeling) to deliver actionable insights for product and growth teams.

🎯 Objectives

Clean and explore raw behavioral event data
Identify activities that strongly correlate with conversion
Define trial goals based on user behavior
Build SQL models for:
Trial Goals tracking
Trial Activation classification
Generate product insights and metrics to support decision-making

🧱 Dataset Description

The dataset consists of event-level behavioral data with the following fields:

Column	Description
organization_id	Unique organization identifier
activity_name	Product activity performed
timestamp	Event timestamp
converted	Whether the organization converted
converted_at	Conversion timestamp
trial_start	Trial start date
trial_end	Trial end date

⚙️ Tech Stack

Python: Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
SQL: Data modeling (marts layer)
Jupyter Notebook: Analysis & visualization

🧹 Data Cleaning & Preparation

Key preprocessing steps included:
Converted all date fields to proper datetime formats
Removed duplicates and invalid records
Standardized activity names
Filtered events within the valid trial window
Created derived features such as:
days_since_trial_start
activity counts per organization

🔍 Exploratory Analysis
Key Analyses Performed:
Overall conversion rate
Activity frequency distribution
Conversion rate by activity
Retention trends over trial duration

These analyses helped identify high-impact behaviors associated with successful conversions.

🧠 Identifying Conversion Drivers

To determine which activities influence conversion:
Aggregated activity counts at the organization level
Performed:
Correlation analysis
Logistic regression modeling
Insight:

Certain activities consistently showed strong positive relationships with conversion, indicating they represent core value realization moments in the product.

🎯 Trial Goals Definition

Based on behavioral analysis, the following trial goals were defined:

Create a project
Invite team members
Upload data
View dashboard

These actions represent meaningful engagement and product adoption.

⚡ Trial Activation Logic

An organization is considered Activated if it completes all defined trial goals.

This provides a clear and measurable definition of successful onboarding.

🧱 Data Models (SQL)

1. Trial Goals 
Tracks whether each organization completed each goal.
Output Example:
organization_id	created_project	invited_team_member	uploaded_data	viewed_dashboard

2. Trial Activation 

Determines whether an organization is fully activated.
Logic:
Activated = All goals completed
Output Example:
organization_id	trial_activated

📊 Product Metrics & Insights
Key Metrics:
✅ Conversion Rate
⚡ Activation Rate
⏱ Time to Conversion
🔁 Retention Curve
📉 Funnel Analysis
Example Insights:
Organizations completing more key actions are significantly more likely to convert
Early engagement (first few days) is critical for activation
Drop-offs occur before users complete core setup steps
📈 Funnel Overview
Trial Started
Key Activity Performed
Activated
Converted

This funnel highlights where users drop off and where optimization efforts should focus.

🚀 Business Impact

This analysis enables:

Clear definition of product-qualified leads (PQLs)
Improved onboarding strategies
Better conversion forecasting
Scalable tracking via data warehouse models
📁 Project Structure
📁 trial-conversion-analysis/
 ├── data/
 │    └── events.csv
 ├── notebooks/
 │    └── analysis.ipynb
 ├── sql/
 │    ├── trial_goals.sql
 │    └── trial_activation.sql
 ├── src/
 │    └── preprocessing.py
 ├── README.md

 
🧠 Key Takeaways
Not all activity is equal — specific actions drive conversion
Activation is a multi-step behavioral milestone, not a single event
Combining analytics + data modeling creates scalable business value


📌 Next Steps (Improvements)
Implement models using dbt for production readiness
Build a real-time activation dashboard (Power BI / Tableau)
Introduce cohort analysis for deeper retention insights
Deploy a predictive model for conversion probability

👤 Author

Michael Agyebeng
Data Analyst | Data Officer | Financial Engineering 
