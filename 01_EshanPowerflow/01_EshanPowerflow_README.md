# 01 — EshanPowerflow: Document Routing & Approval Automation

[← Back to Portfolio](../README.md)

**Tool:** Microsoft Power Automate (Cloud Flow) · SharePoint · Microsoft Teams · Excel Online · AI Builder  
**Type:** Process Automation  
**Status:** ✅ Deployed in production

---

## Problem

Import-export logistics teams receive high-volume shipment documents — invoices, bills of lading, customs filings — that must be routed to the right department, reviewed, approved, and archived. The manual process required 3–5 hours of daily coordination, created compliance risk from misrouting, and had no audit trail.

---

## Solution

A scheduled Power Automate cloud flow that handles the entire pipeline without human intervention:

**Phase 1 — Trigger & File Detection**  
The flow runs on a recurrence schedule, scans a SharePoint Uploads library for new PDF files, and evaluates a condition gate. If no files exist, the flow terminates early — no wasted compute.

**Phase 2 — File Processing & Movement**  
When files are detected, the flow checks a SharePoint List to ensure no concurrent run is in progress (queue locking). It then retrieves file content, creates a copy in the Inward staging folder, deletes the original, compiles a file manifest using Select + Join transformations, and escalates to approval.

**Phase 3 — Approval Routing & Outcome Logging**  
A Teams approval notification is sent to designated approvers. The flow pauses and waits for a response:
- **Approved** → file moved to OUT folder, Teams channel notified, list status updated
- **Rejected** → nested For Each loop logs each file as a new row in the Excel audit table
---

## Step-by-Step Flow Walkthrough

| # | Action | Description |
|---|--------|-------------|
| 1 | Recurrence Trigger | Scheduled polling at defined intervals |
| 2 | Get Files – Uploads | Retrieves all files in SharePoint Uploads library |
| 3 | Initialize Variable | Sets process state tracking variable |
| 4 | Condition: PDF Available | Terminates run early if no valid files found |
| 5 | Get Items (List Free) | Checks SharePoint queue for slot availability |
| 6 | Condition: List Free | Prevents concurrent run conflicts |
| 7 | Update List: PROCESS | Locks the queue — marks slot as in-process |
| 8 | For Each – Move to Inward | Gets file content, creates Inward copy, deletes from Uploads |
| 9 | Get Files – IND | Retrieves file list from IND processing folder |
| 10 | Select + Join | Transforms file array into formatted manifest string |
| 11 | Start and Wait for Approval | Sends Teams approval request — flow pauses here |
| 12 | Condition 1 (Approval Result) | Branches on Approve / Reject |
| 13a | True Path — File to OUT | Moves file, posts Teams notification, updates item status |
| 13b | False Path — Log to Excel | Loops through files, adds each row to Excel audit log |
| 14 | Update Item Free | Releases queue lock for next run |
| 15 | Post Final Status | Sends summary Teams message regardless of outcome |

---

## Key Technical Concepts

- Recurrence triggers with early-exit condition logic
- SharePoint list-based queue locking (race-condition proof)
- Multi-approver async Teams approval with flow pause/resume
- Select + Join transformations for file manifest generation
- Nested For Each loops with Excel row-append operations
- State management across asynchronous approval pauses

---

## Business Impact

| Metric | Result |
|--------|--------|
| Manual coordination eliminated | 3–5 hrs/day |
| Document misrouting risk | Near zero — enforced by condition logic |
| Approval visibility | Real-time via Teams |
| Audit trail completeness | 100% logged — timestamp, approver, decision |
| Concurrent run safety | Race-condition proof via SharePoint list lock |

---

## How to Import and Run This Flow

1. Download [`EshanPowerflow_20260604181708.zip`](EshanPowerflow_20260604181708.zip)
2. Go to [Power Automate](https://make.powerautomate.com) → **My Flows** → **Import**
3. Upload the `.zip` file
4. Map connections: SharePoint, Microsoft Teams, Excel Online
5. Enable the flow

> **Requires:** Microsoft 365 license with Power Automate standard connectors
