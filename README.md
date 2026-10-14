# ClinixOS — Intelligent Clinical & Hospital Management System

> An enterprise-grade Smart Hospital Management System (SHMS) built to automate clinical, nursing, pharmacy, and front-desk workflows.

---

## 🌟 Overview

ClinixOS replaces fragmented paper logs and siloed databases with a synchronized, real-time hospital operating platform. It provides role-based access for every staff member — from doctors and nurses to receptionists and pharmacists.

---

## 🚀 Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React 18 + TypeScript + Vite |
| Backend API | Node.js + Express + TypeScript |
| Database | SQLite |
| Real-Time | WebSocket |
| PDF Reports | PDFKit |
| Auth | JWT + bcrypt |

---

## 🛡️ Role-Based Portals

ClinixOS provides **6 secure role workspaces**, each with dynamic live data:

### 🔵 Admin Executive Hub
- Real-time Hospital KPIs (Bed Occupancy, ICU Vacancy, Revenue)
- Date filtering: Today / Last 7 Days / Current Month
- One-click automated PDF Report Generation

### 🟢 Ward Bed Manager (Nurse Station)
- Interactive visual bed grid — General, Semi-Private, ICU wards
- Live statuses: Vacant, Occupied, Cleaning, Maintenance
- ICU low-vacancy warning banner
- Dynamic bed admission & discharge workflows

### 🩺 Doctor Clinical Workspace
- Split-pane: Patient timeline + Diagnosis & Prescription pad
- ICD-10 Diagnostic Classification catalog with auto-suggest
- Multi-drug prescription builder with dosage/frequency/duration
- Doctor schedule & leave management

### 🏥 Receptionist Intake & Billing Desk
- Walk-in patient registration with auto-generated Patient IDs
- Appointment booking with conflict validation
- Itemized invoicing with multi-mode payment (Cash, Card, Online)
- Thermal receipt layout

### 💊 Pharmacy & Barcode Dispensing Console
- Barcode scanner integration
- Prescription fulfillment queue with automatic stock decrements
- Low-stock warnings and reorder alerts
- Inventory audit logs

### 👤 Patient Self-Service Portal
- Appointment booking with live doctor slot reconciliation
- Electronic prescription record access
- Invoice settlement and insurance claim logging
- Doctor consultation reviews & ratings

---

## 🧪 Test Suite

```bash
cd server
npm run test
```
Results: **7 PASSED, 0 FAILED** ✅

---

## 🔐 Demo Login Credentials

| Role | Email | Password |
|---|---|---|
| Admin | admin@clinixos.org | Admin@2026 |
| Doctor | doctor.cardio@clinixos.org | Doctor@2026 |
| Nurse | nurse@clinixos.org | Nurse@2026 |
| Receptionist | receptionist@clinixos.org | Recept@2026 |
| Pharmacist | pharmacist@clinixos.org | Pharma@2026 |
| Patient | patient.demo@clinixos.org | Patient@2026 |

---

## 🏃 Run Locally

```bash
# Install all dependencies
npm install

# Start backend (port 5000)
cd server && npm run dev

# Start frontend (port 3000)
cd client && npm run dev
```

---

## 📁 Project Structure

```
clinixos/
├── client/          # React frontend (Vite + TypeScript)
│   └── src/
│       ├── portals/ # Role-based dashboards
│       ├── components/
│       └── services/
├── server/          # Express backend (Node.js + TypeScript)
│   └── src/
│       ├── routes/
│       ├── database/
│       └── middleware/
├── shared/          # Shared clinical engine & types
└── tests/           # API & clinical engine tests
```

---

*ClinixOS — Built for real hospitals, real workflows.*
