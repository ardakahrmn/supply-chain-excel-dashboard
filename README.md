# Supply Chain & Logistics Analytics Dashboard (Excel)

An interactive-style **Excel dashboard** that turns raw supply-chain shipment data into a clear, decision-ready view of **risk, delivery performance, inventory pressure, and logistics cost** — built entirely in Excel with a clean `Data → Calc → Dashboard` structure.

<img width="1199" height="700" alt="image" src="https://github.com/user-attachments/assets/176abcaf-5e23-42c8-90db-28d34dd800fa" />


---

## 📌 Overview

This project analyzes **4,000 shipment records** (sampled from a 113k-row logistics dataset) covering **965 products, 94 supplier countries, and 3,500+ suppliers**. The goal: take messy, transaction-level supply-chain data and surface the metrics an operations team actually needs to act on.

The dashboard answers questions like:
- How much of our shipping is **high risk**?
- Are deliveries arriving **on time**?
- Which products are **low on stock** and need reordering?
- How reliable are our suppliers, and how long is the average **lead time**?
- Does higher risk actually cost more?

---

## 🧱 How it's built (3-layer structure)

| Layer | Purpose |
|-------|---------|
| **Data** | Cleaned source table (`SupplyChain`) + a data dictionary. Rounded values, corrected column names. |
| **Calc** | All aggregations via `SUMIFS`, `COUNTIF`, `AVERAGEIFS` + helper flags (`IF`) + PivotTables for country breakdowns. |
| **Dashboard** | KPI cards + 6 charts, dark corporate theme, traffic-light colour logic. |

Nothing is hardcoded — every KPI and chart is formula-driven and updates if the source data changes.

---

## 📊 What's on the dashboard

**KPI cards:** On-Time Delivery %, High-Risk Share %, Reorder-Needed count, Avg Supplier Reliability, Avg Lead Time.

**Charts:**
- **Risk Distribution** (doughnut) — Low / Moderate / High
- **Top Countries by Shipments** (bar)
- **Stock Status** (doughnut) — Reorder vs OK
- **Shipping Cost by Risk** (column)
- **Delivery Performance** (doughnut) — On Time vs Late
- **Lead Time by Risk** (column)

---

## 🔑 Key insights

- **73% of shipments are classified High Risk** — risk is the dominant characteristic of this supply chain, not the exception.
- **Only ~18% of deliveries arrive on time** (target 90%). Late delivery — not cost — is the core operational problem.
- **~2,200 products sit below the reorder threshold**, signalling widespread inventory pressure.
- **Shipping cost shows little correlation with risk level** (Low ≈ Moderate ≈ High). Reducing risk here is unlikely to reduce cost — the levers are reliability and on-time performance, not spend.

> The story the data tells: this is a network where **reliability and on-time delivery are failing**, while cost stays flat regardless of risk. Fixing delivery performance and supplier reliability should take priority over cost-cutting.

---

## 🛠️ Skills demonstrated

- Excel formulas: `SUMIFS`, `COUNTIF`, `AVERAGEIFS`, `IF`, structured table references
- PivotTables for high-cardinality breakdowns (countries)
- Helper columns / flags (reorder, on-time) to turn raw numbers into categories
- Dashboard design: KPI cards, chart selection, colour logic, layout
- Data preparation: cleaning, rounding, renaming, right-sizing a large dataset
- Data storytelling: turning metrics into a clear operational narrative

---

## 📁 Files

- `SupplyChain_Dashboard.xlsx` — the workbook (Data, Calc, Dashboard sheets)
- `dashboard.png` — dashboard screenshot
- `README.md` — this file

---

## 📇 Data

Source: public supply-chain / logistics dataset (Kaggle). Sampled to 4,000 records and cleaned for analysis. All figures are illustrative.

---

**Built by Arda Kahraman** — Industrial Engineer · Data & BI
