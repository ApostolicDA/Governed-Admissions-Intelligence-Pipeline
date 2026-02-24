# 🎓 Governed Admissions Intelligence Pipeline  
### From Fragmented Data to Validated Executive Insight  
**SQL • PostgreSQL • Data Governance • Looker Studio**

---

## 🚨 The Problem

Saint Louis University’s international admissions data existed across four disconnected systems:

- Applicant Records  
- Outreach Data  
- Connect Engagement Logs  
- SEVIS Visa Status  

The data was fragmented, inconsistent, and unreliable for executive-level decision-making.

Key challenges included:

- Scientific notation timestamps (e.g., 1.75E+12)
- String "NULL" values corrupting calculations
- One-to-many outreach duplication
- Missing Country data
- Dashboard metrics with no validation layer

Without proper governance, any visualization built on this foundation risked being misleading.

---

## 🎯 The Objective

To design a **governed analytics pipeline** that:

1. Integrates four raw datasets into a unified PostgreSQL warehouse  
2. Cleans and standardizes data for analytical integrity  
3. Builds an executive-facing Looker Studio dashboard  
4. Validates every KPI directly in SQL  
5. Ensures full reconciliation between database and visualization layer  

This was not just a dashboard project.  
It was a **data integrity project**.

---

## 🛠 Technical Architecture

### Data Layer
- PostgreSQL (pgAdmin 4)
- Staging tables for raw ingestion
- Structured SQL transformations

### Governance Controls
- Scientific notation timestamp correction
- Explicit NULL normalization (`NULLIF`)
- Date standardization (`YYYY-MM-DD`)
- Financial field numeric casting
- Deduplication using `DISTINCT ON`
- Outreach history consolidation via `STRING_AGG`
- LEFT JOIN strategy to preserve applicant records

### Visualization Layer
- Looker Studio Executive Dashboard
- Funnel Analysis
- Financial Metrics
- Geographic Segmentation
- Interactive Filtering

### Validation Layer
All KPIs recalculated using SQL aggregation queries and reconciled against dashboard outputs.

No unresolved discrepancies remained.

---

## 🔄 End-to-End Data Pipeline

1. Raw CSV ingestion into staging tables  
2. Data cleaning and type enforcement  
3. Controlled master dataset integration  
4. Export to visualization layer  
5. SQL-based KPI validation  
6. Reconciliation of filters and aggregations  

This ensured traceability from raw record → final executive insight.

---

## 📊 Validated Executive Insights

- **6,893 Total Applicants**
- **37.8% Admission Rate**
- **58% Yield Rate (Admit → Deposit)**
- **$13.4M Potential Tuition Revenue**
- Strong financial surplus reduces visa risk
- High recruitment concentration in India & Nigeria
- Heavy program dependency on STEM streams

All metrics were confirmed directly from the master PostgreSQL dataset.

---

## ⚠️ Key Data Risks Identified

- 90%+ missing Country data (required pivot to Citizenship)
- Funnel distortion risk from one-to-many outreach joins
- Financial metric sensitivity to NULL handling
- Program dependency concentration risk
- Geographic over-reliance on limited regions

These risks were mitigated through structured SQL governance controls.

---

## 💡 Strategic Recommendations

1. Diversify recruitment markets to reduce geographic dependency  
2. Normalize categorical fields to prevent dashboard aggregation drift  
3. Implement automated ETL validation checks  
4. Expand tracking of financial surplus vs visa outcomes  
5. Introduce time-series analysis using standardized timestamps  

---

## 👤 My Role

**Team Lead – Data Governance & SQL Validation**

- Designed master dataset integration strategy  
- Implemented SQL cleaning transformations  
- Led KPI validation and reconciliation process  
- Ensured dashboard integrity through structured SQL verification  
- Consolidated and standardized final analytical outputs  

---

## 🧠 Why This Project Matters

Dashboards without validation can mislead stakeholders.

This project demonstrates the ability to:

- Engineer reliable analytical systems  
- Think beyond visualization into governance  
- Detect and correct metric distortion risks  
- Deliver executive-ready, validated insights  

It reflects a commitment to building analytics systems where **accuracy precedes aesthetics**.

---

## 🔗 Live Dashboard

[Insert Looker Studio Link Here]

---

## 📂 Repository Structure

- `/sql` → Data cleaning and validation queries  
- `/reports` → Dashboard and validation documentation  
- `/screenshots` → Visual dashboard exports  
- `/presentation` → Final executive presentation  

---

### Built with a Data Governance Mindset.
