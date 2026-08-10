# Supporting Evidence Index

## Period: 2026-02 (period 2 — February 2026)
## Prepared by: Claude Code (AI-assisted)
## Date: 2026-04-06

---

## Purpose

Central index of all evidence supporting the close dossier. Every specification and conclusion in the dossier must trace to evidence listed here.

## Evidence Register

### Phase 1 — Pre-Close Evidence

| # | Evidence item | Source | File / location | Status |
|---|---|---|---|---|
| E-01 | Sales ledger reconciliation (Zoho vs Exact dgb 70) | Claude Code + Finance Lead | `sales-ledger-reconciliation-2026-02.md` | Complete — 18 matched P2, 6 in P1, 4 exceptions |
| E-02 | Bank import confirmation per account | Exact Online dashboard | Pending — Finance Lead must verify import through 28-02-2026 | Not started |
| E-03 | Verwerken confirmation (0 te verwerken) | Exact Online Boekingen Overzicht | Pending — 313/313 entries unprocessed (0% verwerkt) | Blocked |
| E-04 | Exception register status | `exception-resolution-2026-02.md` | 4 open exceptions: INV-000269, INV-000274, INV-000259, INV-000272 | Open |
| E-05 | Pre-close sign-off | Close checklist | Pending — requires E-02, E-03, E-04 completed first | Not started |

### Phase 2 — Controlled Close Evidence

| # | Evidence item | Source | File / location | Status |
|---|---|---|---|---|
| E-06 | Journal listing for the period | Exact Online | Export / screenshot — after verwerken | Blocked by E-03 |
| E-07 | Depreciation preview output | Exact Online Activa module | 124 activamutaties in period 2, 0 verwerkt | Blocked by E-03 |
| E-08 | Depreciation posted confirmation | Exact Online | Depends on E-07 | Blocked |
| E-09 | Salary accrual calculation | Payroll data + template | Pending — Finance Lead prepares | Not started |
| E-10 | Cost accrual entries + basis | Journal entries | Pending — Finance Lead prepares | Not started |
| E-11 | Controlled close sign-off | Close checklist | Depends on E-06 through E-10 | Blocked |

### Phase 3 — Review Close Evidence

| # | Evidence item | Source | File / location | Status |
|---|---|---|---|---|
| E-12 | Trial balance (BS + P&L) | Exact Online | Export after Phase 2 completion | Blocked by Phase 2 |
| E-13 | Balance sheet specifications | Finance Lead | `balance-sheet-specification-2026-02.md` | Shell created — populate after E-12 |
| E-14 | P&L specifications | Finance Lead | `p-and-l-specification-2026-02.md` | Shell created — populate after E-12 |
| E-15 | Analytical review | Finance Lead | `analytical-review-2026-02.md` | Shell created — populate after E-12 |
| E-16 | Bank reconciliation | Finance Lead | Use `templates/reconciliation-template.md` | Blocked by Phase 2 |
| E-17 | VAT reconciliation | Finance Lead | Use `templates/reconciliation-template.md` | Blocked by Phase 2 |
| E-18 | Debtor aging report | Exact Online | Export after verwerken | Blocked by E-03 |
| E-19 | Creditor aging report | Exact Online | Export after verwerken | Blocked by E-03 |
| E-20 | Post-period cash collection data | Bank statements | First 10 BD after 28-02-2026 | Not started |
| E-21 | Asset register export | Exact Online | Export after depreciation run | Blocked by E-08 |
| E-22 | Payroll summary | Payroll provider | February 2026 payroll | Not started |
| E-23 | Control assessment results | Finance Lead | Use `templates/control-assessment-template.md` | Not started |
| E-24 | Review close sign-off | Close checklist | Depends on E-12 through E-23 | Blocked |

### Phase 4 — Final Close Evidence

| # | Evidence item | Source | File / location | Status |
|---|---|---|---|---|
| E-25 | Finance Lead approval | Close checklist | Depends on E-24 | Blocked |
| E-26 | CFO approval (if required) | Close checklist | Depends on E-25 | Blocked |
| E-27 | Period close confirmation | Exact Online | Screenshot: period 2 status = Closed | Blocked |
| E-28 | Lessons learned | Close checklist | 3 lessons documented in close checklist | Partial |
| E-29 | Exception log (final) | `review-signoff-exception-log-2026-02.md` | Initialized — 4 open items from Phase 1 | Partial |

---

## Current Blocking Chain

```
E-04 (4 exceptions) ──blocks──> E-05 (Pre-close sign-off)
E-03 (Verwerken) ──blocks──> E-06, E-07, E-18, E-19
E-04 + E-03 ──blocks──> Phase 2 start
Phase 2 ──blocks──> E-12 (Trial balance) ──blocks──> E-13, E-14, E-15
```

**Critical path:** Exception resolution (E-04) AND verwerken completion (E-03) are both required before any downstream dossier work.

**Additional P2-specific blocker:** INV-000269 AsfaltNu Amsterdam I (EUR 86.394) — debtor does not exist in Exact. Must be created before invoice can be booked. This is a pre-requisite to exception resolution.

---

## Completeness Check

| Check | Result |
|---|---|
| All Phase 1 evidence items completed | [ ] — E-02, E-03, E-04, E-05 pending |
| All Phase 2 evidence items completed | [ ] — Blocked |
| All Phase 3 evidence items completed | [ ] — Blocked |
| All Phase 4 evidence items completed | [ ] — Blocked |
| Every BS specification references evidence | [ ] — Shell created, not yet populated |
| Every P&L specification references evidence | [ ] — Shell created, not yet populated |
| Every analytical review explanation references evidence | [ ] — Shell created, not yet populated |
| No evidence gaps for material items (> EUR 10.000) | [ ] — INV-000269 (EUR 86.394) is material — requires individual evidence once booked |

**Evidence index sign-off:** __________________ Date: __________
