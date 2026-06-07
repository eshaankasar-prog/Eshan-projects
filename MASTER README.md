# Eshan | Supply Chain & Logistics Automation Portfolio

**Eshan Kasar** | MBA – Operations, Supply Chain Management & International Business  
**Role at time of build:** Executive – Global Logistics, UPL Global Business Services Ltd  
**Domain:** Import-Export · Customs Compliance · Logistics Automation · AI in Supply Chain  
**Target Roles:** AI in Supply Chain | Supply Chain Transformation Lead  
**Stack:** Power Automate · Power BI · Power Query · Excel VBA · SharePoint · Teams · React · TypeScript · Supabase

> **All projects below were built and deployed in a live operational environment — not tutorials, not simulations.**  
> Each one replaced a real manual process, with measurable time and cost savings formally submitted as Lean Improvement Projects to senior management.

---

## Table of Contents

| # | Project | Tool | Time Saved | Status |
|---|---------|------|-----------|--------|
| [01](#01-eshanpowerflow--document-routing--approval-automation) | EshanPowerflow | Power Automate · SharePoint · Teams | 3–5 hrs/day | ✅ Deployed |
| [02](#02-kpi-performance-dashboard) | KPI Performance Dashboard | Power BI · SharePoint · Copilot | Real-time visibility | ✅ Deployed |
| [03](#03-cargodocs-saas-in-progress) | Cargodocs SaaS | React · TypeScript · Supabase | — | 🚧 In Progress |
| [04](#04-daily-container-status-tracker) | Daily Container Status Tracker | Power Query · Excel | 130.5 hrs/year | ✅ Lean Project #2 |
| [05](#05-zcomex-turboquery-analysis) | Zcomex TurboQuery Analysis | Power Query · VBA · Excel | ~120 hrs/year | ✅ Deployed |
| [06](#06-auto-skit-report) | Auto SKIT Report | Power Query · Excel | 130.5 hrs/year | ✅ Lean Project #3 |
| [07](#07-auto-coa-report) | Auto COA Report | Power Query · Excel | 43.5 hrs/year | ✅ Lean Project #4 |

---

## 01 EshanPowerflow — Document Routing & Approval Automation

**Folder:** [`01_EshanPowerflow/`](01_EshanPowerflow/)  
**Tool:** Microsoft Power Automate · SharePoint · Microsoft Teams · Excel Online · AI Builder  
**Type:** Process Automation

### What It Solves
Import-export logistics teams handle high volumes of shipment documents — invoices, bills of lading, customs filings — that must be routed, reviewed, approved, and archived across departments. Doing this manually created compliance risk, version errors, and 3–5 hours of daily coordination overhead.

### What It Does
A scheduled Power Automate cloud flow that detects new PDF uploads, locks the processing queue, routes files through a multi-stage Teams approval, moves approved files to the OUT folder, and logs every rejected file to an Excel audit table — zero manual steps.

### Metrics
| Metric | Result |
|--------|--------|
| Manual coordination eliminated | 3–5 hrs/day |
| Document misrouting risk | Near zero |
| Approval visibility | Real-time via Teams |
| Audit trail | 100% logged |

### Files
| File | Description |
|------|-------------|
| [📄 EshanPowerflow_CaseStudy.pdf](01_EshanPowerflow/EshanPowerflow_CaseStudy.pdf) | Full case study with annotated screenshots and step walkthrough |
| [📦 EshanPowerflow_20260604181708.zip](01_EshanPowerflow/EshanPowerflow_20260604181708.zip) | Importable Power Automate flow export |
| [📖 Project README](01_EshanPowerflow/README.md) | Full project documentation |

---

## 02 KPI Performance Dashboard

**Folder:** [`02_KPI_Dashboard/`](02_KPI_Dashboard/)  
**Tool:** Power BI · SharePoint · Microsoft Copilot  
**Type:** Management Reporting — Team Performance Accountability System

### What It Solves
Logistics team managers had no real-time visibility into individual team member performance, SLA adherence, or the root causes behind missed targets. Reviews relied on end-of-week manual tallies with no drill-down and no audit trail on why targets were missed.

### What It Does
Each team member logs daily transactions into an individual SharePoint file. Power BI connects to all files and consolidates them into a unified performance command center with individual filters, transaction counts, SLA Hit/Miss classification, root-cause visibility for every missed SLA, full activity logs, and aggregated performance scoring.

### Files
| File | Description |
|------|-------------|
| [🖼️ Dashboard ](02_KPI_Dashboard/Dashboard-Kpi.pdf/) | Power BI report screenshots |
| [📖 Project README](02_KPI_Dashboard/README.md) | Full project documentation |

> Live demo available on request — Power BI runs inside M365 tenant and cannot be shared via public URL.

---

## 03 Cargodocs SaaS *(In Progress)*

**Folder:** [`03_Cargodocs/`](03_Cargodocs/)  
**Stack:** React · TypeScript · Supabase · TanStack Router · Lovable AI  
**Type:** Full-Stack Product Build

### What It Is
A logistics document management SaaS application being built from scratch — the product-level answer to the same operational pain points solved manually in projects 04–07.

### Files
| File | Description |
|------|-------------|
| [🖼️ App Screenshots](03_Cargodocs/assets/) | Current build screenshots |
| [📖 Project README](03_Cargodocs/README.md) | Full project documentation |

---

## 04 Daily Container Status Tracker

**Folder:** [`04_Daily_Container_Status/`](04_Daily_Container_Status/)  
**Tool:** Power Query · Excel  
**Type:** Lean Improvement Project #2 — formally submitted Dec 22, 2025

### What It Solves
The daily container status report took ~30 minutes per day per planner and produced frequent inconsistencies across 7 planners, 8 global regions, and 20+ manufacturing plants.

### Lean Impact
| Metric | Value |
|--------|-------|
| Time saved/year | 130.5 hours |
| Financial impact | $926.85/year |
| Refresh time | 5–6 min vs. 30 min manual |

### Files
| File | Description |
|------|-------------|
| [📊 Daily_Container_Status_SAMPLE.xlsx](04_Daily_Container_Status/Daily_Container_Status_SAMPLE.xlsx) | Anonymized working file with Power Queries intact |
| [🖼️ Screenshots](04_Daily_Container_Status/assets/) | Dashboard and query screenshots |
| [📖 Project README](04_Daily_Container_Status/README.md) | Full project documentation |

---

## 05 Zcomex TurboQuery Analysis

**Folder:** [`05_Zcomex_TurboQuery/`](05_Zcomex_TurboQuery/)  
**Tool:** Power Query · VBA · Excel  
**Type:** Operational Tool — Import PO Compliance Checker

### What It Solves
Processing raw ZCOMEX export data for import PO compliance was a 2-hour weekly manual task. Missing documents, blank ETDs, and unassigned containers were caught too late.

### Files
| File | Description |
|------|-------------|
| [📊 Zcomex_TurboQuery_Analysis_SAMPLE.xlsx](05_Zcomex_TurboQuery/Zcomex_TurboQuery_Analysis_SAMPLE.xlsx) | Anonymized 23-sheet compliance analyzer |
| [🖼️ Screenshots](05_Zcomex_TurboQuery/assets/) | Tool and query screenshots |
| [📖 Project README](05_Zcomex_TurboQuery/README.md) | Full project documentation |

---

## 06 Auto SKIT Report

**Folder:** [`06_Auto_SKIT_Report/`](06_Auto_SKIT_Report/)  
**Tool:** Power Query · Excel  
**Type:** Lean Improvement Project #3 — formally submitted Dec 18, 2025

### What It Solves
The NAM region SKIT report took 35 minutes daily to prepare manually across multiple data sources. Copy-paste errors caused PGI processing delays.

### Lean Impact
| Metric | Value |
|--------|-------|
| Time saved/year | 130.5 hours |
| Refresh time | 5–6 min vs. 35 min manual |

### Files
| File | Description |
|------|-------------|
| [📊 SKIT_COA_Query_SAMPLE.xlsx](06_Auto_SKIT_Report/SKIT_COA_Query_SAMPLE.xlsx) | Anonymized working file — SKIT sheets |
| [🖼️ Screenshots](06_Auto_SKIT_Report/assets/) | Report and query screenshots |
| [📖 Project README](06_Auto_SKIT_Report/README.md) | Full project documentation |

---

## 07 Auto COA Report

**Folder:** [`07_Auto_COA_Report/`](07_Auto_COA_Report/)  
**Tool:** Power Query · Excel  
**Type:** Lean Improvement Project #4 — formally submitted Dec 18, 2025

### What It Solves
COA document tracking for US-bound agrochemical containers took ~10 minutes daily. Missing COAs flagged late caused port pickup delays.

### Lean Impact
| Metric | Value |
|--------|-------|
| Time saved/year | 43.5 hours |
| Refresh time | 1–2 min vs. 10 min manual |

### Files
| File | Description |
|------|-------------|
| [📊 SKIT_COA_Query_SAMPLE.xlsx](07_Auto_COA_Report/SKIT_COA_Query_SAMPLE.xlsx) | Anonymized working file — COA sheets |
| [🖼️ Screenshots](07_Auto_COA_Report/assets/) | Report and query screenshots |
| [📖 Project README](07_Auto_COA_Report/README.md) | Full project documentation |

---

## Proof of Work — Lean Project Submissions

| Project | Lean # | Submitted To | Date |
|---------|--------|-------------|------|
| Daily Container Status Tracker | #2 | SCM Manager + SCM Lead | Dec 22, 2025 |
| Auto SKIT Report | #3 | SCM Leadership | Dec 18, 2025 |
| Auto COA Report | #4 | SCM Leadership | Dec 18, 2025 |

Email references and Lean project PPTs available on request during the interview process.

---

## Total Impact Summary

| Metric | Value |
|--------|-------|
| Total annual hours saved (documented) | 304.5+ hours |
| Financial impact (documented, USD) | $926.85/year — Container Status alone |
| Manual processes fully automated | 5 |
| Teams impacted | Global Logistics · Planning · NAM Operations · SCM Leadership |
| Tools deployed in production | Power Automate · Power Query · Power BI · VBA · SharePoint · Teams |

---

## Data Privacy Notice

All sample files use anonymized data. Company names, personnel names, product names, container numbers, B/L numbers, and PO numbers have been replaced with generic placeholders. Formula logic, Power Query M-code, VBA structure, and data relationships are preserved exactly as built in production.

---

## Contact

- **LinkedIn:** *(add)*
- **Email:** *(add)*
- **Live Demo (Power BI / Power Automate):** Available via screen-share — contact to schedule
