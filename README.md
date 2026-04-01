# Financial-Risk-and-Loan-Analytic-Power-BI-Project-

A multi-page interactive Power BI report analyzing financial risk metrics, applicant demographics, and loan default patterns across borrower segments, employment types, and credit score bands.

## Purpose

This Power BI report is built to analyze loan portfolio risk by examining borrower profiles, default behavior, income brackets, and year-over-year trends. It is structured across three focused report pages to support risk analysts and financial decision-makers with actionable, validated insights.

## Tech Stack

The report was built using the following tools and technologies:
- **SQL Server Management Studio (SSMS)** – Primary data storage and source
- **Power BI Dataflow (Power BI Service)** – Cloud-based data ingestion layer from SSMS
- **Power BI Desktop** – Data modeling, DAX development, and visualization
- **DAX (Data Analysis Expressions)** – All KPIs and measures, organized in page-specific calculated tables
- **Microsoft Excel** – Data validation of every DAX measure using pivot tables
- **Power BI Theme** – Consistent dark navy and teal color theme applied across all pages

## Data Source

- **Data Origin:** SQL Server Management Studio (SSMS)
- **Pipeline:** SSMS → Power BI Dataflow (Service) → Power BI Desktop

## Data Architecture & DAX Organization

- Data was imported from SQL Server into Power BI Service as a **Dataflow**, then connected to Power BI Desktop for modeling and reporting.
- All DAX measures are organized into **dedicated calculated tables — one per report page** — keeping the model clean and maintainable.
- Every DAX measure was **validated using Excel pivot tables** to ensure accuracy before being used in visuals.

## Features / Highlights

**Business Problem:** <br>
Financial institutions managing large loan portfolios need a structured way to identify high-risk borrower segments, track default trends over time, and understand the demographic factors driving credit exposure.

**Goals of the Report:** <br>
- Identify high-risk borrower segments by credit score, income bracket, and employment type
- Track year-over-year changes in loan volume and default rates
- Analyze demographic patterns influencing loan amounts and default behavior
- Deliver page-specific insights with embedded analytical commentary

## Walkthrough of Key Pages

### Page 1 – Financial Risk Metrics <br>
- **Ribbon Chart** – YTD loan amount segmented by credit score bins and marital status
- **Decomposition Tree** – Loan amount breakdown by income bracket and employment type (filtered to High Income)
- **Line Charts** – YOY loan amount change and YOY default loan change from 2013 to 2018
- **Key Insight:** 2015 saw the sharpest YOY default spike at +2.70%, flagged for external economic investigation

### Page 2 – Applicant Demographics & Financial Profile <br>
- **Line Chart** – Median loan amount across credit score bands (Low to High)
- **Donut Chart** – Average loan amount for high-credit borrowers by age group and marital status
- **Line Chart** – Number of loans distributed across education/employment types
- **Clustered Column Chart** – Loan amounts for middle-age adults segmented by mortgage and dependents status
- **Key Insights:**
  - Single seniors carry the highest average loan at 128.57K — highest risk-adjusted exposure in the portfolio
  - Adults with medium credit score hold 4.6bn in loans — the largest and most vulnerable segment

### Page 3 – Loan Default and Overview <br>
- **Line Charts** – Loan amount by purpose, average income by employment type, and default rate by employment type
- **Line Chart** – Average loan amount by age group
- **Line Chart** – Default rate (%) trend by year (2013–2018)
- **Key Insights:**
  - Unemployed borrowers default at a 44% higher rate than full-time employees (3.39% vs 2.36%)
  - Default rates have remained between 11.5–11.75% across all years, suggesting systemic risk rather than a trend

## Design Decisions
- **Consistent Theme** – Dark navy header with teal/light blue visuals applied uniformly across all three pages
- **Page-Scoped DAX Tables** – Measures are isolated per page to avoid clutter and improve debugging
- **Excel Validation** – Every metric was cross-verified in Excel pivot tables before publishing
- **Embedded Insights Panel** – Each page includes a highlighted commentary box with the most critical business finding

## Screenshots



### Loan Default and Overview
<img width="1878" height="1068" alt="Screenshot 2026-04-01 094107" src="https://github.com/user-attachments/assets/012a87be-9398-410e-8e8b-0bd06c825c3d" />

### Applicant Demographics & Financial Profile
<img width="1881" height="1065" alt="Screenshot 2026-04-01 094127" src="https://github.com/user-attachments/assets/55a5335b-7c4f-4736-b949-77d4d99d13d7" />

### Financial Risk Metrics
<img width="1883" height="1066" alt="Screenshot 2026-04-01 094143" src="https://github.com/user-attachments/assets/2e7cce80-9012-425e-9017-75f6c06b30be" />
