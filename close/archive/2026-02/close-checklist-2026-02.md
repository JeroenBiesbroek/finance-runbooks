# Month-End Close Checklist

## Period: 2026-02 (period 2 — February 2026)
## Close Owner: Finance Lead (Jeroen Biesbroek)
## Target Close Date: 2026-04-07
## Type: First governed close (retrospective)

> This is the first close executed under the governed close model.
> February 2026 is already past — this applies governance to an already-completed accounting period.

---

## Phase 1: Pre-Close

**Status: TO REDO — previous data extraction was for period 3 (March). Must re-extract for period 2 (February).**

### Data Extraction Summary

| Source | Period | Extraction date | Method |
|---|---|---|---|
| Zoho Books | February 2026 (01-02 to 28-02) | Pending | Browser: Verkoop > Facturen, date filter |
| Exact Online | 2026 period 2 | Pending | Browser: Financieel > Boekingen > Overzicht |

> **Note:** The prior extraction (2026-04-05) captured period 3 (March) data. That data is invalid for this close. Period 2 data must be extracted separately.

### Exact Online Booking Summary — Period 2 (February 2026)

| Dagboek | Description | Te verwerken | Verwerkt | Notes |
|---|---|---|---|---|
| 20 | NL16 RABO 0352 7584 06 | — | — | To be verified |
| 22 | NL74 RABO 3666 7097 88 | — | — | To be verified |
| 60 | Inkoopboek | — | — | To be verified |
| 70 | Verkoopboek | — | — | To be verified |
| 80 | Memoriaal Lonen | — | — | To be verified |
| 90 | Memoriaal | — | — | To be verified |
| 94 | Memoriaal uitgestelde omzet/kosten | — | — | To be verified |
| 95 | Activamutaties | — | — | To be verified |

### Task Results

| # | Task | Owner | Done | Notes |
|---|---|---|---|---|
| 1.1 | Verify all sales invoices synced from Zoho Books | Finance Lead | [ ] | Compare Zoho Books February invoice count to Exact Online dagboek 70 period 2 count |
| 1.2 | Review sales invoice sync exceptions | Finance Lead | [ ] | First governed close — empty exception register expected |
| 1.3 | Confirm all purchase invoices processed | Finance Lead | [ ] | Check dagboek 60 period 2 |
| 1.4 | Confirm all bank statements imported and matched | Finance Lead | [ ] | Verify bank import through 28-02-2026 for both accounts |
| 1.5 | Review bank matching exceptions | Finance Lead | [ ] | Depends on 1.4 |
| 1.6 | Review open exception items | Finance Lead | [ ] | Check GitHub issues |

### Hard Blocker

**All dagboek entries for period 2 must have status "Verwerkt" before Phase 2 can begin.**

**Required action by Finance Lead:**
1. Process (verwerken) all entries in dagboek 70 (verkoopboek) for period 2
2. Process all entries in dagboek 60 (inkoopboek) for period 2
3. Process all entries in dagboek 20 + 22 (bank) for period 2
4. Process entries in dagboek 80, 90, 94, 95 for period 2
5. After processing, verify no errors occurred

**Navigation in Exact Online:** Financieel > Boekingen > Verwerken

### Pre-Close Sign-Off

**Pre-close sign-off:** __________________ Date: __________

---

## Phase 2: Controlled Close

**Status: BLOCKED — waiting for Phase 1 completion and processing**

| # | Task | Owner | Done | Notes |
|---|---|---|---|---|
| 2.1 | Post recurring journal entries | Finance Lead | [ ] | Use journal templates from finance-config-catalog |
| 2.2 | Post salary accruals (vakantiegeld, 13e maand) | Finance Lead | [ ] | Template 2 — confirm amounts from payroll |
| 2.3 | Post cost accruals (accountant, energy, etc.) | Finance Lead | [ ] | Template 3 — estimate amounts |
| 2.4 | Reverse prior period cost accruals | Finance Lead | [ ] | N/A for first close |
| 2.5 | Run fixed asset depreciation (preview → review → post) | Finance Lead | [ ] | Check period 2 depreciation status |
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
| 3.2 | P&L review — compare to prior period | Finance Lead | [ ] | Compare to January 2026 (period 1) |
| 3.3 | VAT reconciliation | Finance Lead | [ ] | Use templates/reconciliation-template.md |
| 3.4 | Bank balance reconciliation | Finance Lead | [ ] | Exact GL balance vs bank statement at 28-02-2026 |
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
| 4.4 | Archive close package in close/archive/2026-02/ | Finance Lead | [ ] | Commit completed checklist + evidence via PR |
| 4.5 | Document lessons learned | Finance Lead | [ ] | |
| 4.6 | Create improvement issues in GitHub | Finance Lead | [ ] | |

**Final close sign-off:** __________________ Date: __________

---

## Lessons Learned (from process setup — not yet from execution)

1. **Sales invoices are entered via dagboek 70 (Verkoopboek), not the Verkoopfacturen module.** Runbook updated.
2. **"Verwerken boekingen" is a required step before controlled close.** Runbook updated with explicit Step 2.6.
3. **Secondary bank account (NL74 RABO) may have import lag.** Runbook updated with check.

## Improvement Items (identified so far)

- [x] Add "Verwerken boekingen" as explicit pre-close step — done in runbook
- [x] Update runbook to reference dagboek 70 — done
- [x] Document bank import lag — done
