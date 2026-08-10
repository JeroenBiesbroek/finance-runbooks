# Review Sign-Off and Exception Log

## Period: 2026-02 (period 2 — February 2026)
## Prepared by: Claude Code (AI-assisted)
## Date: 2026-04-06

---

## Dossier Completeness Review

| # | Dossier component | Complete | Notes |
|---|---|---|---|
| 1 | Close checklist (all 4 phases) | [ ] | Phase 1 completed; Phases 2-4 blocked by exceptions + verwerken |
| 2 | Balance sheet specifications | [ ] | Shell created — populate after trial balance available |
| 3 | P&L specifications | [ ] | Shell created — populate after trial balance available |
| 4 | Analytical review | [ ] | Shell created — populate after trial balance available |
| 5 | Supporting evidence index | [ ] | Initialized — Phase 1 partially filled |
| 6 | All evidence items present | [ ] | E-01 complete; E-02 through E-29 pending |

---

## Exception Log

### Open Exceptions

| # | Description | Amount | Area | Type | Owner | Required action | Deadline | Blocks close? |
|---|---|---|---|---|---|---|---|---|
| 1 | INV-000269 AsfaltNu Amsterdam I — missing from Exact (debtor does not exist) | EUR 86.394,00 | Sales ledger | `data-error` | Thijs → Finance Lead | Create AsfaltNu Amsterdam I as debtor in Exact, then book invoice | Before Phase 1 sign-off | Yes — CRITICAL, material item > EUR 10K |
| 2 | INV-000274 Sterk B.V. — amount mismatch between Zoho and Exact (split P1+P2) | EUR 125,93 diff | Sales ledger | `data-error` | Finance Lead | Investigate: Exact P1 (1.133,39) + P2 (280,83) = 1.414,22 vs Zoho 1.540,15. Reconcile difference | Before Phase 1 sign-off | Yes — blocks CTRL-SI-001 |
| 3 | INV-000259 Bredenoord B.V. — possible duplicate (same invoice in P1 entry 26700032 and P2 entry 26700041) | EUR 1.861,37 | Sales ledger | `data-error` | Finance Lead | Confirm which period is correct, remove duplicate entry | Before Phase 1 sign-off | Yes — blocks CTRL-SI-001 |
| 4 | INV-000272 Gebr. van der Poel — possible duplicate (same invoice in P1 entry 26700039 and P2 entry 26700043) | EUR 754,79 | Sales ledger | `data-error` | Finance Lead | Confirm which period is correct, remove duplicate entry | Before Phase 1 sign-off | Yes — blocks CTRL-SI-001 |
| 5 | Verwerken incomplete — 313 of 313 entries unprocessed | N/A | All dagboeken | `process-gap` | Finance Lead | Process all entries in Exact Online | Before Phase 2 start | Yes — blocks Phase 2 |

### Resolved Exceptions

| # | Description | Resolution | Resolved by | Date |
|---|---|---|---|---|
| — | No resolved exceptions yet | — | — | — |

### Accepted Exceptions (immaterial / deferred)

| # | Description | Amount | Justification | Accepted by | Date |
|---|---|---|---|---|---|
| — | No accepted exceptions yet | — | — | — | — |

---

## Review Notes

### Balance Sheet Review Notes

| Area | Reviewer note |
|---|---|
| Fixed assets | Not yet reviewed — 124 activamutaties unprocessed in dagboek 95 |
| Debtors | Partial — sales ledger reconciled (18/28 matched in P2, 6 in P1, 4 exceptions). INV-000269 EUR 86K missing — material item |
| Bank | Not yet reviewed — 37 bank entries unprocessed (dagboek 20: 36, dagboek 22: 1) |
| Creditors | Not yet reviewed — 71 unprocessed in dagboek 60 |
| VAT | Not yet reviewed — requires processed data |
| Accruals | Not yet reviewed — depends on Phase 2 journal entries |

### P&L Review Notes

| Area | Reviewer note |
|---|---|
| Revenue | Not yet reviewed — dagboek 70: 25 entries, 0 verwerkt. 6 Zoho invoices booked into P1 (cross-period) |
| Direct costs | Not yet reviewed — requires processed purchase data |
| Operating expenses | Not yet reviewed — requires processed memorial data |
| Depreciation | Not yet reviewed — 124 activamutaties unprocessed |
| Unusual items | No unusual items identified yet — review after verwerken |

### Analytical Review Notes

| Note |
|---|
| Analytical review for February 2026 will compare against January 2026 (prior month). January 2026 must be closed first or at minimum have a trial balance available for comparison. If Period 1 close is not complete, the analytical review can use preliminary January numbers but must note this limitation. |

---

## Sign-Off

### Phase 3 — Review Close Sign-Off

| Condition | Met? |
|---|---|
| All BS accounts reviewed and specified | [ ] |
| All P&L lines reviewed and specified | [ ] |
| Analytical review completed | [ ] |
| All material variances explained | [ ] |
| All reconciliations completed | [ ] |
| Exception log reviewed | [ ] |
| Evidence index complete | [ ] |

**Review close sign-off:** __________________ Date: __________

### Phase 4 — Final Close Sign-Off

| Condition | Met? |
|---|---|
| Review close signed off | [ ] |
| All close-blocking exceptions resolved or accepted | [ ] |
| Dossier complete per standard | [ ] |
| Finance Lead approval | [ ] |
| CFO approval (if required) | [ ] |

**Finance Lead approval:** __________________ Date: __________

**CFO approval:** __________________ Date: __________

---

## Lessons Learned

| # | Finding | Action | Owner |
|---|---|---|---|
| 1 | AsfaltNu Amsterdam I debtor missing from Exact — EUR 86K invoice cannot be booked without debtor record | Debtor creation in Exact is a prerequisite for invoice booking — add to pre-close checklist | Finance Lead |
| 2 | Cross-period invoices (6 February invoices in P1) create reconciliation complexity | Consider standardizing invoice period allocation rules | Finance Lead |
| 3 | 0% verwerkt at close start — no entries processed for entire period | Verwerken should ideally be ongoing, not batched at close time | Process improvement |
