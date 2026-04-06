# Month-End Reporting Dossier Standard

**Owner:** Finance Lead
**Version:** v1.0 — 2026-04-06
**Status:** Active
**Applies to:** Every governed month-end close

---

## Purpose

This standard defines the minimum content, structure, and quality requirements for the month-end reporting dossier. The dossier is the evidence package that substantiates the financial position at period end. A close is not complete until the dossier meets this standard.

## Dossier Structure

| # | Component | Template | Mandatory | Preparer | Reviewer |
|---|---|---|---|---|---|
| 1 | Close cover / status sheet | Part of close checklist | Yes | Finance Lead | CFO (if required) |
| 2 | Balance sheet specifications | `templates/balance-sheet-specification-template.md` | Yes | Finance Lead | Finance Lead self-review + CFO for material items |
| 3 | P&L specifications | `templates/p-and-l-specification-template.md` | Yes | Finance Lead | Finance Lead self-review |
| 4 | Analytical review | `templates/analytical-review-template.md` | Yes | Finance Lead | Finance Lead |
| 5 | Supporting evidence index | `templates/supporting-evidence-index-template.md` | Yes | Finance Lead | Finance Lead |
| 6 | Review sign-off and exception log | `templates/review-signoff-and-exception-log-template.md` | Yes | Finance Lead | CFO (if material exceptions) |

## When Each Component Is Prepared

| Close phase | Dossier work |
|---|---|
| Phase 1 (Pre-close) | Evidence index started; sales ledger reconciliation completed |
| Phase 2 (Controlled close) | Journal evidence captured; depreciation output saved |
| Phase 3 (Review close) | BS/P&L specifications completed; analytical review completed; evidence index finalized |
| Phase 4 (Final close) | Review sign-off completed; exception log closed; dossier archived |

## Minimum Account Areas

### Balance Sheet — Mandatory Specifications

| Area | GL range | What must be substantiated | Blocks close if missing |
|---|---|---|---|
| Tangible fixed assets | 0xxx | Rollforward, investments, disinvestments, depreciation, invoice/contract support | Yes |
| Debtors | 1300-1399 | Aging, post-period cash review, major open items | Yes |
| Prepayments / accrued assets | 1450-1462 | Nature, release schedule, supporting contracts | Yes — if balance > EUR 5.000 |
| Bank | 1100-1199 | Reconciliation to bank statement | Yes |
| Creditors | 1600-1699 | Aging, disputed items, major open items | Yes |
| Tax / VAT | 1500-1599, 1700-1749 | Reconciliation to returns, open positions | Yes |
| Accrued liabilities | 1770-1899 | Nature, calculation basis, supporting evidence | Yes — if balance > EUR 5.000 |
| Equity / reserves | 0500-0999 | Movement explanation | Yes — if any movement |

### P&L — Mandatory Specifications

| Area | GL range | What must be substantiated | Blocks close if missing |
|---|---|---|---|
| Revenue | 8000-8999 | Month, YTD, prior month, prior year, component breakdown, variance explanations | Yes |
| Direct costs | 7000-7999 | Month, YTD, prior comparisons, material variances | Yes — if margin impact > 5% |
| Operating expenses | 4000-4999 | Month, YTD, prior comparisons, material variances | Yes |
| Depreciation | within 4400-4499 | Reconciliation to asset rollforward | Yes |
| Salary costs | 4000-4099 | Reconciliation to payroll, accruals | Yes |
| Unusual / manual items | Any | Full explanation with supporting evidence | Yes — always |

## Materiality Thresholds

| Threshold | Definition | Effect |
|---|---|---|
| Explanation threshold — BS | Balance > EUR 5.000 or change > EUR 2.500 | Must be specified and explained |
| Explanation threshold — P&L | Variance > 10% vs prior month OR > EUR 2.500 absolute | Must be explained in analytical review |
| Material item | Any single item > EUR 10.000 | Must have individual evidence |
| Close-blocking | Any unexplained balance or variance exceeding materiality | Blocks Phase 4 sign-off |

## Dossier Completeness Gate

The close cannot proceed to Phase 4 (Final Close) unless:
- [ ] All mandatory BS specifications completed
- [ ] All mandatory P&L specifications completed
- [ ] Analytical review completed with all material variances explained
- [ ] Evidence index complete — every specification references its evidence
- [ ] Exception log: all exceptions either resolved or accepted with documented justification
- [ ] Finance Lead sign-off on dossier completeness

## Archive

Each period's dossier is committed to `close/archive/YYYY-MM/` and includes:
- Completed close checklist
- Completed specifications (BS + P&L)
- Completed analytical review
- Completed evidence index
- Completed review sign-off and exception log
- All referenced evidence files (or links to Exact Online exports)
