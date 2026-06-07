# 02 — KPI Performance Dashboard

[← Back to Portfolio](../README.md)

**Tool:** Power BI · SharePoint · Microsoft Copilot  
**Type:** Management Reporting — Team Performance Accountability System  
**Status:** ✅ Deployed in production

---

## Problem

A logistics team of multiple planners had no real-time visibility into individual performance. Managers relied on end-of-week manual tallies — no drill-down capability, no audit trail on why targets were missed, and no way to identify patterns in SLA breaches without manually reviewing individual files.

---

## Solution

Each team member logs their daily transactions into an individual SharePoint file. Power BI connects to all files simultaneously, consolidates them into a unified data model, and surfaces a fully interactive performance command center.

[![KPI Dashboard Overview](assets/screenshots/dashboard_overview.png)](assets/screenshots/dashboard_overview.png)
*Add your screenshot here — dashboard overview*

---

## What the Dashboard Shows

### Individual & Team Filters
Slice the entire report by any team member, date range, or activity type. Switch between a full-team view and a focused single-person view in one click.

### Transaction Counts
Daily and cumulative activity volume per person — how many transactions were processed, when, and by whom.

### SLA Tracking — Hit / Miss Classification
Every task is automatically classified as **SLA Hit** or **SLA Missed** against defined completion thresholds. No manual flagging required — the logic runs on refresh.

### Root Cause Visibility
When an SLA is missed, the reason entered by the team member at the time of logging is visible directly in the dashboard. Managers see the "why" without any manual follow-up or chasing.

### Activity Log
Full chronological transaction log with timestamps per person — a complete audit trail of all activity within any selected period.

### Performance Scoring
Aggregated KPIs per team member based on three dimensions: volume (transactions processed), timeliness (completion vs. SLA), and accuracy (as tracked in the source logs).

---

## Data Architecture

```
SharePoint (Team Member Files)
    ├── Planner_A_Daily_Log.xlsx
    ├── Planner_B_Daily_Log.xlsx
    ├── Planner_C_Daily_Log.xlsx
    └── ... (one file per team member)
            ↓
    Power BI — Get Data → SharePoint Folder
            ↓
    Unified Data Model
    ├── Transactions table
    ├── SLA Rules table
    ├── Team Members dimension
    └── Date dimension
            ↓
    Dashboard — Filters / KPIs / Activity Log / Root Cause
```

---

## Key Technical Concepts

- Power BI connected to SharePoint folder — auto-picks up new team member files
- Dynamic slicers for team member, date range, and SLA status
- Conditional DAX logic for SLA Hit/Miss classification against per-activity thresholds
- Drill-through from summary KPI card to individual transaction-level activity log
- Microsoft Copilot integration — natural language querying of dashboard data
- Incremental refresh configuration for performance on large log datasets

---

## Why This Matters for AI in Supply Chain Roles

This is not a reporting tool. It is a **team accountability system with root-cause traceability** — the type of operational governance infrastructure a Supply Chain Transformation lead designs and deploys. Building it required understanding both the data pipeline and the management question being answered: not just "what happened" but "why did it miss, and who owns the fix."

---

## Files in This Folder

| File | Description |
|------|-------------|
| [🖼️ Screenshots](assets/screenshots/) | Power BI dashboard screenshots |

> **Note:** Power BI reports run inside an M365 organizational tenant and cannot be shared via public URL. Screenshots and a Loom walkthrough serve as portfolio artifacts. Live demo available on request via screen-share.
