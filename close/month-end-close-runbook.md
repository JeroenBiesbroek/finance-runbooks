# Month-End Close Runbook

**Owner:** Finance Lead

## When to use
Every month-end. Start at business day -5 relative to month-end.

## Prerequisites
- Access to Exact Online
- Close checklist from [templates/close-checklist-template.md](../templates/close-checklist-template.md)
- Previous close package for reference

## Procedure

### Step 1: Initialize
1. Create close checklist for the period
2. Assign task owners
3. Confirm target close date with Finance Lead

### Step 2: Pre-Close

**2.1 Sales Invoice Sync**
1. Compare Zoho Books invoice count to Exact Online
   - Zoho Books: Verkoop > Facturen, filter by period dates
   - Exact Online: Financieel > Boekingen > Overzicht, filter dagboek **70 - Verkoopboek**, period. Count = "Aantal te verwerken boekingen" + "Aantal verwerkte boekingen"
   - *Note:* Sales invoices are entered via dagboek 70 (Verkoopboek), not the Verkoopfacturen module.
2. Verify counts match between Zoho Books and Exact
3. Review pending/failed items
4. Resolve or defer exceptions (document each)

**2.2 Purchase Processing**
1. Verify no unprocessed purchase invoices in Exact
2. Follow up on outstanding approvals

**2.3 Bank Processing**
1. Verify all bank statements imported through month-end
   - Check each bank account's last import date (dashboard shows "Bijgewerkt t/m")
   - *Known gap:* secondary bank account (NL74 RABO 3666 7097 88) may lag behind. If import date < period end, trigger manual import via Financieel > Bank en kas > Bankrekeningen > Afschriften > Import.
2. Review and match unmatched items
3. Document items that cannot be matched

**2.4 Exception Review**
1. Review all open exceptions in GitHub
   - *First governed close:* an empty exception register is expected. This step confirms no exceptions exist.
2. Determine which can be resolved before close
3. Document deferrals with justification

**2.5 Pre-Close Sign-Off**
1. Review with Finance Lead
2. Obtain sign-off

### Step 2.6: Process All Entries (Verwerken)

**Before starting the controlled close, all dagboek entries for the period must be processed.**

1. Go to Financieel > Boekingen > Verwerken
2. Select year and period
3. Process each dagboek:
   - 20 — Bank NL16 RABO
   - 22 — Bank NL74 RABO
   - 60 — Inkoopboek
   - 70 — Verkoopboek
   - 80 — Memoriaal Lonen
   - 90 — Memoriaal
   - 94 — Memoriaal uitgestelde omzet en kosten
   - 95 — Activamutaties
4. Verify: "Aantal te verwerken boekingen" = 0 for all dagboeken in the period
5. Document: total entries processed per dagboek

> **Gate:** Do not proceed to Step 3 until all entries show "Verwerkt". Unprocessed entries will not appear in trial balance, reconciliations, or financial reports.

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

**4.1 Reporting Dossier — Specifications**
1. Complete balance sheet specifications using `templates/balance-sheet-specification-template.md`:
   - Fixed asset rollforward (investments, disinvestments, depreciation)
   - Debtor aging + post-period cash collection review
   - Bank reconciliation (GL vs statement)
   - Creditor aging
   - VAT reconciliation (GL vs BTW-aangifte)
   - Prepayments and accrued liabilities with calculation basis
2. Complete P&L specifications using `templates/p-and-l-specification-template.md`:
   - Revenue by category (month, YTD, prior month, prior year)
   - Direct costs and gross margin
   - Operating expenses by category
   - Depreciation reconciliation to asset rollforward
   - Salary cost reconciliation to payroll
   - Unusual / manual items explained

**4.2 Reporting Dossier — Analytical Review**
1. Complete analytical review using `templates/analytical-review-template.md`
2. Explain all variances exceeding thresholds (> 10% AND > EUR 2.500 for P&L; > EUR 2.500 for BS)
3. Complete gross margin analysis and top-5 customer shift analysis

**4.3 Evidence and Exception Log**
1. Complete supporting evidence index using `templates/supporting-evidence-index-template.md`
2. Complete review sign-off and exception log using `templates/review-signoff-and-exception-log-template.md`
3. Resolve or accept all exceptions

**4.4 Control Review**
1. Complete control checklist
2. Document any control failures

**4.5 Review Close Sign-Off**
1. Verify dossier meets standard: `close/MONTH_END_REPORTING_DOSSIER_STANDARD.md`
2. Compile results, escalate unresolved issues
3. Obtain Finance Lead sign-off

### Step 5: Final Close

1. Finance Lead approval
2. CFO approval (if required)
3. Close period in Exact Online → verify status = "Closed"
4. Archive reporting dossier: save complete dossier (checklist, specifications, analytical review, evidence index, sign-off log) in `finance-runbooks/close/archive/YYYY-MM/` via PR
5. Document lessons learned
6. Create improvement issues in GitHub if applicable

## Troubleshooting

| Issue | See |
|---|---|
| Sync exceptions | [Sales Invoice Sync Runbook](../exceptions/sales-invoice-sync-runbook.md) |
| Bank exceptions | [Bank Exception Runbook](../exceptions/bank-exception-runbook.md) |
| Journal errors | [Journal Handling Runbook](../operations/journal-handling-runbook.md) |
| Depreciation issues | [Fixed Asset Runbook](../operations/fixed-asset-control-runbook.md) |
