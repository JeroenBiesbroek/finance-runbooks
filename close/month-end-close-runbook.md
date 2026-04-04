# Month-End Close Runbook

**Owner:** Finance Lead

## When to use
Every month-end. Start at business day -5 relative to month-end.

## Prerequisites
- Access to Exact Online
- Close checklist from finance-templates
- Previous close package for reference

## Procedure

### Step 1: Initialize
1. Create close checklist for the period
2. Assign task owners
3. Confirm target close date with Finance Lead

### Step 2: Pre-Close

**2.1 Sales Invoice Sync**
1. Run sync report from finance-automation
2. Verify counts match between Zoho Books and Exact
3. Review pending/failed items
4. Resolve or defer exceptions (document each)

**2.2 Purchase Processing**
1. Verify no unprocessed purchase invoices in Exact
2. Follow up on outstanding approvals

**2.3 Bank Processing**
1. Verify all bank statements imported through month-end
2. Review and match unmatched items
3. Document items that cannot be matched

**2.4 Exception Review**
1. Review all open exceptions in GitHub
2. Determine which can be resolved before close
3. Document deferrals with justification

**2.5 Pre-Close Sign-Off**
1. Review with Finance Lead
2. Obtain sign-off

### Step 3: Controlled Close

**3.1 Recurring Entries**
1. Review recurring entry template for correctness
2. Post recurring entries
3. Verify amounts match expected

**3.2 Accruals and Deferrals**
1. Review accrual schedule
2. Post accruals with supporting documentation
3. Reverse prior period accruals if applicable

**3.3 Manual Journals**
1. Post each journal with support attached
2. Obtain Finance Lead approval per journal

**3.4 Fixed Assets**
1. Run depreciation calculation (preview first)
2. Review output for reasonableness
3. Post depreciation
4. Process additions/disposals with approval

**3.5 Controlled Close Sign-Off**
1. Review with Finance Lead
2. Obtain sign-off

### Step 4: Review Close

**4.1 Financial Reviews**
1. Balance sheet: review each account
2. P&L: compare to budget and prior period, explain variances
3. VAT reconciliation
4. Bank balance reconciliation
5. Debtor and creditor balance reviews

**4.2 Control Review**
1. Complete control checklist
2. Document any control failures

**4.3 Review Close Sign-Off**
1. Compile results, escalate unresolved issues
2. Obtain Finance Lead sign-off

### Step 5: Final Close

1. Finance Lead approval
2. CFO approval (if required)
3. Close period in Exact Online → verify status = "Closed"
4. Archive close package
5. Document lessons learned
6. Create improvement issues in GitHub if applicable

## Troubleshooting

| Issue | See |
|---|---|
| Sync exceptions | [Sales Invoice Sync Runbook](../exceptions/sales-invoice-sync-runbook.md) |
| Bank exceptions | [Bank Exception Runbook](../exceptions/bank-exception-runbook.md) |
| Journal errors | [Journal Handling Runbook](../operations/journal-handling-runbook.md) |
| Depreciation issues | [Fixed Asset Runbook](../operations/fixed-asset-control-runbook.md) |
