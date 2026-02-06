# Power BI – Project Financial Control Dashboard

## Overview
This Power BI dashboard provides an **executive-level financial overview** of multiple projects, focusing on invoicing, payments, expenses, profitability, and cash collection performance.

It is designed for:
- Project Managers
- Finance teams
- Executives needing quick financial insights

---

## Key Business Questions Answered
- How much have we **invoiced vs collected**?
- What is the **outstanding amount** across projects?
- Which projects are **most profitable**?
- How do **expenses and payments trend over time**?
- What is the **collection efficiency (%)**?

---

## Executive KPIs
- **Total Invoiced**
- **Total Paid**
- **Total Expenses**
- **Net Profit**
- **Outstanding Amount**
- **Collection Rate (%)** with conditional formatting

---

## Data Model
The model follows a **star schema** design:

- **Fact tables**
  - FactInvoices
  - FactPayments
  - FactExpenses
  - FactChangeOrders

- **Dimension tables**
  - DimProjects
  - DimDate

Surrogate keys (ProjectID, Date) are used to ensure clean relationships and scalability.

---

## Key DAX Measures
Some highlighted measures include:

```DAX
Outstanding Amount =
[Total Invoiced] - [Total Paid]
Collection Rate % =
DIVIDE([Total Paid], [Total Invoiced])

Net Profit =
[Total Invoiced] - [Total Expenses]
