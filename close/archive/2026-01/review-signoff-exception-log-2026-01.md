# Review Sign-Off and Exception Log

## Period: 2026-01 (period 1 — January 2026)
## Prepared by: Claude Code (AI-assisted)
## Date: 2026-04-06

---

## Dossier Completeness Review

| # | Dossier component | Complete | Notes |
|---|---|---|---|
| 1 | Close checklist (all 4 phases) | [ ] | Phase 1 completed; Phases 2-4 blocked by verwerken |
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
| 1 | IO260054 Sterk B.V. — manual dgb 70 entry without Zoho origin | EUR 663,96 | Sales ledger | `data-error` | Finance Lead | Confirm this is an authorized direct Exact entry | Before Phase 1 sign-off | Yes — blocks CTRL-SI-001 sign-off |
| 2 | 7 February invoices booked into Exact period 1 | EUR 15.167,92 | Sales ledger | `timing-difference` | Finance Lead | Accept period 1 allocation or rebook to period 2 | Before Phase 1 sign-off | Yes — blocks CTRL-SI-001 sign-off |
| 3 | Verwerken incomplete — 237 of 302 entries unprocessed | N/A | All dagboeken | `process-gap` | Finance Lead | Process all remaining entries in Exact Online | Before Phase 2 start | Yes — blocks Phase 2 |

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
| Fixed assets | Not yet reviewed — 121 activamutaties unprocessed in dagboek 95 |
| Debtors | Partial — sales ledger reconciled (20/20 Zoho matched), but debtor aging not yet available |
| Bank | Not yet reviewed — 47 bank entries unprocessed (dagboek 20: 45, dagboek 22: 2) |
| Creditors | Not yet reviewed — 22 unprocessed in dagboek 60 |
| VAT | Not yet reviewed — requires processed data |
| Accruals | Not yet reviewed — depends on Phase 2 journal entries |

### P&L Review Notes

| Area | Reviewer note |
|---|---|
| Revenue | Not yet reviewed — dagboek 70 partially processed (12 verwerkt, 17 te verwerken) |
| Direct costs | Not yet reviewed — requires processed purchase data |
| Operating expenses | Not yet reviewed — requires processed memorial data |
| Depreciation | Not yet reviewed — 121 activamutaties unprocessed |
| Unusual items | 1 known item: IO260054 Sterk manual entry (EUR 663,96) — pending confirmation |

### Analytical Review Notes

| Note |
|---|
| Analytical review cannot start until trial balance is available after Phase 2 completion. January 2026 is the first period — no prior month for P&L comparison. YTD = current month. Prior year (2025) comparison requires 2025 data from Exact. |

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
| 1 | Cross-period booking pattern (February invoices in period 1) is structural — needs conscious decision per close | Document cross-period policy in operating model | Finance Lead |
| 2 | Buse Gas B.V. exists in Exact but not in Zoho — direct-entry customers bypass sync flow | Decide: bring into Zoho or accept as permanent exception | Finance Lead |
| 3 | Period 1 partially processed (21.5%) before governed model applied — verwerken was not systematic | Governed model now requires 100% verwerken before Phase 2 | Already addressed |
