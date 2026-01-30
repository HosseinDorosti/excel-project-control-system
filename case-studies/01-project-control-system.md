# Excel Project Control System  
## Business Analysis Case Study

### 1. Executive Summary
This project demonstrates the design of a lightweight **Project Control System** built in Excel for small construction and service-based businesses.  
The solution centralizes project, invoice, payment, expense, and change order tracking while providing clear operational and financial KPIs.

---

### 2. Business Context & Problem
Small contractors often manage their operations using disconnected spreadsheets, emails, and paper invoices. This results in:
- delayed invoice follow-ups
- unclear payment and holdback status
- limited visibility into project profitability
- difficulty tracking project progress across multiple jobs

---

### 3. Objectives & Success Criteria
**Objectives**
- Centralize project financial and operational data
- Improve visibility into cash flow and profitability
- Reduce manual tracking and errors
- Enable faster decision-making using KPIs

**Success Criteria**
- Users can view project status and progress at a glance
- Outstanding invoices and overdue amounts are clearly visible
- Portfolio-level KPIs are automatically calculated

---

### 4. Stakeholders & Users
| Role | Needs |
|----|----|
| Owner / Manager | Profitability, cash flow, portfolio status |
| Office Admin | Invoicing, payment tracking |
| Project Manager | Project progress and follow-ups |

---

### 5. Scope Definition

**In Scope**
- Project tracking
- Invoice and payment management
- Expense tracking
- KPI dashboard
- Holdback and change order visibility

**Out of Scope**
- Payroll
- Tax filing
- External accounting system integration

---

### 6. Key Requirements

#### Functional Requirements
- Track projects with status and contract value
- Record invoices and payments per project
- Calculate remaining balance automatically
- Track expenses and gross margin
- Display KPIs at project and portfolio level

#### Non-Functional Requirements
- Easy to use for non-technical users
- Data validation to reduce errors
- Protected formulas to prevent accidental changes

---

### 7. Process Overview

**Current State (Before)**
- Manual tracking across multiple spreadsheets
- No centralized reporting
- High risk of missed follow-ups

**Future State (After)**
- Centralized Excel system
- Automated calculations
- Visual dashboards and alerts

---

### 8. Data Model (High Level)

**Core Tables**
- Projects
- Invoices
- Payments
- Expenses
- Change Orders

Each table uses a unique identifier (e.g., ProjectID) to maintain relationships and data integrity.

---

### 9. Solution Design Highlights
- Structured Excel tables with filters
- Drop-down lists for statuses
- Automated KPI calculations
- Dashboard summarizing portfolio performance
- Separation of input sheets and reporting sheets

---

### 10. Testing & Validation
- Formula validation using sample data
- Cross-checking totals between tables
- Scenario testing (completed vs active projects)

---

### 11. Risks & Mitigations
| Risk | Mitigation |
|----|----|
| User edits formulas | Sheet protection |
| Data inconsistency | Validation rules |
| Scalability limits | Defined data limits and guidance |

---

### 12. Future Enhancements
- Power BI integration
- Automated reminders
- Multi-user collaboration via SharePoint
- Version tracking

---

### 13. Key Skills Demonstrated
- Business requirements analysis
- Process modeling
- Data modeling
- KPI definition
- Excel solution design

