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
