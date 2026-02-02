## Use Case: Record Invoice Payment

**Primary Actor:** Office Administrator  
**Goal:** Record a payment against an issued invoice

**Preconditions:**
- Project exists
- Invoice has been created

**Main Flow:**
1. User selects the related invoice
2. User enters payment date and amount
3. System validates the entry
4. Outstanding balance updates automatically

**Postconditions:**
- Invoice balance is reduced
- Project financial KPIs update

**Exceptions:**
- Payment exceeds invoice amount → validation error

# Use Case Specifications – Excel Project Control System

These use cases describe how key roles interact with the system. They are written
to align business needs, process flows, and Excel sheet design.

---

## UC-01 Maintain Projects
**Primary Actor:** Project Manager  
**Goal:** Create or update project records so progress and financial tracking remains accurate.

**Preconditions**
- Project is approved to start OR existing project requires update.

**Main Flow**
1. Actor adds/updates Project details (ProjectID, client, status, contract value, dates, progress).
2. System validates required fields and allowed status values.
3. System updates project-level KPIs and dashboard rollups.

**Postconditions**
- Project record is current and visible in reporting.

**Exceptions**
- Missing required fields → system prompts correction.
- Invalid status value → system rejects entry.

**Related Sheets**
- Projects, Dashboard

---

## UC-02 Create Invoices
**Primary Actor:** Office Administrator  
**Goal:** Create an invoice linked to a project for billing and receivables tracking.

**Preconditions**
- Project exists and is active.

**Main Flow**
1. Actor creates an invoice record (InvoiceID, ProjectID, date, amount).
2. System validates ProjectID and invoice amount.
3. System updates outstanding balance and dashboard receivables KPIs.

**Postconditions**
- Invoice is tracked and contributes to receivables metrics.

**Exceptions**
- ProjectID not found → system rejects entry.
- Invoice amount ≤ 0 → validation error.

**Related Sheets**
- Invoices, Dashboard

---

## UC-03 Record Payments
**Primary Actor:** Office Administrator  
**Goal:** Record a received payment against an invoice to keep balances accurate.

**Preconditions**
- Invoice exists and has an outstanding balance.

**Main Flow**
1. Actor enters payment (PaymentID, InvoiceID, date, amount).
2. System validates InvoiceID and confirms payment does not exceed outstanding balance.
3. System updates invoice status, outstanding balance, and project KPIs.
4. Dashboard refreshes KPI values.

**Postconditions**
- Payment is recorded and receivables reflect the new balance.

**Exceptions**
- Payment amount > outstanding balance → validation error.
- Invoice already closed/paid → system blocks entry.

**Related Sheets**
- Payments, Invoices, Dashboard

---

## UC-04 Track Expenses
**Primary Actor:** Office Administrator  
**Goal:** Capture project expenses to support margin tracking and profitability analysis.

**Preconditions**
- Project exists.

**Main Flow**
1. Actor enters expense (ExpenseID, ProjectID, date, amount, category).
2. System validates ProjectID and amount.
3. System updates project profitability KPIs and dashboard rollups.

**Postconditions**
- Expenses contribute to project-level and portfolio-level margin metrics.

**Exceptions**
- Category missing/invalid → system prompts correction.
- Amount ≤ 0 → validation error.

**Related Sheets**
- Expenses, Dashboard

---

## UC-05 Manage Change Orders
**Primary Actor:** Project Manager  
**Goal:** Track scope/value changes and keep contract value and KPIs current.

**Preconditions**
- Project exists.

**Main Flow**
1. Actor submits a change order (ChangeOrderID, ProjectID, amount, description, status).
2. Owner/Manager reviews and approves/rejects.
3. If approved, system updates contract value and recalculates KPIs.

**Postconditions**
- Approved change orders are reflected in contract value and reporting.

**Exceptions**
- Change order rejected/deferred → no contract change is applied.

**Related Sheets**
- Change Orders, Projects, Dashboard

---

## UC-06 Review Dashboard & KPIs
**Primary Actor:** Owner / Manager  
**Goal:** Review portfolio KPIs for decision-making.

**Preconditions**
- Project, invoice, payment, expense, and change order data exists.

**Main Flow**
1. Actor opens dashboard.
2. Actor filters by time period and/or project status (if available).
3. Actor reviews KPIs (cash flow, outstanding invoices, progress, margin).

**Pos**
