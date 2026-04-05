# Phase 2 Restart Checklist — March 2026

**Purpose:** Confirm all prerequisites are met before starting the controlled close for March 2026.

## Prerequisites (all must be true)

| # | Prerequisite | How to verify | Status |
|---|---|---|---|
| 1 | All dagboek entries for period 3 processed | Financieel > Boekingen > Overzicht: year 2026, all dagboeken show 0 "Te verwerken" for period 3 | [ ] |
| 2 | Phase 1 pre-close signed off | Close checklist Phase 1 section has sign-off name + date | [ ] |
| 3 | Bank import complete through 31-03-2026 | Dashboard: both RABO accounts show "Bijgewerkt t/m" >= 31-03-2026 | [ ] |
| 4 | Journal templates amounts confirmed | finance-config-catalog/journals/journal-templates.md: expense GL accounts and estimated amounts filled in by Finance Lead | [ ] |

## Phase 2 Tasks with Evidence Requirements

| # | Task | Evidence to capture | Where to save |
|---|---|---|---|
| 2.1 | Post recurring journal entries | Journal listing from Exact for period 3, dagboek 90 | close/archive/2026-03/ |
| 2.2 | Post salary accruals | Journal entry with amounts, GL accounts used, calculation basis | close/archive/2026-03/ |
| 2.3 | Post cost accruals | Journal entry per accrual category, estimated amount + basis | close/archive/2026-03/ |
| 2.4 | Reverse prior period accruals | N/A for first close | — |
| 2.5 | Run fixed asset depreciation | Depreciation preview output (before posting) + posted confirmation | close/archive/2026-03/ |
| 2.6 | Process asset additions/disposals | Approval record per item (if any) | close/archive/2026-03/ |
| 2.7 | Manual journals | Each entry with supporting documentation attached | close/archive/2026-03/ |
| 2.8 | Verify all journals correct | Journal listing for period 3 — all dagboeken, verwerkt entries | close/archive/2026-03/ |

## Phase 2 Exit Criteria

- [ ] All recurring entries posted and verified against templates
- [ ] Salary accruals posted (or documented as N/A with reason)
- [ ] Cost accruals posted (or documented as N/A with reason)
- [ ] Depreciation run completed (preview reviewed, posted)
- [ ] All manual journals have attached support
- [ ] Finance Lead sign-off on controlled close

## After Phase 2

Commit all evidence to `close/archive/2026-03/` via PR. Then proceed to Phase 3 (Review Close).
