# Bank Exception Runbook

**Owner:** Finance Lead

## When to use
When bank statements fail to import, transactions cannot be matched, reconciliation shows differences, or unmatched items are older than 5 business days.

## Common exceptions

### B-01: Statement import failure
1. Check file format (MT940 / CAMT.053)
2. Check for corruption or duplicate
3. Adjust import settings if needed
4. Re-attempt import

### B-02: Unmatched payment received
1. Search debtor in Exact, check open invoices
2. Partial payment: match with partial amount
3. Overpayment: match + create difference journal (Finance Lead approval)
4. Unknown debtor: investigate, create exception

### B-03: Unmatched payment made
1. Search creditor in Exact, check open purchase invoices
2. Match if found
3. If no match: investigate (pre-payment? direct debit?)
4. Book to appropriate account (Finance Lead approval)

### B-04: Bank balance mismatch
1. Generate reconciliation report
2. List all reconciling items
3. Timing differences: document and carry forward
4. Errors: correct in appropriate period
5. Unexplained: escalate to Finance Lead
6. Complete reconciliation template

### B-05: Duplicate transaction
1. Verify duplicate by comparing amount, date, reference
2. Reverse duplicate (Finance Lead approval)
3. Investigate root cause (double import?)

## Escalation
- Unmatched items > 5 business days → Finance Lead
- Balance mismatch > EUR 100 → Finance Lead
- Suspected fraud → Finance Lead + CFO immediately
