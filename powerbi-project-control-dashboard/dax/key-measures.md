# Key DAX Measures (Highlights)

## Total Invoiced
Sum of invoice amounts.
```DAX
Total Invoiced = SUM ( FactInvoices[Net Invoice Amount] )
Total Paid = SUM ( FactPayments[PaymentAmount] )
Total Expenses = SUM ( FactExpenses[Amount] )
Net Profit = [Total Invoiced] - [Total Expenses]
Outstanding Amount = [Total Invoiced] - [Total Paid]
Collection Rate % = DIVIDE ( [Total Paid], [Total Invoiced] )
