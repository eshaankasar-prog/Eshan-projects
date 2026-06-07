# 03 — Cargodocs SaaS *(In Progress)*
> **Live app link:** *https://cargodocs.lovable.app/*

**Stack:** React · TypeScript · Supabase · TanStack Router · Lovable AI  
**Type:** Full-Stack Product Build  
**Status:** 🚧 In active development

---

## What It Is

Cargodocs is a logistics document management SaaS application built from scratch. It targets the same operational pain points solved manually in projects 04–07 of this portfolio — but as a product anyone can use, not an internal spreadsheet tied to one organisation's SharePoint.

---

## Why It Exists

Every project in this portfolio exposed the same underlying problem:

> Logistics teams manage critical documents — bills of lading, COAs, SKIT reports, container status — through a patchwork of spreadsheets, email threads, and manual cross-referencing. This breaks at scale, creates compliance risk, and eats hours that should go to higher-value work.

Projects 04–07 fixed that problem within one organisation using Power Query and Excel. Cargodocs is the answer at the product level — built to be deployable by any logistics or import-export operation, not just one team.

The difference between those projects and Cargodocs is the difference between **fixing a broken process** and **replacing it with infrastructure**.

---

## Technical Stack

| Layer | Technology | Purpose |
|-------|-----------|---------|
| Frontend | React + TypeScript | Component-based UI with full type safety |
| Routing | TanStack Router | File-based routing with type-safe navigation |
| Backend | Supabase | PostgreSQL database + Auth + Storage + Realtime |
| Build tool | Vite | Fast dev server and production bundler |
| AI-assisted build | Lovable AI | Accelerated scaffolding and component generation |

---

## Planned Feature Set

### Core Document Management
- Upload and store shipment documents (BLs, invoices, COAs, packing lists)
- Tag documents by shipment, container, or destination
- Status tracking — pending, in review, approved, archived

### Container & Shipment Tracking
- Link documents to specific containers and POs
- Track document availability before key milestones (port pickup, PGI, customs clearance)
- Flag missing documents automatically before deadline

### COA & SKIT Automation
- Auto-cross-reference COA availability against active delivery numbers
- Generate SKIT-style port pickup readiness reports on demand
- Replace the manual Power Query process from Project 06 with a live web interface

### Team Collaboration
- Role-based access — operations, documentation, management views
- Activity log per document and per user
- SLA flags on document submission deadlines

### AI Layer *(in design)*
- Document parsing — extract key fields (container number, ETD, HS code) from uploaded PDFs
- Anomaly detection — flag shipments with inconsistent or missing data patterns

---

## Current Build Status

- ✅ Project scaffolded — React + TypeScript + TanStack Router
- ✅ Supabase backend configured — auth and database schema in progress
- 🚧 Core document upload and management module — in development
- 🚧 Container-document linking — in design
- 🔲 COA cross-reference engine — planned
- 🔲 AI document parsing — planned

> **Live app link:** *https://cargodocs.lovable.app/*
