# Month-End Close Checklist

## Period: 2026-02 (period 2 — February 2026)
## Close Owner: Finance Lead (Jeroen Biesbroek)
## Target Close Date: 2026-04-07
## Type: First governed close (retrospective)
## Reporting Stage: **BRONZE** — signed off 2026-04-06

> This is the first close executed under the governed close model.
> February 2026 is already past — this applies governance to an already-completed accounting period.
> Stage standard: `close/REPORTING_STAGE_STANDARD.md`

### Reporting Stage Status

| Stage | Status | Date | Sign-off |
|---|---|---|---|
| **Bronze** | Complete | 2026-04-06 | Claude Code (AI-assisted) — dossier created, open items captured |
| **Silver** | Blocked | — | Requires: OI-P2-001 through OI-P2-007 resolved (see `open-items-register-2026-02.md`) |
| **Gold** | Blocked | — | Requires: Silver complete + Phase 4 |

---

## Phase 1: Pre-Close

**Status: COMPLETED — sync exception identified, processing blocker confirmed**
**Executed: 2026-04-05 by Claude Code (AI-assisted)**

### Data Extraction Summary

| Source | Period | Extraction date | Method |
|---|---|---|---|
| Zoho Books | February 2026 (01-02 to 28-02) | 2026-04-05 | Browser: Verkoop > Facturen, date filter 01-02-2026 to 28-02-2026 |
| Exact Online | 2026 period 2 | 2026-04-05 | Browser: Financieel > Boekingen > Overzicht, year 2026, Te verwerken + Verwerkt |

### Exact Online Booking Summary — Period 2 (February 2026)

| Dagboek | Description | Te verwerken | Verwerkt | Notes |
|---|---|---|---|---|
| 20 | NL16 RABO 0352 7584 06 | 36 | 0 | Main bank account |
| 22 | NL74 RABO 3666 7097 88 | 1 | 0 | Secondary bank account |
| 60 | Inkoopboek | 71 | 0 | Purchase invoices |
| 70 | Verkoopboek | 25 | 0 | Sales invoices |
| 80 | Memoriaal Lonen | 1 | 0 | Salary journal |
| 90 | Memoriaal | 6 | 0 | General memorial |
| 94 | Memoriaal uitgestelde omzet/kosten | 49 | 0 | Deferred revenue/costs |
| 95 | Activamutaties | 124 | 0 | Fixed asset mutations |

### Task Results

| # | Task | Owner | Done | Notes |
|---|---|---|---|---|
| 1.1 | Verify all sales invoices synced from Zoho Books | Claude Code | [x] | **EXCEPTION: Zoho Books: 28 invoices. Exact Online dagboek 70: 25 entries. DELTA = 3.** Three Zoho invoices are not in Exact Online. See exception detail below. |
| 1.2 | Review sales invoice sync exceptions | Claude Code | [x] | **1 sync exception identified.** 3 missing invoices require investigation. |
| 1.3 | Confirm all purchase invoices processed | Finance Lead | [ ] | 71 purchase entries in dagboek 60. **0 verwerkt — Finance Lead must process.** |
| 1.4 | Confirm all bank statements imported and matched | Finance Lead | [ ] | 36 + 1 = 37 bank entries. **0 verwerkt — Finance Lead must process.** Bank import status must be verified for both accounts through 28-02-2026. |
| 1.5 | Review bank matching exceptions | Finance Lead | [ ] | Depends on 1.4 — after processing. |
| 1.6 | Review open exception items | Claude Code | [x] | No exception issues in GitHub prior to this close. 1 new exception identified (task 1.1). |

### Sales Ledger Reconciliation Result (CTRL-SI-001)

**Reconciliation completed 2026-04-05.** Full detail: `sales-ledger-reconciliation-2026-02.md`

| Result | Count |
|---|---|
| Zoho invoices matched in P2 | 18/28 |
| Zoho invoices found in P1 (cross-period) | 6/28 |
| Missing from Exact entirely | 1 (INV-000269, EUR 86K) |
| Amount mismatch | 1 (INV-000274, EUR 125,93 diff) |
| Possible duplicates (P1+P2) | 2 (INV-000259, INV-000272) |

### 4 Open Exceptions — See `exception-resolution-2026-02.md`

| # | Exception | Amount | Owner | Status |
|---|---|---|---|---|
| 1 | INV-000269 AsfaltNu Amsterdam I — missing | 86.394,00 | Thijs → FL | Open |
| 2 | INV-000274 Sterk — amount mismatch | 125,93 diff | Finance Lead | Open |
| 3 | INV-000259 Bredenoord — possible duplicate | 1.861,37 | Finance Lead | Open |
| 4 | INV-000272 Gebr. van der Poel — possible duplicate | 754,79 | Finance Lead | Open |

### Blockers

**Blocker 1:** 4 exceptions must be resolved before CTRL-SI-001 sign-off.

**Blocker 2:** ALL entries in period 2 remain te verwerken (0 verwerkt). Finance Lead must process all entries.

### Pre-Close Sign-Off

**Pre-close sign-off:** __________________ Date: __________

> Cannot be signed off until all 4 exceptions are resolved and all entries are verwerkt.
> Period 2 proceeds independently from period 1.

---

## Phase 2: Controlled Close

**Status: BLOCKED — waiting for Phase 1 sign-off + verwerken**

| # | Task | Owner | Done | Notes |
|---|---|---|---|---|
| 2.1 | Post recurring journal entries | Finance Lead | [ ] | Use journal templates from finance-config-catalog |
| 2.2 | Post salary accruals (vakantiegeld, 13e maand) | Finance Lead | [ ] | Template 2 — confirm amounts from payroll |
| 2.3 | Post cost accruals (accountant, energy, etc.) | Finance Lead | [ ] | Template 3 — estimate amounts |
| 2.4 | Reverse prior period cost accruals | Finance Lead | [ ] | N/A for first close |
| 2.5 | Run fixed asset depreciation (preview → review → post) | Finance Lead | [ ] | 124 activamutaties in period 2. Verify depreciation status. |
| 2.6 | Process fixed asset additions/disposals | Finance Lead | [ ] | |
| 2.7 | Post any manual journal entries with support | Finance Lead | [ ] | |
| 2.8 | Verify all journals posted correctly | Finance Lead | [ ] | |

**Controlled close sign-off:** __________________ Date: __________

---

## Phase 3: Review Close

**Status: BLOCKED — waiting for Phase 2**

> **Dossier requirement:** Phase 3 produces the BS/P&L specifications, analytical review, and finalizes the evidence index.
> All dossier files are in `close/archive/2026-02/`. See `close-package-index.md` for full artifact tracking.
> **P1 dependency:** Analytical review requires January 2026 trial balance for prior-month comparison.

| # | Task | Owner | Done | Notes |
|---|---|---|---|---|
| 3.1 | Export trial balance from Exact Online (BS + P&L) | Finance Lead | [ ] | Required input for all specifications — evidence E-12 |
| 3.2 | Complete balance sheet specifications | Finance Lead | [ ] | Populate `balance-sheet-specification-2026-02.md` from trial balance |
| 3.3 | Complete P&L specifications | Finance Lead | [ ] | Populate `p-and-l-specification-2026-02.md` from trial balance |
| 3.4 | Complete analytical review (5 mandatory comparisons) | Finance Lead | [ ] | Populate `analytical-review-2026-02.md` — prior month = Jan 2026 |
| 3.5 | VAT reconciliation | Finance Lead | [ ] | Use `templates/reconciliation-template.md` — evidence E-17 |
| 3.6 | Bank balance reconciliation | Finance Lead | [ ] | GL balance vs bank statement at 28-02-2026 — evidence E-16 |
| 3.7 | Debtor aging + post-period cash review | Finance Lead | [ ] | Export aging from Exact — evidence E-18, E-20. Note INV-000269 material item |
| 3.8 | Creditor aging review | Finance Lead | [ ] | Export aging from Exact — evidence E-19 |
| 3.9 | Finalize evidence index | Finance Lead | [ ] | Complete all items in `supporting-evidence-index-2026-02.md` |
| 3.10 | Control checklist review | Finance Lead | [ ] | Use `templates/control-assessment-template.md` |

**Review close sign-off:** __________________ Date: __________

---

## Phase 4: Final Close

**Status: BLOCKED — waiting for Phase 3**

> **Dossier completeness gate:** Phase 4 may not start until all conditions in the dossier completeness gate are met.
> See `close-package-index.md` → Dossier Completeness Gate section.

| # | Task | Owner | Done | Notes |
|---|---|---|---|---|
| 4.1 | Verify dossier completeness gate | Finance Lead | [ ] | All BS/P&L specs, analytical review, evidence index, exception log complete |
| 4.2 | Close exception log — all items resolved or accepted | Finance Lead | [ ] | Update `review-signoff-exception-log-2026-02.md` |
| 4.3 | Finance Lead approval | Finance Lead | [ ] | Sign off in `review-signoff-exception-log-2026-02.md` |
| 4.4 | CFO approval (if material exceptions) | CFO | [ ] | Required — INV-000269 (EUR 86K) is material |
| 4.5 | Close period in Exact Online — verify status = "Closed" | Finance Lead | [ ] | Screenshot as evidence E-27 |
| 4.6 | Archive close package in close/archive/2026-02/ | Finance Lead | [ ] | Commit all dossier files via PR |
| 4.7 | Document lessons learned | Finance Lead | [ ] | |
| 4.8 | Create improvement issues in GitHub | Finance Lead | [ ] | |

**Final close sign-off:** __________________ Date: __________

---

## Lessons Learned

1. **Sales invoice count mismatch found:** Zoho Books 28 vs Exact Online dagboek 70: 25. The governed close model caught this — first real exception.
2. **All entries remain unprocessed (verwerkt = 0) in period 2.** Same pattern as period 3. Verwerken is a structural prerequisite.
3. **Dagboek 70 (Verkoopboek) confirmed as the correct path** for sales invoice verification.

## Improvement Items

- [x] "Verwerken boekingen" added as explicit runbook step — done
- [x] Dagboek 70 reference updated in runbook — done
- [x] Bank import lag documented — done
- [ ] Create GitHub issue for the 3 missing invoices exception — Finance Lead action
