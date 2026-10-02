# TaxWise: Intelligent Tax Analysis, Forecasting & Compliance Platform

TaxWise is an enterprise-grade financial analytics and taxation SaaS platform engineered for **Junior Financial Analysts – Taxation** and corporate financial teams. It integrates statutory corporate tax calculation (Section 115BAA), time-series liability forecasting (OLS Linear Regression & Holt's Exponential Smoothing), compliance calendar tracking, risk intelligence matrix scoring, audit readiness preparation, and scenario planning.

---

## 🚀 Key Features & Connected Modules

### 1. Corporate Tax Calculation Engine
- **Statutory Formulaic Model**: Computes corporate tax liabilities under Section 115BAA baseline rate (22.0%), statutory surcharge (10.0%), and Health & Education Cess (4.0%), yielding an effective statutory rate of 25.17%.
- **Deduction Allocations**: Itemized allowable claims under Section 80JJAA (employment generation), Section 35(2AB) (in-house scientific R&D), and accelerated depreciation under Section 32(1)(iia).
- **Tax Credits Waterfall**: Full offset reconciliation against Advance Tax installments (Challan 280), TDS credits (Form 26AS), and Minimum Alternate Tax (MAT) credits.

### 2. Tax Strategy Simulator (Scenario Planning)
- **Side-by-Side Model Comparison**: Compare baseline operational strategies against optimized models with allowable depreciation write-offs and tax incentives.
- **Potential Difference Analytics**: Quantitative breakdown of tax liability reduction and effective tax rate (ETR) optimization with mandatory analytical disclaimers.

### 3. Time-Series Tax Liability Forecasting
- **Statistical Methodologies**: Select between Ordinary Least Squares (OLS) Linear Regression, Holt's Double Exponential Smoothing, and 3-Month Moving Averages.
- **Dynamic Horizons**: 3-Month, 6-Month, and 12-Month forward projection bands with 95% confidence bounds ($\pm 1.96$ standard errors).
- **CSV/XLSX Upload Engine**: Drag-and-drop trial balance upload with instant parsing, validation, and historical recalibration.

### 4. Statutory Compliance Center
- **Calendar & Threshold Tracker**: Tracks Advance Tax quarterly milestones (15%, 45%, 75%, 100%), monthly GST statements (GSTR-1, GSTR-3B), TDS quarterly returns (Form 26Q, 24Q), and Form 3CEB Transfer Pricing.
- **Penalty Risk Exposure**: Monitors Section 234C, Section 234E, and Section 47 statutory penalty exposure.
- **Document Metadata Attachment**: Upload and attach verification challans and reconciliation sheets.

### 5. Tax Risk Intelligence Matrix
- **Quantitative Scoring Model**: $\text{Risk Score} = \text{Probability (1–5)} \times \text{Financial Impact (1–5)}$ mapped to an interactive $5 \times 5$ severity matrix.
- **Exposure Vectors**: Catalog and track Transfer Pricing margins, GSTR-2B ITC mismatches, and Section 194J vs 194C classification disputes.

### 6. Tax Audit Readiness Center
- **9 Core Evidentiary Categories**: Pre-audit checklist covering Financial Statements, Tax Returns (ITR-6), Invoices, Expense Records, Bank Statements, Payroll Records, Tax Challans, Contracts, and Tax Notices.
- **Readiness Index Score**: Dynamic readiness percentage with category status tracking (Uploaded, Needs Review, Missing).

### 7. Tax Efficiency Analytics
- **Executive Ratios**: Effective Tax Rate (ETR), Tax-to-Revenue Ratio, Tax-to-Profit Ratio, Compliance Cost, Net Profit After Tax (NPAT).
- **Short-Term vs. Long-Term Roadmaps**: Clear distinction between immediate quarter operational tweaks and multi-year structural R&D incentives.

### 8. Transaction Management Ledger
- **Financial Ledger**: Date, Reference/Invoice No, Category, Inflow/Outflow amount, GST classification, Tax Withheld, Settlement status, and automated monthly rollups.

### 9. Executive Reporting Center
- **Formal Regulatory Reports**: Downloadable CSV and high-resolution print/PDF views for Tax Liability Audits, Forecast Projections, Compliance Status Schedules, and Audit Scorecards.

---

## 🛠️ Technology Stack

- **Frontend**: React 19, TypeScript, Tailwind CSS v4, Lucide Icons, Custom Responsive Financial SVG Charts
- **Backend**: Node.js, Express REST API, Native Crypto Salt & Hash
- **Computation**: Custom Financial Mathematical Engines for Section 115BAA & OLS Forecasting
- **Data Ingestion**: PapaParse CSV/XLSX Parser
- **State Management**: React Context with Persistent LocalStorage & In-Memory Backend Store

---

## 🏗️ Architecture & Project Structure

```
├── server/
│   ├── types.ts            # Domain entity interfaces & types
│   ├── store.ts            # Persistent store with pre-seeded demo data
│   ├── taxEngine.ts        # Section 115BAA & tax efficiency calculation formulas
│   ├── forecastEngine.ts   # OLS Linear Regression, Holt's, & Moving Average math
│   └── routes.ts           # Express REST API endpoints (/api/*)
├── src/
│   ├── components/
│   │   ├── charts/         # SVG financial charts (Revenue, ETR, Forecast, Matrix, Donut)
│   │   └── common/         # Navbar, Sidebar, ToastContainer, GlobalSearchModal, Modal
│   ├── context/
│   │   └── AppContext.tsx  # Central state, auth, dark mode, notifications, companies
│   ├── pages/              # Dashboard, Calculator, Planning, Forecasting, Compliance, etc.
│   ├── services/
│   │   └── api.ts          # Centralized fetch API client
│   ├── types.ts            # Client-side TypeScript definitions
│   ├── App.tsx             # Root router & layout wrapper
│   └── main.tsx            # React application entry point
├── server.ts               # Full-stack Express server mounting Vite dev middlewares
├── package.json
└── tsconfig.json
```

---

## 🔑 Demo Credentials

To explore the pre-populated enterprise environment:
- **Email**: `analyst@taxwise.io`
- **Password**: `Password123!`
- **Role**: Junior Financial Analyst – Taxation
- **Default Organization**: Apex Technologies Pvt. Ltd. (FY 2026-27, Revenue ₹12.4 Cr)
- *Or click "Launch Demo Dashboard" on the Sign In modal for 1-click instant access.*

---

## 🌐 REST API Documentation

| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `POST` | `/api/auth/login` | Authenticate user & issue session token |
| `POST` | `/api/auth/register` | Register new analyst account |
| `GET` | `/api/companies` | List all corporate entities |
| `POST` | `/api/companies` | Register new corporate entity |
| `GET` | `/api/dashboard/stats` | Aggregate KPI cards & interactive chart payloads |
| `POST` | `/api/tax/calculate` | Execute Section 115BAA corporate tax computation |
| `GET` | `/api/tax/scenarios` | Retrieve strategy simulator scenarios |
| `POST` | `/api/tax/scenarios` | Create / duplicate strategic scenario |
| `POST` | `/api/tax/forecast` | Run OLS / Exponential Smoothing time-series projection |
| `GET` | `/api/compliance` | List statutory compliance milestones & score |
| `POST` | `/api/compliance/:id/mark-complete` | Mark filing completed |
| `GET` | `/api/risks` | Retrieve risk catalog & 5x5 matrix metrics |
| `POST` | `/api/risks` | Catalog new tax risk profile |
| `GET` | `/api/audit` | Audit checklist documents & readiness index |
| `POST` | `/api/audit/upload` | Upload & verify audit documentation |
| `GET` | `/api/tax-efficiency` | Compute ETR, tax-to-revenue, and opportunity roadmap |
| `GET` | `/api/reports` | List generated executive reports |
| `POST` | `/api/reports` | Compile & save formal report |
| `GET` | `/api/search` | Global command palette search (Ctrl + K) |
| `POST` | `/api/demo/reset` | Reset demo dataset to default baseline |

---

## 💻 Environment Variables

Configure `.env` using `.env.example`:
```env
PORT=3000
JWT_SECRET="taxwise-secure-jwt-secret-key-production"
DATABASE_URL="file:./taxwise.db"
UPLOAD_DIR="./uploads"
```

---

## 🚀 Running Locally

```bash
# 1. Install dependencies
npm install

# 2. Run full-stack dev server (Express + Vite)
npm run dev

# 3. Build for production
npm run build

# 4. Run production server
npm start
```
