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
| [04](#04-daily-container-status-tracker) | Daily Container Status Tracker | Power Query · Excel | 130.5 hrs/year | ✅ Lean Project |
| [05](#05-zcomex-turboquery-analysis) | Zcomex TurboQuery Analysis | Power Query · VBA · Excel | ~120 hrs/year | ✅ Deployed |
| [06](#06-auto-skit-report) | Auto SKIT Report | Power Query · Excel | 130.5 hrs/year | ✅ Lean Project |
| [07](#07-auto-coa-report) | Auto COA Report | Power Query · Excel | 43.5 hrs/year | ✅ Lean Project |

---

## 01 EshanPowerflow — Document Routing & Approval Automation

**Folder:** `01_EshanPowerflow/`  
**Tool:** Microsoft Power Automate · SharePoint · Microsoft Teams · Excel Online · AI Builder  
**Type:** Process Automation

### What It Solves
Import-export logistics teams handle high volumes of shipment documents — invoices, bills of lading, customs filings — that must be routed, reviewed, approved, and archived across departments. Doing this manually created compliance risk, version errors, and 3–5 hours of daily coordination overhead.

### What It Does
A scheduled Power Automate cloud flow that:
- Detects new PDF uploads in a SharePoint library via recurrence trigger
- Uses SharePoint List-based queue locking to prevent concurrent run conflicts
- Routes files through a multi-stage approval workflow via Microsoft Teams
- On **approval** → moves files to the OUT folder, posts Teams channel notification, updates list status
- On **rejection** → loops through files with nested For Each, logs each to an Excel audit table with timestamp and approver
- Releases the process lock for the next run cycle

### Key Technical Concepts
- Recurrence triggers with early-exit condition logic (PDF Available gate)
- SharePoint list-based state management (race-condition proof)
- Multi-approver async Teams approval with flow pause/resume
- Select + Join transformations for file manifest compilation
- Nested For Each loops with Excel row-append operations

### Metrics
| Metric | Result |
|--------|--------|
| Manual coordination eliminated | 3–5 hrs/day |
| Document misrouting risk | Near zero — enforced by condition logic |
| Approval visibility | Real-time via Teams |
| Audit trail | 100% logged — timestamp, approver, decision |

### Files in This Folder
```
01_EshanPowerflow/
├── EshanPowerflow_CaseStudy.pdf
├── EshanPowerflow_20260604181708.zip
├── README.md

```

> **To import the flow:** Power Automate → My Flows → Import → Upload .zip → Map connections (SharePoint, Teams, Excel) → Enable. Requires M365 with standard connectors.

---

## 02 KPI Performance Dashboard

**Folder:** `02_KPI_Dashboard/`  
**Tool:** Power BI · SharePoint · Microsoft Copilot  
**Type:** Management Reporting — Team Performance Accountability System

### What It Solves
Logistics team managers had no real-time visibility into individual team member performance, SLA adherence, or the root causes behind missed targets. Performance reviews relied on end-of-week manual tallies with no drill-down capability and no audit trail on why targets were missed.

### What It Does
Each team member logs their daily transactions into an individual SharePoint file. Power BI connects to all files simultaneously and consolidates them into a unified performance command center:

- **Individual & team filters** — slice by any team member, date range, or activity type
- **Transaction counts** — daily and cumulative volume per person
- **SLA tracking** — every task classified as SLA Hit or SLA Missed against defined thresholds
- **Hit/Miss rate** — visual SLA adherence percentage per team member and for the team overall
- **Root cause visibility** — when an SLA is missed, the reason entered by the team member surfaces directly in the dashboard — no chasing, no manual follow-up
- **Activity log** — full chronological transaction log with timestamps per person
- **Performance scoring** — aggregated KPIs based on volume, timeliness, and SLA adherence

### Why This Is More Than a Dashboard
This is a **team accountability system with root-cause traceability** — the kind of tool a Supply Chain Transformation lead would design for operational governance. It required understanding both the data pipeline (SharePoint → Power BI) and the management question being answered (not just "what happened" but "why did it miss").

### Key Technical Concepts
- Power BI connected to multiple SharePoint sources with unified data model
- Dynamic slicers for team member, date, and SLA status
- Conditional SLA Hit/Miss classification logic
- Drill-through from summary KPI view to transaction-level activity log
- Microsoft Copilot integration for natural language querying of dashboard data

### Files in This Folder
```
02_KPI_Dashboard/
├── README.md
└── assets/
    └── screenshots/    ← add Power BI screenshots here
```

> **Note:** Power BI reports run inside an M365 tenant and cannot be shared via public URL. Screenshots and Loom walkthrough serve as portfolio artifacts. Live demo available on request.

---

## 03 Cargodocs SaaS *(In Progress)*

**Folder:** `03_Cargodocs/`  
**Stack:** React · TypeScript · Supabase · TanStack Router · Lovable AI  
**Type:** Full-Stack Product Build

### What It Is
Cargodocs is a logistics document management SaaS application being built from scratch. It targets the same operational pain points solved manually in projects 04–07 below — but as a product, not an internal spreadsheet.

### Why It Exists
Every project in this portfolio exposed the same underlying problem: logistics teams manage critical documents — BLs, COAs, SKIT reports, container status — through a patchwork of spreadsheets and manual emails. Cargodocs is the product-level answer to that problem.

The difference between projects 04–07 and Cargodocs is the difference between **fixing a broken process** and **replacing it with infrastructure**.

### Current Build Status
- ✅ Project scaffolded — React + TypeScript + TanStack Router
- ✅ Supabase backend configured
- 🚧 Core document management module in development
- 🚧 AI-assisted document parsing — in design

### Files in This Folder
```
03_Cargodocs/
├── README.md
└── assets/
    └── screenshots/
```

> **Live app / repo link:** *(add when ready)*

---

## 04 Daily Container Status Tracker

**Folder:** `04_Daily_Container_Status/`  
**Tool:** Power Query · Excel  
**Type:** Lean Improvement Project #2 — formally submitted Dec 22, 2025

### What It Solves
The team's daily container status report was prepared manually, taking ~30 minutes per day with frequent inconsistencies. Seven logistics planners across 8 global regions and 20+ manufacturing plants had no single source of truth.

### What It Does
Power Query automation consolidating multi-source data into a live operational dashboard:
- **Summary** — container counts by Plant, Region, and Logistics Planner
- **Booking Pending** — open ARD windows, transporter arrangements, DO expiry flags
- **Open Orders** — dispatch pipeline by plant and region
- **Dispatch Log** — MTD dispatch tracking with stuffing status
- Refreshes in 5–6 minutes vs. 30 minutes manual

### Lean Impact (Formally Documented)
| Metric | Value |
|--------|-------|
| Time saved per day | 25 minutes |
| Time saved per year | 130.5 hours |
| Financial impact (INR/year) | ₹81,562.50 |
| Financial impact (USD/year) | $926.85 |
| Implementation date | 22 December 2025 |

### Files in This Folder
```
04_Daily_Container_Status/
├── Daily_Container_Status_SAMPLE.xlsx
├── README.md
└── assets/
    └── screenshots/
```

> The sample file contains the original Power Query logic intact. Data → Refresh All to inspect query structure. Source paths will need remapping to your own data.

---

## 05 Zcomex TurboQuery Analysis

**Folder:** `05_Zcomex_TurboQuery/`  
**Tool:** Power Query · VBA · Excel  
**Type:** Operational Tool — Import PO Compliance Checker

### What It Solves
Processing raw ZCOMEX system exports for import PO compliance review was a 2-hour weekly manual task. Missing documents, blank ETDs, and unassigned containers were caught late — causing shipment delays and compliance flags.

### What It Does
A 23-sheet automated compliance analyzer ingesting ZCOMEX export data and flagging exceptions:
- **IND DOC PND** — India import documents pending
- **CO DOC PND** — country of origin documents pending
- **Missing Container** — POs with no container assigned
- **ETD Blank** — shipments with no ETD set
- **Load No Blank** — missing load numbers
- **Transit Time tabs** — country-by-country TT exception tracking (India, Brazil, Mexico, Belgium, Netherlands, US, Japan, CN, HK)
- **VBA Summary layer** — instant exception counts across all categories, auto-updated on refresh

### Key Technical Concepts
- Power Query M-language transformations on raw ERP exports
- VBA macro-driven summary aggregation
- Multi-country transit time threshold logic
- Cross-tab exception categorization across 23 structured sheets

### Files in This Folder
```
05_Zcomex_TurboQuery/
├── Zcomex_TurboQuery_Analysis_SAMPLE.xlsx
├── README.md
└── assets/
    └── screenshots/
```

---

## 06 Auto SKIT Report

**Folder:** `06_Auto_SKIT_Report/`  
**Tool:** Power Query · Excel  
**Type:** Lean Improvement Project #3 — formally submitted Dec 18, 2025

### What It Solves
The SKIT (Shipment Kit) report for the NAM region was prepared manually in 35 minutes daily — cross-referencing delivery numbers, container assignments, and port pickup dates across multiple sources. Copy-paste errors caused PGI processing delays.

### What It Does
Power Query automation that:
- Consolidates shipment delivery numbers, container numbers, and B/L data from multiple source files
- Tracks port pickup dates and send-for-PGI timestamps per shipment
- Flags shipments pending PGI processing
- Maintains a running volume log of processed SKIT-PGI records with remarks
- Produces the full NAM SKIT report in 5–6 minutes vs. 35 minutes

### Lean Impact (Formally Documented)
| Metric | Value |
|--------|-------|
| Time saved per day | ~29 minutes |
| Time saved per year | 130.5 hours |
| Submitted to | SCM Leadership — Subodh Kumar, Vimal Kumar |
| Date | 18 December 2025 |

### Files in This Folder
```
06_Auto_SKIT_Report/
├── SKIT_COA_Query_SAMPLE.xlsx
├── README.md
└── assets/
    └── screenshots/
```

---

## 07 Auto COA Report

**Folder:** `07_Auto_COA_Report/`  
**Tool:** Power Query · Excel  
**Type:** Lean Improvement Project #4 — formally submitted Dec 18, 2025

### What It Solves
Certificate of Analysis (COA) document tracking for US-bound agrochemical containers was done manually in ~10 minutes daily. Missing COAs flagged late caused port pickup delays — a compliance and cost risk.

### What It Does
Power Query automation that:
- Cross-references COA document availability against active delivery numbers and container numbers
- Flags any shipment where COA is pending before port pickup date
- Generates a clean COA status report in 1–2 minutes vs. 10 minutes
- Integrates with the SKIT query file for a unified NAM-region document status view

### Lean Impact (Formally Documented)
| Metric | Value |
|--------|-------|
| Time saved per day | ~8–9 minutes |
| Time saved per year | 43.5 hours |
| Critical function | Prevents port pickup delays from missing COA |
| Submitted to | SCM Leadership — Subodh Kumar, Vimal Kumar |
| Date | 18 December 2025 |

### Files in This Folder
```
07_Auto_COA_Report/
├── SKIT_COA_Query_SAMPLE.xlsx
├── README.md
└── assets/
    └── screenshots/
```

---

## Proof of Work — Lean Project Submissions

These projects were formally submitted to Supply Chain leadership as Lean Improvement initiatives while employed as Executive – Global Logistics. They are not retrospective portfolio additions.

| Project | Lean # | Submitted To | Date |
|---------|--------|-------------|------|
| Daily Container Status Tracker | #2 | Madhuri Jadhav (SCM Manager), Vishal Pahlajani (SCM Lead) | Dec 22, 2025 |
| Auto SKIT Report | #3 | Subodh Kumar, Vimal Kumar (SCM Leadership) | Dec 18, 2025 |
| Auto COA Report | #4 | Subodh Kumar, Vimal Kumar (SCM Leadership) | Dec 18, 2025 |

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

All sample files use anonymized data. The following have been replaced with generic placeholders:
- Company and supplier names → AgroCo / AgriChem / AgriClient-XX
- Personnel names → Planner-A through H
- Product and chemical names → PRODUCT-A through P
- Container numbers → ABCDXXXXXXX
- B/L numbers → BL-XXXXX
- PO and order numbers → first 3 digits + XXX

Formula logic, Power Query M-code, VBA structure, and data relationships are preserved exactly as built in production.

---

## Contact

- **LinkedIn:** *(add)*
- **Email:** *(add)*
- **Live Demo (Power BI / Power Automate):** Available via screen-share — contact to schedule
