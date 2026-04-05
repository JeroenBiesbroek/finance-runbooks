# Month-End Close Checklist

## Period: 2026-03
## Close Owner: Finance Lead (Jeroen Biesbroek)
## Target Close Date: 2026-04-07
## Type: First governed close (retrospective)

> This is the first close executed under the governed close model.
> March 2026 is already past — this applies governance to an already-completed accounting period.

---

## Phase 1: Pre-Close

**Status: IN PROGRESS — data verification completed, processing blocker identified**
**Executed: 2026-04-05 by Claude Code (AI-assisted)**

### Data Extraction Summary

| Source | Period | Extraction date | Method |
|---|---|---|---|
| Zoho Books | March 2026 (01-03 to 31-03) | 2026-04-05 | Browser: Verkoop > Facturen, date filter |
| Exact Online | 2026 period 3 | 2026-04-05 | Browser: Financieel > Boekingen > Overzicht |

### Exact Online Booking Summary — Period 3 (March 2026)

| Dagboek | Description | Te verwerken | Verwerkt | Notes |
|---|---|---|---|---|
| 20 | NL16 RABO 0352 7584 06 | 53 | 0 | Main bank account |
| 22 | NL74 RABO 3666 7097 88 | 2 | 0 | Secondary bank account |
| 60 | Inkoopboek | 83 | 0 | Purchase invoices |
| 70 | Verkoopboek | 29 | 0 | Sales invoices |
| 80 | Memoriaal Lonen | 1 | 0 | Salary journal |
| 90 | Memoriaal | 5 | 0 | General memorial |
| 94 | Memoriaal uitgestelde omzet/kosten | 35 | 0 | Deferred revenue/costs |
| 95 | Activamutaties | 122 | 0 | Fixed asset mutations |

### Task Results

| # | Task | Owner | Done | Notes |
|---|---|---|---|---|
| 1.1 | Verify all sales invoices synced from Zoho Books | Claude Code | [x] | **Zoho Books: 29 invoices. Exact Online dagboek 70: 29 entries. COUNT MATCHES.** Invoices entered via Verkoopboek (70), not Verkoopfacturen module. |
| 1.2 | Review sales invoice sync exceptions | Claude Code | [x] | First governed close — no exceptions in GitHub. Zero sync exceptions. |
| 1.3 | Confirm all purchase invoices processed | Finance Lead | [ ] | 83 purchase entries in dagboek 60. **0 verwerkt — Finance Lead must process.** |
| 1.4 | Confirm all bank statements imported and matched | Finance Lead | [ ] | 53 + 2 = 55 bank entries. **0 verwerkt — Finance Lead must process.** Bank imported through 03-04-2026 (main) and 23-03-2026 (secondary). |
| 1.5 | Review bank matching exceptions | Finance Lead | [ ] | Depends on 1.4 — after processing. |
| 1.6 | Review open exception items | Claude Code | [x] | No exception issues in GitHub. Empty register expected for first close. |

### Hard Blocker Identified

**ALL entries in Exact Online period 3 have status "Te verwerken" (0 verwerkt).** No entries have been processed for March 2026. This must be resolved before Phase 2 can begin.

**Required action by Finance Lead:**
1. Process (verwerken) all entries in dagboek 70 (verkoopboek) for period 3
2. Process all entries in dagboek 60 (inkoopboek) for period 3
3. Process all entries in dagboek 20 + 22 (bank) for period 3
4. Process entries in dagboek 80, 90, 94, 95 for period 3
5. After processing, verify no errors occurred

**Navigation in Exact Online:** Financieel > Boekingen > Verwerken

### Pre-Close Sign-Off

**Pre-close sign-off:** __________________ Date: __________

> Cannot be signed off until all dagboek entries are processed (verwerkt) by Finance Lead.

---

## Phase 2: Controlled Close

**Status: BLOCKED — waiting for Phase 1 processing**

| # | Task | Owner | Done | Notes |
|---|---|---|---|---|
| 2.1 | Post recurring journal entries | Finance Lead | [ ] | Use journal templates. Salary accruals: confirm amounts. |
| 2.2 | Post salary accruals (vakantiegeld, 13e maand) | Finance Lead | [ ] | Template 2 — amounts must be determined from payroll data |
| 2.3 | Post cost accruals (accountant, energy, etc.) | Finance Lead | [ ] | Template 3 — amounts must be estimated |
| 2.4 | Reverse prior period cost accruals | Finance Lead | [ ] | N/A for first close |
| 2.5 | Run fixed asset depreciation (preview → review → post) | Finance Lead | [ ] | 122 activamutaties already entered but 0 verwerkt. Check if depreciation run has been done. |
| 2.6 | Process fixed asset additions/disposals | Finance Lead | [ ] | |
| 2.7 | Post any manual journal entries with support | Finance Lead | [ ] | |
| 2.8 | Verify all journals posted correctly | Finance Lead | [ ] | |

**Controlled close sign-off:** __________________ Date: __________

---

## Phase 3: Review Close

**Status: BLOCKED — waiting for Phase 2**

| # | Task | Owner | Done | Notes |
|---|---|---|---|---|
| 3.1 | Balance sheet review — each account | Finance Lead | [ ] | |
| 3.2 | P&L review — compare to prior period | Finance Lead | [ ] | No budget loaded; compare to February 2026 |
| 3.3 | VAT reconciliation | Finance Lead | [ ] | Use templates/reconciliation-template.md |
| 3.4 | Bank balance reconciliation | Finance Lead | [ ] | Exact GL balance vs bank statement at 31-03-2026 |
| 3.5 | Debtor balance review | Finance Lead | [ ] | |
| 3.6 | Creditor balance review | Finance Lead | [ ] | |
| 3.7 | Variance analysis — explain material items | Finance Lead | [ ] | |
| 3.8 | Control checklist review | Finance Lead | [ ] | Use templates/control-assessment-template.md |

**Review close sign-off:** __________________ Date: __________

---

## Phase 4: Final Close

**Status: BLOCKED — waiting for Phase 3**

| # | Task | Owner | Done | Notes |
|---|---|---|---|---|
| 4.1 | Finance Lead approval | Finance Lead | [ ] | |
| 4.2 | CFO approval (if required) | CFO | [ ] | |
| 4.3 | Close period in Exact Online — verify status = "Closed" | Finance Lead | [ ] | |
| 4.4 | Archive close package in close/archive/2026-03/ | Finance Lead | [ ] | Commit completed checklist + evidence via PR |
| 4.5 | Document lessons learned | Finance Lead | [ ] | |
| 4.6 | Create improvement issues in GitHub | Finance Lead | [ ] | |

**Final close sign-off:** __________________ Date: __________

---

## Lessons Learned (in progress)

1. **Sales invoices are entered via dagboek 70 (Verkoopboek), not the Verkoopfacturen module.** The runbook and handoff document should reference dagboek 70, not the sales invoice module.
2. **All dagboek entries for March 2026 are unprocessed.** The close cannot proceed until entries are verwerkt. This is a routine Exact Online step but was not explicit in the runbook.
3. **29/29 invoice count match between Zoho Books and Exact Online confirms the manual sync is working.** No sync exceptions.
4. **122 activamutaties entries exist for period 3.** This is a high number — needs review to understand if these are all depreciation entries or include other asset mutations.

## Improvement Items (identified so far)

- [ ] Add "Verwerken boekingen" as an explicit pre-close step in the runbook (currently implicit)
- [ ] Update runbook to reference dagboek 70 (Verkoopboek) for sales invoice verification, not Verkoopfacturen module
- [ ] Document the bank import lag: secondary account (NL74 RABO) last imported 23-03-2026 — missing 8 days
