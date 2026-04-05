# Close Package Index — March 2026

**Period:** 2026-03
**Status:** In progress

This index tracks all required close-package artifacts for the March 2026 governed close.

## Required Artifacts

### Phase 1 — Pre-Close Evidence

| # | Artifact | Status | File/Location |
|---|---|---|---|
| 1.1 | Sales invoice sync count comparison (Zoho 29 = Exact 29) | Done | Documented in close-checklist-2026-03.md |
| 1.2 | Exception register status | Done | 0 exceptions (first close) |
| 1.3 | Bank import confirmation per account | Pending | Finance Lead captures after import completion |
| 1.4 | Verwerken confirmation (0 te verwerken) | Pending | Finance Lead captures after processing |
| 1.5 | Pre-close sign-off | Pending | Name + date in close checklist |

### Phase 2 — Controlled Close Evidence

| # | Artifact | Status | File/Location |
|---|---|---|---|
| 2.1 | Journal listing period 3 (all dagboeken, verwerkt) | Pending | Export from Exact Online |
| 2.2 | Depreciation preview + post confirmation | Pending | Screenshot or export from Exact |
| 2.3 | Salary accrual calculation + journal entry | Pending | Calculation basis + GL entry |
| 2.4 | Cost accrual entries + estimation basis | Pending | Per category: amount + basis |
| 2.5 | Controlled close sign-off | Pending | Name + date in close checklist |

### Phase 3 — Review Close Evidence

| # | Artifact | Status | File/Location |
|---|---|---|---|
| 3.1 | Balance sheet review notes | Pending | Per-account review notes |
| 3.2 | P&L analytical review (vs prior period) | Pending | Variance analysis with explanations |
| 3.3 | VAT reconciliation | Pending | Use templates/reconciliation-template.md |
| 3.4 | Bank reconciliation | Pending | Use templates/reconciliation-template.md |
| 3.5 | Debtor balance review | Pending | Aging analysis or balance confirmation |
| 3.6 | Creditor balance review | Pending | Aging analysis or balance confirmation |
| 3.7 | Control assessment results | Pending | Use templates/control-assessment-template.md |
| 3.8 | Review close sign-off | Pending | Name + date in close checklist |

### Phase 4 — Final Close Evidence

| # | Artifact | Status | File/Location |
|---|---|---|---|
| 4.1 | Finance Lead approval | Pending | Name + date in close checklist |
| 4.2 | CFO approval (if required) | Pending | Name + date |
| 4.3 | Period close confirmation from Exact Online | Pending | Screenshot: period status = "Closed" |
| 4.4 | Lessons learned | In progress | Documented in close checklist |

## Minimum Substantiation Standard

For this first governed close, the minimum acceptable substantiation per category:

| Category | Minimum evidence | Format |
|---|---|---|
| **Sales invoice completeness** | Count comparison Zoho vs Exact | Table in close checklist (done) |
| **Purchase completeness** | Confirmation all invoices processed | Note after verwerken |
| **Bank completeness** | Import date confirmation per account | Note with dates |
| **Journals** | Journal listing for the period | Export or screenshot from Exact |
| **Depreciation** | Preview output before posting | Screenshot from Exact |
| **Balance sheet** | Per-account review with notes on material balances | Notes in review section |
| **P&L** | Comparison to prior period, explain variances > 10% | Notes in review section |
| **VAT** | GL balance vs BTW-aangifte reconciliation | Completed reconciliation template |
| **Bank reconciliation** | GL balance vs bank statement balance | Completed reconciliation template |
| **Controls** | At minimum: CTRL-SI-001 (sync completeness) assessed | Control assessment template |

## Notes

- For the first governed close, the goal is to prove the process works and capture lessons — not to produce audit-grade documentation.
- Evidence quality will improve with each subsequent close cycle.
- All artifacts are committed to `close/archive/2026-03/` via PR.
