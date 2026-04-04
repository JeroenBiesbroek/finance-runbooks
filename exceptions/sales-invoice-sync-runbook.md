# Sales Invoice Sync Exception Runbook

**Owner:** Technical Lead

## When to use
When sales invoice sync reports exceptions, invoices are stuck in pending/failed status, or monitoring alerts trigger.

## Common exceptions

### E-01: Missing debtor mapping
**Symptom:** "debtor not found"
1. Look up customer in Zoho Books
2. Check if debtor exists in Exact Online
3. If exists: add mapping to `finance-config-catalog/mappings/debtor/`
4. If not: create debtor in Exact first, then add mapping
5. Re-run sync, verify posted

### E-02: Invalid VAT code
**Symptom:** "VAT code not found"
1. Check VAT rate on Zoho Books invoice
2. Look up correct Exact VAT code
3. If mapping missing: update `finance-config-catalog/mappings/vat/`
4. If rate wrong in Zoho: coordinate with sales team
5. Re-run sync

### E-03: Duplicate invoice
**Symptom:** "duplicate invoice number"
1. Look up invoice in both systems
2. True duplicate: mark as skipped with documentation
3. Re-issue: coordinate with Finance Lead

### E-04: GL account not found
**Symptom:** "GL account not found"
1. Check product category on invoice
2. Update account mapping or create account in Exact (Finance Lead approval)
3. Re-run sync

### E-05: API connection error
**Symptom:** Connection timeout or API error
1. Check Exact Online / Zoho Books API status
2. If temporary: auto-retry handles it (3 retries with backoff)
3. If prolonged: notify Technical Lead + Finance Lead
4. Re-run sync once restored

### E-06: Closed period
**Symptom:** "period is closed"
1. Confirm period status and invoice date
2. Options: post to next open period (document), or reopen period (Finance Lead + CFO)
3. Execute and document

## Monitoring
- Check sync status daily
- Review exception counts weekly
- Escalate if > 5 exceptions/day or any invoice stuck > 48h
