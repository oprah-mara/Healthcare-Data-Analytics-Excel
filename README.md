# Healthcare Data Analysis & Interactive Excel Dashboard

A healthcare analytics project built in Microsoft Excel to explore hospital operations, patient visits, financial performance, and patient outcomes. The project uses data cleaning, Power Query, the Excel Data Model, DAX measures, PivotTables, PivotCharts, and interactive slicers to transform raw hospital data into meaningful insights.

![Healthcare Dashboard Preview](Healthcare%20interactive%20dashboard.png)

## 1. Project Overview

This project analyzes hospital activity over a two-year period, from January 2024 to December 2025. It focuses on understanding patient visit patterns, revenue and payment collection, department performance, diagnoses, patient satisfaction, and readmissions.

The goal is to demonstrate how Excel can be used to organize healthcare data, monitor key performance indicators (KPIs), and support data-driven operational decisions.

**Note:** The dataset is synthetic and was created for analytical and educational purposes. It does not contain actual patient records.

## 2. Project at a Glance

| Metric | Details |
|---|---|
| Domain | Healthcare Analytics |
| Tool | Microsoft Excel |
| Dataset Period | January 2024 – December 2025 |
| Hospital Visits | 1,800 |
| Cleaned Patient Records | 400 |
| Departments | 8 |
| Currency | Nigerian Naira (NGN) |
| Dashboard | Interactive |

## 3. Business Questions

The analysis explores questions such as:

- How do hospital visits and revenue vary over time?
- Which visit types account for the highest revenue?
- What are the most common diagnoses?
- How does payment collection vary across insurance providers and visit types?
- Which insurance categories have the highest outstanding balances?
- How do patient demographics vary by visit type?
- How do readmission rates and average length of stay differ across departments?
- How does patient satisfaction vary by department?

## 4. Dataset Description

The workbook contains three primary datasets:

- **Patients:** Patient demographics, age, gender, city, and insurance type.
- **Departments:** Department names, department heads, bed capacity, and floor information.
- **Visits:** Visit dates, visit types, diagnoses, length of stay, treatment costs, insurance coverage, payments, outcomes, satisfaction scores, and readmission status.

A calendar table was also created to support time-based analysis.

## 5. Tools & Techniques

- Microsoft Excel
- Power Query for data preparation
- Excel Data Model and Power Pivot
- DAX measures
- PivotTables and PivotCharts
- Interactive slicers
- Data cleaning and transformation
- KPI development and dashboard design

## 6. Data Cleaning & Preparation

The project involved preparing raw patient and visit records for analysis.

Key preparation steps included:

- Identifying and removing duplicate patient records.
- Standardizing inconsistent gender values.
- Trimming unnecessary spaces from text fields.
- Handling missing city values.
- Standardizing inconsistent visit-type capitalization.
- Converting visit dates into consistent date values.
- Creating calculated columns for outstanding balances and length-of-stay categories.
- Building relationships between patient, department, visit, and calendar tables.

The cleaned datasets were organized in the Excel Data Model to support analysis across multiple tables.

## 7. Key Performance Indicators (KPIs)

The analysis includes the following hospital performance metrics:

| KPI | Result |
|---|---:|
| Total Visits | 1,800 |
| Total Treatment Revenue | ₦436,095,200 |
| Total Amount Collected | ₦341,620,600 |
| Collection Rate | 78.34% |
| Outstanding Balance | ₦94,474,600 |
| Average Treatment Cost per Visit | ₦242,275 |
| Average Length of Stay | 4.45 days |
| Average Patient Satisfaction | 3.35 / 5 |
| Inpatient Readmission Rate | 12.44% |

## 8. Analysis & Key Findings

**Visit Type and Revenue**
- Inpatient visits generated approximately ₦371.1 million, representing the largest share of treatment revenue.
- Outpatient visits accounted for the highest number of visits, with 807 records.

**Diagnosis Analysis**
- Malaria was the most frequently recorded diagnosis, with 220 visits.
- Pneumonia followed with 165 visits.

**Payment Collection**
- The overall collection rate was 78.34%.
- Outstanding balances totaled approximately ₦94.47 million.
- Self-pay patients accounted for the largest outstanding balance.

**Patient Outcomes**
- The overall inpatient readmission rate was 12.44%.
- Average length of stay was approximately 4.45 days.
- Average patient satisfaction was 3.35 out of 5.

**Year-over-Year Revenue**
- Treatment revenue was approximately ₦221.14 million in 2024.
- Treatment revenue was approximately ₦214.96 million in 2025.
- This represents a decrease of approximately 2.8%.

## 9. Interactive Dashboard

The Excel dashboard provides a visual overview of hospital performance through KPI cards and eight charts.

Dashboard components include:

- Revenue by visit type.
- Monthly revenue trends.
- Top 10 diagnoses by visit volume.
- Collection rate by visit type and insurance type.
- Patient gender and age-group analysis.
- Readmission rate and average length of stay by department.
- Patient satisfaction by department.
- Outstanding balances by insurance type.

**Interactive slicers:**
- Year
- Department
- Insurance Type
- City

These slicers allow users to filter the dashboard and explore hospital performance across different categories.

## 10. Business Value

This project demonstrates how healthcare data can be used to:

- Monitor hospital financial performance.
- Identify patterns in patient visits and diagnoses.
- Track payment collection and outstanding balances.
- Compare operational and patient outcome metrics.
- Explore performance across departments and patient groups.

## 11. Limitations

- The dataset is synthetic and does not represent actual hospital operations.

