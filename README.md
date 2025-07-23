# Support Ops Analysis & Dashboard
I created a support operations proof of concept that mirrors Zendesk workflows and performance objectives. Below is a visual overview of the dashboard built for this project. It highlights key customer experience metrics, including ticket volume, resolution time, SLA breach rate, CSAT, channel performance, and escalation trends.

<img width="990" height="764" alt="image" src="https://github.com/user-attachments/assets/f154f493-2401-44a7-9400-f72c56a66d79" />


# Project Overview: Support Ticket Analysis & Alert System

This project demonstrates how a support operations manager can quickly surface insights, automate monitoring, and drive CX improvements using data. Built in under 24 hours, this proof of concept replicates a real Zendesk environment using mock data across multiple support channels. It combines Python automation, Excel reporting, and predictive modeling to proactively manage ticket load, SLA performance, and customer satisfaction.

# Objective
To simulate a live CX operations workflow that monitors daily support activity, identifies performance risks, and provides decision-ready insights modeled around the KPIs and tools common in modern support environments.

# Methods & Tools
**1. Python (Jupyter Notebook)**

-Data ingestion & transformation: Cleaned a mock 90-day Zendesk export in .xlsx format, parsed ISO timestamps, and handled missing fields.

-Feature engineering: Calculated resolution_time in hours, flagged SLA breaches by priority tier (based on custom thresholds), and generated rolling metrics.

-Alert logic: Created a 7-day moving average baseline with a dynamic +20% buffer to detect abnormal ticket surges and potential backlogs.

-Forecast modeling: Used linear regression with weekday dummies to project ticket volume through month-end, capturing seasonality in support behavior.

-Evaluation metrics: Tracked model accuracy with MAE, RMSE, and MAPE to ensure reliable forecasting.

**2. Excel Automation**

-Monthly Summary Sheet: Used COUNTIFS, AVERAGEIFS, and date-based formulas to compute monthly KPIs: ticket volume, resolution time, SLA breach rate, and CSAT.

-Channel Performance Sheet: Dynamically extracted unique channels using formula logic, then calculated performance metrics across each source.

**Dashboard Sheet:**
-KPI cards with conditional formatting and sparklines

-Dual-axis combo chart visualizing channel volume, resolution speed, and CSAT in one view


**3. Visualization & Interpretation**
Leveraged Matplotlib/Seaborn (Python) and Excel charting to visualize time series trends, SLA risk bands, satisfaction drivers, and resolution distribution curves.


# Insights
-Social Media tickets consistently underperformed, with over 30% breaching SLA and CSAT trailing by 0.6 points vs email/web.

-CSAT drops sharply when resolution time exceeds 24 hours, especially for high-priority tickets, confirming SLA urgency as a CX lever.

-Ticket surges occurred most frequently on Mondays and Fridays, pointing to operational strain at week transitions.

-15% of open tickets were flagged as SLA-at-risk based on real-time tracking logic.

# Operational Recommendations
-Implement predictive alerting in Zendesk using the moving average + buffer model to auto-flag workload spikes.

-Reassign at-risk tickets proactively via priority-based triggers, minimizing CSAT fallout.

-Redirect social traffic to faster channels like email or chat through automated responses and workflows.

-Staffing model adjustment: Allocate more agents or flexible capacity to Mondays and Fridays where volume peaks recur.

# Why This Matters
This project shows not just the ability to analyze support data, but also to:

-Build robust monitoring systems based on available data

-Automate performance tracking and forecasting

-Translate ticket-level data into strategic operational moves

-Align closely with Circle’s mission to scale support through data, not headcount

It reflects the same mindset needed to lead and optimize customer experience operations in a modern SaaS environment, fast, insightful, and measurable.
