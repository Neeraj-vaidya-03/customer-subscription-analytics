# customer-subscription-analytics
An end-to-end data analytics project using SQL for relational database analysis and Power BI for executive dashboarding.
# Customer Subscription Analytics: SQL & Power BI End-to-End Project

## 📌 Project Overview
This project focuses on executing an end-to-end data analytics workflow—moving from relational database querying to interactive executive dashboarding. The core goal is to analyze customer subscription data, identify high-churn risk segments, evaluate engagement metrics, and provide actionable retention insights for business stakeholders.

---

## 🔍 Part 1: SQL Relational Database Analysis
The raw data was initially stored in a relational MySQL database schema `customersubscriptions`. Complex aggregations and filtering techniques were applied to answer key business operational metrics:
*   **Segmented Churn Volumes:** Conducted conditional aggregation via `SUM(CASE WHEN...)` to dynamically tabulate Active vs. Churned customer segments grouped across Subscription Types.
*   **Customer Feedback Breakdown:** Derived localized user satisfaction averages using `AVG()` multi-level grouping layered across Subscription Type and Gender matrixes.
*   **Low-Engagement Isolation:** Constructed targeted logical filter pipelines (`WHERE ... AND ...`) to extract critical high-risk lists combining low session counts (<5) and low satisfaction scores (<5).
*   **Inactivity Trackers:** Utilized `DATEDIFF()` and `DATE_SUB()` logic bounds to surface customers completely inactive for over 60 days.
*   **Cohort & Demographics:** Modeled custom conditional demographic brackets (`CASE WHEN BETWEEN...`) to construct age group-wise attrition metrics.

---

## 📊 Part 2: Power BI Interactive Executive Dashboard
The summarized relational logic was integrated directly into a comprehensive, responsive Power BI analytical app via an active data connector pipeline.
*   **Data Pipeline Architecture:** Established an optimal database connection mapping schema fields dynamically.
*   **Advanced DAX Modeling:** Programmed core performance metric measures (`Total Customers`, `Churned Customers`, and `% Churned Rate`) to fuel enterprise KPI visual tracking blocks.
*   **Strategic Visual Architecture Implemented:**
    1.  **Donut Charts:** Displaying the direct ratio distribution of Active vs. Churned client segments.
    2.  **Clustered Column Charts:** Providing quick dynamic evaluations of overall churn rates split by specific subscription lengths.
    3.  **Line-Trend Chronology:** Illustrating ongoing customer cancellation velocities over time.
    4.  **Scatter Matrix Plots:** Correlating raw cross-interaction points (User Engagement vs. Feedback Score) alongside dual color-legend alerts signaling active/churn statuses.
*   **Dynamic Multi-Slicer Paneling:** Wired multi-level visual filtering panels for Subscription Type, Gender, and Age variables, giving users the power to alter the canvas instantly.

---

## 💡 Core Insights & Value Delivered
*   Identified specific friction thresholds where lower engagement session numbers directly drop overall customer satisfaction scores.
*   Surfaced precise age demographic segments experiencing disproportionate cancellation trends.
*   Delivered a unified data ecosystem transitioning from rigid transactional records to an interactive tracking framework for marketing/retention stakeholders.
