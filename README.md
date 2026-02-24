
# 🎓 Governed Admissions Intelligence Pipeline  
**From Raw Admissions Data to Validated Executive Dashboard**

---
## 🚀 What I Built

Designed and implemented a governed admissions analytics system that:

• Integrated 4 raw operational systems into a centralized PostgreSQL warehouse  
• Cleaned and standardized 6,800+ records  
• Engineered a master analytical dataset  
• Built an executive dashboard with validated KPIs  
• Implemented SQL-based metric reconciliation to ensure BI accuracy  

This project demonstrates production-style data engineering, governance, and business intelligence validation.
## 📌 Overview

This project delivers an end-to-end admissions analytics pipeline integrating four fragmented datasets (**Applicant, Connect, Outreach, SEVIS**) into a governed PostgreSQL warehouse powering a fully validated executive dashboard in Looker Studio.

The system was designed to:

- Clean and standardize 6,800+ application records  
- Resolve data quality issues (NULL handling, timestamp inconsistencies, one-to-many relationships)  
- Engineer a master integration layer using SQL  
- Build a dynamic admissions funnel dashboard  
- Implement a SQL-based KPI validation framework  
- Ensure full metric reconciliation between database and visualization layer  

All dashboard metrics were validated directly against the PostgreSQL master dataset to ensure governance, accuracy, and stakeholder trust.

---

## 🏢 Business Problem

The admissions data ecosystem suffered from:

- Fragmented data sources across four systems  
- Inconsistent timestamp formats (epoch vs string dates)  
- 90%+ missing Country data  
- One-to-many outreach records inflating funnel counts  
- Misaligned aggregation logic between database and dashboard  

Without validation controls, KPI reporting risked inaccuracies that could misinform strategic decisions.

---

## 🏗 Data Architecture

**Raw CSV Files**  
→ PostgreSQL Staging Tables  
→ Data Cleaning & Standardization Layer  
→ Master Integrated Table (`master_applicants`)  
→ Looker Studio Executive Dashboard  
→ SQL Validation & Reconciliation Layer  

This architecture ensures that visualization metrics are fully governed by database logic.

---

## 🧹 Data Engineering Highlights

- Converted epoch timestamps using `TO_TIMESTAMP()`  
- Standardized NULL values using `NULLIF()`  
- Preserved full applicant base using LEFT JOIN integration  
- Consolidated one-to-many outreach records using `DISTINCT ON` and `STRING_AGG()`  
- Created binary indicator flags for accurate funnel metrics  
- Implemented numeric casting for financial aggregation  
- Ensured no duplicate inflation of deposit or admission counts  

---

## 📊 Executive Dashboard KPIs

The validated dashboard includes:

- Total Applicants  
- Admission Rate (37.8%)  
- Yield Rate (58%)  
- Tuition Revenue (~$13.4M Potential)  
- Financial Surplus  
- Funnel Analysis (Applied → Admitted → Deposit)  
- Citizenship Leaderboard  
- Program Popularity Distribution  

All metrics were reconciled against PostgreSQL queries.

---

## 🔐 KPI Validation & Governance Framework

To ensure metric integrity, each dashboard KPI was re-calculated directly in PostgreSQL using equivalent SQL aggregation queries.

### Validation Process

1. Identify dashboard KPI  
2. Write equivalent SQL aggregation  
3. Execute query on master dataset  
4. Compare SQL output with dashboard metric  
5. Reconcile discrepancies  

### Filter-Level Validation

The following interactive filters were validated using SQL WHERE clauses:

- Citizenship filter (e.g., Zimbabwe)  
- Intake filter (Fall 2024)  
- Visa Status filter (Accepted)  

All metrics reconciled successfully, confirming dashboard accuracy and filter integrity.

---

## 📈 Key Insights

- Strong 58% yield from admitted students  
- Heavy applicant concentration in STEM programs  
- Geographic dependency on a few key regions  
- Financial surplus suggests strong visa readiness  
- Fall intake dominates, creating operational bottlenecks  

---
## 📈 Business Impact

- Identified 58% yield rate from admitted students
- Exposed geographic concentration risk (India & Nigeria dependency)
- Highlighted STEM program dominance (~40% concentration)
- Revealed 99% missing Country data risk
- Improved stakeholder trust via SQL-backed KPI validation
---
## ⚠️ Data Risks Identified

- 99% missing Country data → Citizenship used as proxy  
- Counselor assignment stored in non-normalized format  
- Timestamp inconsistency limits time-series analysis  
- Null-sensitive financial aggregations  
- Operational blind spots in outreach appointment tracking  

---

## 🚀 Future Enhancements

- Automate ETL pipeline  
- Normalize counselor assignment structure  
- Implement timestamp standardization  
- Build predictive yield model  
- Develop visa approval correlation analysis  
- Introduce automated data quality monitoring  

---

## 🛠 Tools Used

- PostgreSQL (pgAdmin 4)  
- SQL  
- Looker Studio  
- Microsoft Excel / CSV  
- GitHub for documentation  

---

## 📸 Recommended Repository Structure


Governed-Admissions-Intelligence-Pipeline/
│
├── README.md
├── sql/
│ ├── staging_queries.sql
│ ├── cleaning_queries.sql
│ ├── master_table_creation.sql
│ ├── validation_queries.sql
│
├── assets/
│ ├── architecture_diagram.png
│ ├── dashboard_overview.png
│ ├── funnel_closeup.png
│ ├── financial_kpis.png
│ ├── sql_validation_example.png
│
└── documentation/
├── data_quality_report.pdf
├── insight_summary_slides.pptx


---

## 🧠 What This Project Demonstrates

- End-to-end analytics engineering  
- Data governance implementation  
- KPI reconciliation methodology  
- Funnel logic validation  
- Financial metric standardization  
- Executive-ready dashboard design  

This project reflects the full analytics lifecycle — from raw data ingestion to validated strategic insights.
