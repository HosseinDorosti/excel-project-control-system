# Requirements – Excel Project Control System

This document summarizes the key functional and non-functional requirements and
maps them to diagrams and implementation areas.

---

## Functional Requirements (FR)

**FR-01 Project Tracking**
- Maintain project records with status, dates, contract value, and progress.
- Supports portfolio rollups and dashboard KPIs.
- Related: UC-01, Use Case Diagram

**FR-02 Invoice Management**
- Create invoices linked to ProjectID.
- Track invoice status and outstanding amount.
- Related: UC-02, Invoice-to-Cash Process

**FR-03 Payment Recording**
- Record payments linked to InvoiceID.
- Update balances, invoice status, and dashboard KPIs.
- Related: UC-03, Invoice-to-Cash Process

**FR-04 Expense Tracking**
- Record expenses linked to ProjectID and category.
- Support profitability/margin KPIs.
- Related: UC-04, Data Model

**FR-05 Change Order Management**
- Record change orders linked to ProjectID.
- Apply approved changes to contract value and recalculated KPIs.
- Related: UC-05, Change Order Process

**FR-06 Reporting & Dashboard**
- Present portfolio KPIs (cash flow, outstanding, progress, margin).
- Allow filtering by project status/time (if implemented).
- Related: UC-06, Dashboard

---

## Non-Functional Requirements (NFR)

**NFR-01 Usability**
- Non-technical users can add data and interpret KPIs quickly.

**NFR-02 Data Quality**
- Validation rules prevent invalid IDs, negative amounts, and invalid statuses.

**NFR-03 Protection & Integrity**
- Protect formulas and key calculation areas to prevent accidental edits.

**NFR-04 Maintainability**
- Structured tables and consistent IDs support scalability and future BI integration.
