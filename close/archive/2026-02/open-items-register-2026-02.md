# Open-Items Register

## Period: 2026-02 (period 2 — February 2026)
## Prepared by: Claude Code (AI-assisted)
## Date: 2026-04-06

---

## Purpose

Controlled register of all unresolved items for period 2's close. Every item has an owner, action, and stage-blocking classification. Items are resolved progressively as the period moves from Bronze → Silver → Gold.

## Classification Key

| Classification | Meaning |
|---|---|
| `blocks-silver` | Must be resolved before Silver reporting stage |
| `blocks-gold` | Must be resolved before Gold reporting stage |
| `carry-forward` | Does not block this period; carried to next period |
| `resolved` | Completed — moved to resolved section |

---

## Open Items

| ID | Description | Amount | Owner | Required action | Classification | Source | Created | Target |
|---|---|---|---|---|---|---|---|---|
| OI-P2-001 | INV-000269 AsfaltNu Amsterdam I — missing from Exact. Debtor does not exist. | EUR 86.394,00 | Thijs → Finance Lead | Create AsfaltNu Amsterdam I as debtor in Exact Online, then book invoice | `blocks-silver` | Phase 1, CTRL-SI-001, exception #1 | 2026-04-05 | Before Phase 1 sign-off |
| OI-P2-002 | INV-000274 Sterk B.V. — amount mismatch (Exact P1+P2 = 1.414,22 vs Zoho 1.540,15) | EUR 125,93 diff | Finance Lead | Investigate split across P1/P2, reconcile EUR 125,93 difference | `blocks-silver` | Phase 1, CTRL-SI-001, exception #2 | 2026-04-05 | Before Phase 1 sign-off |
| OI-P2-003 | INV-000259 Bredenoord B.V. — possible duplicate (P1 entry 26700032 + P2 entry 26700041) | EUR 1.861,37 | Finance Lead | Confirm correct period, remove duplicate entry in Exact | `blocks-silver` | Phase 1, CTRL-SI-001, exception #3 | 2026-04-05 | Before Phase 1 sign-off |
| OI-P2-004 | INV-000272 Gebr. van der Poel — possible duplicate (P1 entry 26700039 + P2 entry 26700043) | EUR 754,79 | Finance Lead | Confirm correct period, remove duplicate entry in Exact | `blocks-silver` | Phase 1, CTRL-SI-001, exception #4 | 2026-04-05 | Before Phase 1 sign-off |
| OI-P2-005 | Verwerken incomplete — 313 of 313 entries unprocessed (0% verwerkt) | N/A | Finance Lead | Process all entries: Financieel > Boekingen > Verwerken, period 2 | `blocks-silver` | Phase 1, E-03 | 2026-04-05 | Before Phase 2 start |
| OI-P2-006 | Bank import confirmation — verify imports through 28-02-2026 for both accounts | N/A | Finance Lead | Check Exact Online: last import date per bank account >= 28-02-2026 | `blocks-silver` | Phase 1, E-02 | 2026-04-06 | Before Phase 1 sign-off |
| OI-P2-007 | 6 February Zoho invoices found in Exact period 1 (cross-period) | N/A | Finance Lead | Confirm revenue allocation is intentional or rebook to period 2 | `blocks-silver` | Phase 1, CTRL-SI-001 | 2026-04-05 | Before Phase 1 sign-off |

---

## Resolved Items

| ID | Description | Resolution | Resolved by | Date |
|---|---|---|---|---|
| — | No resolved items yet | — | — | — |

---

## Carry-Forward Items (to next period)

| ID | Description | Amount | Owner | Carried to period |
|---|---|---|---|---|
| — | No carry-forward items yet | — | — | — |

---

## Register Summary

| Classification | Count | Total amount |
|---|---|---|
| `blocks-silver` | 7 | EUR 89.136,09 + verwerken + bank confirmation + cross-period allocation |
| `blocks-gold` | 0 | — |
| `carry-forward` | 0 | — |
| `resolved` | 0 | — |

---

## What Can Already Be Done Now (Bronze-Complete Tasks)

The following work is complete and does not depend on any open item:

| Task | Status | Evidence |
|---|---|---|
| Phase 1 data extraction (Zoho + Exact) | Done | Close checklist Phase 1 |
| Sales ledger reconciliation CTRL-SI-001 | Done — 18/28 matched P2, 6 in P1, 4 exceptions documented | `sales-ledger-reconciliation-2026-02.md` |
| Exception resolution detail prepared | Done | `exception-resolution-2026-02.md` |
| Dossier shell files created (BS, P&L, analytical, evidence index, exception log) | Done | All files in `close/archive/2026-02/` |
| Evidence index initialized with Phase 1 data | Done | `supporting-evidence-index-2026-02.md` |
| Exception log populated with all known items | Done | `review-signoff-exception-log-2026-02.md` |
| Open-items register created with all blockers documented | Done | This file |
| Close-package-index tracking all artifacts | Done | `close-package-index.md` |
| Phase 2 restart checklist prepared | Done | `phase2-restart-checklist.md` |

**Register sign-off:** __________________ Date: __________
