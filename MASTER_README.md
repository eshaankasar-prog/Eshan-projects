# Eshan | Supply Chain & Logistics Automation Portfolio

**Eshan** | MBA – Operations, Supply Chain Management & International Business  
**Domain:** Import-Export | Logistics | Customs Compliance | AI in Supply Chain  
**Target Roles:** AI in Supply Chain | Supply Chain Transformation Lead  
**Stack:** Power Automate · Power BI · Power Query · Excel · SharePoint · Teams · React/TypeScript (Cargodocs)

---

## Portfolio at a Glance

| # | Project | Tool(s) | Business Problem Solved |
|---|---------|---------|------------------------|
| 01 | [EshanPowerflow](#01-eshanpowerflow) | Power Automate, SharePoint, Teams, Excel | Automated document routing & multi-stage approval — eliminated 3–5 hrs/day manual coordination |
| 02 | [Daily Container Status Tracker](#02-daily-container-status-tracker) | Power Query, Excel | Real-time container operations dashboard across 8 regions, 20+ plants, 7 planners |
| 03 | [Zcomex TurboQuery Analysis](#03-zcomex-turboquery-analysis) | Power Query, VBA, Excel | Automated import PO compliance checker — flags doc gaps, missing containers, ETD blanks |
| 04 | [SKIT & COA Query](#04-skit--coa-query) | Power Query, Excel | Port pickup & PGI tracker for US-bound agrochemical containers with COA cross-reference |
| 05 | [Real-time Logistics Dashboard](#05-real-time-logistics-dashboard) | Power BI, Microsoft Copilot | *(Add your description here)* |
| 06 | [Cargodocs SaaS](#06-cargodocs-saas) | React, TypeScript, Supabase, TanStack Router | Full-stack logistics document management SaaS — built with Lovable AI |

---

## 01 EshanPowerflow

**Folder:** `01_EshanPowerflow/`  
**Tool:** Microsoft Power Automate (Cloud Flow)  
**Integrations:** SharePoint · Teams · Excel Online · AI Builder

A scheduled automation replacing 3–5 hours of daily manual document coordination. Detects new uploads, routes files through multi-stage approval, moves approved files to output folders, and logs every decision to an Excel audit trail — zero manual steps.

**Key Technical Concepts:** Recurrence triggers · SharePoint list-based queue locking · Multi-approver Teams approval · Select + Join transformations · Nested For Each loops · State management across async approval pauses

→ [Full Case Study PDF](01_EshanPowerflow/EshanPowerflow_CaseStudy.pdf)  
→ [Flow Export (.zip)](01_EshanPowerflow/EshanPowerflow_20260604181708.zip)  
→ [Guide](01_EshanPowerflow/assets/Guide.pdf)

---

## 02 Daily Container Status Tracker

**Folder:** `02_Daily_Container_Status/`  
**Tool:** Power Query + Excel  
**Data:** 822 containers · 8 global regions · 20+ manufacturing plants · 7 logistics planners

Operational command center for export container management. Tracks dispatch MTD, open ARD windows, stuffing status, DO expiry, transporter arrangements, and booking pipeline — all auto-refreshed via Power Query from source data.

**Sheets:** Summary (by Plant / Region / Planner) · Booking Pending · Open Orders · Dispatch Log

**Key Technical Concepts:** Multi-source Power Query consolidation · Dynamic summary pivots by region and planner · ARD window calculations · Conditional status flags

→ [Sample Data File](02_Daily_Container_Status/Daily_Container_Status_SAMPLE.xlsx)  
→ [Screenshots](02_Daily_Container_Status/assets/)

---

## 03 Zcomex TurboQuery Analysis

**Folder:** `03_Zcomex_TurboQuery/`  
**Tool:** Power Query + VBA + Excel  
**Data:** Multi-country import PO pipeline (India, Brazil, Mexico, Belgium, Netherlands, US, Japan, CN, HK)

Automated import compliance analyzer. Processes raw ZCOMEX export data and flags exceptions across 15+ categories: missing India/CO documents, blank ETDs, missing container assignments, expired payment terms, transit time breaches by country, and load number gaps. VBA-driven summary layer provides instant exception counts.

**Key Technical Concepts:** Power Query M-language transformations · VBA summary automation · Multi-country transit time logic · Exception categorization across 23 tabs · Conditional compliance flags

→ [Sample Data File](03_Zcomex_TurboQuery/Zcomex_TurboQuery_Analysis_SAMPLE.xlsx)  
→ [Screenshots](03_Zcomex_TurboQuery/assets/)

---

## 04 SKIT & COA Query

**Folder:** `04_SKIT_COA_Query/`  
**Tool:** Power Query + Excel  
**Data:** US-bound agrochemical container shipments — COA document tracking + PGI processing pipeline

Cross-references Certificate of Analysis (COA) document availability against active shipment delivery numbers, container numbers, and B/L data. Maintains a full volume tracker of processed SKIT-PGI records with port pickup dates, send-for-PGI timestamps, and remarks. Flags shipments where COA is pending before port pickup.

**Key Technical Concepts:** Power Query cross-referencing across multiple data sources · VLOOKUP-equivalent logic for COA status · Volume tracking with process metadata · Subject-line generation for email automation

→ [Sample Data File](04_SKIT_COA_Query/SKIT_COA_Query_SAMPLE.xlsx)  
→ [Screenshots](04_SKIT_COA_Query/assets/)

---

## 05 Real-time Logistics Dashboard

**Folder:** `05_PowerBI_Dashboard/`  
**Tool:** Power BI + Microsoft Copilot  
*(Add description here — what does it track? What KPIs? What data source?)*

→ [Case Study PDF](05_PowerBI_Dashboard/Dashboard-Kpi.pdf)

---

## 06 Cargodocs SaaS

**Folder:** `06_Cargodocs/`  
**Stack:** React · TypeScript · Supabase · TanStack Router · Lovable AI

A full-stack logistics document management SaaS application — currently in active development as part of the AI in Supply Chain portfolio transition.

→ [Live App / Repo Link] *(add when ready)*

---

## Why This Portfolio Matters

These aren't tutorial projects. Every file here was built to solve a real operational problem in an active import-export environment:

- **EshanPowerflow** replaced a manual daily process across 5 departments
- **Container Tracker** gave a logistics team of 7 planners a single source of truth across 822 active containers
- **Zcomex TurboQuery** turned a 2-hour weekly compliance review into a 5-minute exception check
- **SKIT/COA Query** eliminated a recurring bottleneck between port operations and documentation teams

> **Note on data privacy:** All sample files use anonymized/generic data. Company names, supplier names, customer names, product names, and personnel identifiers have been replaced with generic placeholders. The structure, formulas, and logic are preserved exactly as built.

---

## Contact & Links

- **LinkedIn:** *(add)*  
- **Email:** *(add)*  
- **Live Demo (Power Automate / Power BI):** Available on request via screen-share
