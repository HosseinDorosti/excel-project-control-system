User Stories – Excel Project Control System

These user stories translate business needs into implementable requirements and
align with the documented use cases, process flows, and data model.

Epic: Project Tracking
US-01 Create / Update Project

As a Project Manager
I want to create and update project records
So that progress, financials, and KPIs remain accurate.

Acceptance Criteria

Project must have a unique ProjectID

Status must be selected from a predefined list

Contract value must be greater than zero

Changes update dashboard KPIs automatically

US-02 Track Project Progress

As a Project Manager
I want to update project progress percentage
So that portfolio progress reflects actual completion.

Acceptance Criteria

Progress % must be between 0–100

Progress updates are reflected in dashboard rollups

Completed projects are excluded from “active” KPIs

Epic: Invoice Management
US-03 Create Invoice

As an Office Administrator
I want to create invoices linked to projects
So that billing and receivables can be tracked.

Acceptance Criteria

Invoice must reference an existing ProjectID

Invoice amount must be greater than zero

Invoice status defaults to “Submitted”

Outstanding balance updates automatically

US-04 View Outstanding Invoices

As an Office Administrator
I want to view outstanding invoices
So that I can prioritize follow-ups.

Acceptance Criteria

Outstanding invoices are clearly flagged

Fully paid invoices are excluded

Totals roll up to dashboard KPIs

Epic: Payment Recording
US-05 Record Payment

As an Office Administrator
I want to record payments against invoices
So that balances and cash flow are accurate.

Acceptance Criteria

Payment must reference an existing InvoiceID

Payment amount cannot exceed outstanding balance

Invoice status updates automatically

Dashboard KPIs refresh

US-06 Prevent Overpayment

As the System
I want to block payments exceeding invoice balance
So that data integrity is preserved.

Acceptance Criteria

Validation error shown for overpayment

No data is saved if validation fails

Epic: Expense Tracking
US-07 Record Project Expense

As an Office Administrator
I want to record expenses by project
So that profitability can be tracked.

Acceptance Criteria

Expense must reference an existing ProjectID

Amount must be greater than zero

Expense category is required

Margin KPIs update automatically

Epic: Change Order Management
US-08 Submit Change Order

As a Project Manager
I want to submit a change order
So that scope and value changes are tracked.

Acceptance Criteria

Change order must reference an existing ProjectID

Amount may be positive or negative

Status defaults to “Pending Approval”

US-09 Approve Change Order

As an Owner / Manager
I want to approve change orders
So that contract values and KPIs remain accurate.

Acceptance Criteria

Approved change orders update contract value

Rejected change orders do not affect financials

Dashboard KPIs recalculate automatically

Epic: Reporting & Dashboard
US-10 Review Portfolio KPIs

As an Owner / Manager
I want to review portfolio KPIs
So that I can make informed decisions.

Acceptance Criteria

KPIs reflect current project, invoice, payment, and expense data

Metrics update automatically without manual recalculation
