# ClinixOS — Intelligent Clinical & Hospital Management System
**Conforming to IEEE Std 830-1998 & HL7 v3 Healthcare Standards**

---

## 🌟 Executive Overview
**ClinixOS** is an enterprise-grade Smart Hospital Management System (SHMS) developed to automate clinical, nursing, pharmacy, and front-desk workflows. It replaces fragmented paper logs and siloed databases with a synchronized, real-time operating platform.

---

## 🚀 Live System Architecture
- **Frontend Client**: React 18 + TypeScript + Vite with **Glassmorphism** clinical design system.
  - **Local URL**: `http://localhost:3001`
- **Backend API Server**: Node.js + Express + TypeScript + SQLite/ANSI SQL Engine + PDFKit.
  - **REST API**: `http://localhost:5000/api`
  - **Real-Time WebSocket Telemetry**: `ws://localhost:5000/ws`

---

## 🛡️ Role-Based Portals & Functionality
ClinixOS features 6 distinct role workspaces with dynamic data and clean placeholders:

1. **Admin Executive Hub (`FR-06`, `FR-08`)**
   - Real-time Hospital KPIs (Bed Occupancy rate, ICU Vacancy %, Outpatient Visits today, Revenue).
   - Date filtering (`Today`, `Last 7 Days`, `Current Month`).
   - One-click Automated PDF Report Generation (Monthly Billing, Pharmacy Inventory Audit, Ward Census).
2. **Ward Bed Mapping & Live Telemetry (`FR-03`, `BR-03`)**
   - Interactive visual grid covering General, Semi-Private, and Intensive Care Units (ICU).
   - Live color statuses: 🟩 **Vacant**, 🟥 **Occupied**, 🟨 **Cleaning Needed**, 🟧 **Maintenance**.
   - Automatic ICU low vacancy warning banner (< 10%).
   - Business rule enforcement: prevents assigning beds marked as Cleaning or Maintenance.
3. **Doctor Clinical Workspace (`FR-01`, `FR-02`, `BR-02`)**
   - Split-pane interface: Patient clinical timeline on left, diagnosis and prescription pad on right.
   - Built-in **ICD-10 Diagnostic Classification catalog** with auto-suggest search.
   - Dynamic multi-item drug prescription builder (Dosage, Frequency, Duration, Quantity).
   - Verified digital doctor license signature.
   - Doctor schedule leave toggle (blocks appointment slots in real time).
4. **Receptionist Intake & Billing Desk (`FR-01`, `FR-02`, `FR-09`)**
   - Walk-in registration generating non-modifiable sequential Patient IDs (`PT-2026-0001`).
   - Conflict-validated appointment booking across operating hours (8:00 AM – 8:00 PM).
   - Anti-hoarding restriction: limits patients to max 2 active pending appointments.
   - Invoicing with itemized consultation, bed care, and medication costs.
   - Multi-mode payment recording (Cash, Card, Online) and thermal receipt printer layout.
5. **Pharmacy & Barcode Dispensing Console (`FR-05`, `Section 3.2`)**
   - Hardware USB Barcode scanner simulator.
   - Prescription fulfillment queue with automated stock decrements.
   - Critical low-stock visual warnings & WebSocket alerts.
   - Custom reorder threshold configuration & inventory audit logs.
6. **Patient Self-Service Portal (`FR-01.5`, `FR-02`)**
   - Self-service booking with live doctor slot reconciliation.
   - Electronic prescription record review.
   - Online invoice settlement & insurance claim logging.
   - Doctor consultation review & rating (1 to 5 stars).

---

## 🧪 Automated Test Suite
To run the automated IEEE 830 acceptance test suite:
```bash
cd server
node -e "require('ts-node/register'); require('../tests/api.test.ts')"
```
**Results**: `7 PASSED, 0 FAILED` (100% Pass Rate).
