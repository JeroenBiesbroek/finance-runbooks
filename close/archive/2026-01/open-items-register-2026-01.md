# Open-Items Register

## Period: 2026-01 (period 1 — January 2026)
## Prepared by: Claude Code (AI-assisted)
## Date: 2026-04-06

---

## Purpose

Controlled register of all unresolved items for period 1's close. Every item has an owner, action, and stage-blocking classification. Items are resolved progressively as the period moves from Bronze → Silver → Gold.

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
| OI-P1-001 | IO260054 Sterk B.V. — manual dagboek 70 entry without Zoho origin | EUR 663,96 | Finance Lead | Confirm this is an authorized direct Exact entry | `blocks-silver` | Phase 1, CTRL-SI-001 | 2026-04-05 | Before Phase 1 sign-off |
| OI-P1-002 | 7 February invoices booked into Exact period 1 | EUR 15.167,92 | Finance Lead | Accept period 1 allocation, or rebook to period 2 | `blocks-silver` | Phase 1, CTRL-SI-001 | 2026-04-05 | Before Phase 1 sign-off |
| OI-P1-003 | Verwerken incomplete — 237 of 302 entries unprocessed (21.5% verwerkt) | N/A | Finance Lead | Process all remaining entries: Financieel > Boekingen > Verwerken, period 1 | `blocks-silver` | Phase 1, E-03 | 2026-04-05 | Before Phase 2 start |
| OI-P1-004 | Bank import confirmation — verify imports through 31-01-2026 for both accounts | N/A | Finance Lead | Check Exact Online: last import date per bank account >= 31-01-2026 | `blocks-silver` | Phase 1, E-02 | 2026-04-06 | Before Phase 1 sign-off |
| OI-P1-005 | Buse Gas B.V. exists in Exact but not in Zoho — direct-entry customer outside sync flow | EUR 1.612,24 (credit note) | Finance Lead | Decide: bring into Zoho or accept as permanent non-synced debtor | `carry-forward` | Phase 1, lesson #4 | 2026-04-05 | No deadline — policy decision |
| OI-P1-006 | Cross-period booking policy — February invoices systematically in period 1 | N/A | Finance Lead | Document cross-period allocation policy in operating model | `carry-forward` | Phase 1, lesson #3 | 2026-04-05 | No deadline — policy decision |

---

## Resolved Items

| ID | Description | Resolution | Resolved by | Date |
|---|---|---|---|---|
| — | No resolved items yet | — | — | — |

---

## Carry-Forward Items (to next period)

| ID | Description | Amount | Owner | Carried to period |
|---|---|---|---|---|
| OI-P1-005 | Buse Gas B.V. Zoho/Exact sync decision | EUR 1.612,24 | Finance Lead | Ongoing — not period-specific |
| OI-P1-006 | Cross-period booking policy | N/A | Finance Lead | Ongoing — not period-specific |

---

## Register Summary

| Classification | Count | Total amount |
|---|---|---|
| `blocks-silver` | 4 | EUR 15.831,88 + verwerken + bank confirmation |
| `blocks-gold` | 0 | — |
| `carry-forward` | 2 | N/A (policy decisions) |
| `resolved` | 0 | — |

---

## What Can Already Be Done Now (Bronze-Complete Tasks)

The following work is complete and does not depend on any open item:

| Task | Status | Evidence |
|---|---|---|
| Phase 1 data extraction (Zoho + Exact) | Done | Close checklist Phase 1 |
| Sales ledger reconciliation CTRL-SI-001 | Done — 20/20 Zoho matched, 9 extra explained | `sales-ledger-reconciliation-2026-01.md` |
| Dossier shell files created (BS, P&L, analytical, evidence index, exception log) | Done | All files in `close/archive/2026-01/` |
| Evidence index initialized with Phase 1 data | Done | `supporting-evidence-index-2026-01.md` |
| Exception log populated with all known items | Done | `review-signoff-exception-log-2026-01.md` |
| Open-items register created with all blockers documented | Done | This file |
| Close-package-index tracking all artifacts | Done | `close-package-index.md` |

**Register sign-off:** __________________ Date: __________
