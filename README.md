# Hospital Operations & Patient Analytics (Excel)

An end-to-end Excel analytics project on a synthetic hospital dataset (Jan 2024 – Dec 2025, currency in NGN). Raw data is cleaned with Power Query, modeled in the Excel Data Model, summarized with DAX measures and PivotTables, and presented in an interactive dashboard.

> Data is synthetic, generated for training purposes. No real patient information.

## Tools
Excel · Power Query · Power Pivot / DAX · PivotTables & Slicers

## Data model
| Table | Type | Grain | Rows |
|---|---|---|---|
| `tblVisits` | Fact | 1 row per visit/admission | 1,800 |
| `tblPatients` | Dimension | 1 row per patient | 400 (after cleaning) |
| `tblDepartments` | Dimension | 1 row per department | 8 |
| `Calender` | Date dimension | 1 row per day | 731 |

```
tblPatients[PatientID]    1 ──► *  tblVisits[PatientID]
tblDepartments[DeptID]    1 ──► *  tblVisits[DeptID]
Calender[Date]            1 ──► *  tblVisits[VisitDate]
```

## Data cleaning
| Issue in raw data | Fix |
|---|---|
| 8 duplicate patient records | De-duplicated on `PatientID` |
| Mixed Gender spellings (`Male`, `male`, `FEMALE`, `F`, ` Male`) | Standardized to `M` / `F` |
| Extra spaces in text fields | Trimmed |
| Blank `City` values | Handled in the patient table |
| Some `VisitDate` values stored as text | Converted to date type |
| Mixed-case `VisitType` (e.g. `outpatient`) | Standardized to proper case |
| Blank `SatisfactionScore` | Left blank (= no survey response) so averages aren't skewed |

Added columns: `Outstanding` (TreatmentCost − AmountPaid), `LOS Band`, `Age Group`.

## KPIs (DAX measures)
| Measure | Value |
|---|---|
| Total Visits | 1,800 |
| Total Revenue | ₦436.1M |
| Collected | ₦341.6M |
| Collection Rate | 78.3% |
| Avg Cost / Visit | ₦242,275 |
| Avg Length of Stay | 4.45 days |
| Avg Satisfaction | 3.35 / 5 |
| Readmission Rate | 12.4% |
| Revenue YoY (2025 vs 2024) | 0.97 (₦215.0M vs ₦221.1M, about −2.8%) |

## Analysis (PivotTables)
1. Revenue and visits by visit type
2. Monthly revenue trend
3. Top 10 diagnoses by volume
4. Collection rate by visit type and insurance type
5. Visits by gender, age group and visit type
6. Readmission rate and average LOS by department
7. Satisfaction by department
8. Outstanding balance by insurance type

## Selected findings
- Inpatient visits are 43% of volume but 85% of revenue (₦371.1M of ₦436.1M).
- Malaria (220) and pneumonia (165) are the most frequent diagnoses.
- Self-Pay carries the largest outstanding balance (₦32.7M of ₦94.5M).
- Orthopaedics has the highest satisfaction (3.57); Emergency the lowest (3.23).

## Dashboard
![Dashboard](docs/images/dashboard.png)

## How to use
Open `workbook/Healthcare_Excel_Project.xlsx` in desktop Excel (Windows recommended; the Data Model, DAX measures and slicers need Power Pivot). The CSVs in `data/` are for quick inspection without Excel.

## Author
Amarachi · [GitHub](https://github.com/oprah-mara)

