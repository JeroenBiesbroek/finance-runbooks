# Month-End Close Checklist

## Period: 2026-02 (period 2 — February 2026)
## Close Owner: Finance Lead (Jeroen Biesbroek)
## Target Close Date: 2026-04-07
## Type: First governed close (retrospective)

> This is the first close executed under the governed close model.
> February 2026 is already past — this applies governance to an already-completed accounting period.

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

### Sync Exception: 3 Missing Invoices

**Zoho Books has 28 invoices for February 2026. Exact Online dagboek 70 has 25 entries. Delta = 3.**

**Required action by Finance Lead:**
1. Identify which 3 Zoho Books invoices are missing from Exact Online dagboek 70
2. For each missing invoice, determine:
   - Is it entered in a different dagboek or period?
   - Was it skipped intentionally?
   - Does it need to be entered?
3. Resolve or document each as a deferral with justification

**Materiality assessment:** 28 invoices total, 3 missing = 10.7% gap. This exceeds the 5% threshold for investigation per the governed handoff document (section 14: monitoring).

### Blockers

**Blocker 1: Sync exception** — 3 missing invoices must be investigated before pre-close sign-off.

**Blocker 2: Verwerken** — ALL entries in Exact Online period 2 have status "Te verwerken" (0 verwerkt). Finance Lead must process all entries before Phase 2 can begin.

**Required actions by Finance Lead:**
1. Investigate the 3 missing invoices (sync exception)
2. Process (verwerken) all entries for period 2: Financieel > Boekingen > Verwerken
3. Verify bank import covers through 28-02-2026 for both RABO accounts
4. Sign off on pre-close

### Pre-Close Sign-Off

**Pre-close sign-off:** __________________ Date: __________

> Cannot be signed off until sync exception is resolved and all entries are processed.

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

## Lessons Learned

1. **Sales invoice count mismatch found:** Zoho Books 28 vs Exact Online dagboek 70: 25. The governed close model caught this — first real exception.
2. **All entries remain unprocessed (verwerkt = 0) in period 2.** Same pattern as period 3. Verwerken is a structural prerequisite.
3. **Dagboek 70 (Verkoopboek) confirmed as the correct path** for sales invoice verification.

## Improvement Items

- [x] "Verwerken boekingen" added as explicit runbook step — done
- [x] Dagboek 70 reference updated in runbook — done
- [x] Bank import lag documented — done
- [ ] Create GitHub issue for the 3 missing invoices exception — Finance Lead action
