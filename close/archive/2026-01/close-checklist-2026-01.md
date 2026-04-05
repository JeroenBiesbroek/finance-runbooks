# Month-End Close Checklist

## Period: 2026-01 (period 1 — January 2026)
## Close Owner: Finance Lead (Jeroen Biesbroek)
## Target Close Date: 2026-04-07
## Type: Retrospective governed close

> Retrospective close applying the governed model to January 2026.

---

## Phase 1: Pre-Close

**Status: COMPLETED — sync exception identified, partial processing found**
**Executed: 2026-04-05 by Claude Code (AI-assisted)**

### Data Extraction Summary

| Source | Period | Extraction date | Method |
|---|---|---|---|
| Zoho Books | January 2026 (01-01 to 31-01) | 2026-04-05 | Browser: Verkoop > Facturen, date filter 01-01-2026 to 31-01-2026 |
| Exact Online | 2026 period 1 | 2026-04-05 | Browser: Financieel > Boekingen > Overzicht, year 2026, Te verwerken + Verwerkt |

### Exact Online Booking Summary — Period 1 (January 2026)

| Dagboek | Description | Te verwerken | Verwerkt | Total | Notes |
|---|---|---|---|---|---|
| 20 | NL16 RABO 0352 7584 06 | 45 | 0 | 45 | Main bank — not processed |
| 22 | NL74 RABO 3666 7097 88 | 2 | 0 | 2 | Secondary bank — not processed |
| 60 | Inkoopboek | 22 | 27 | 49 | Partially processed |
| 70 | Verkoopboek | 17 | 12 | 29 | Partially processed |
| 80 | Memoriaal Lonen | 1 | 0 | 1 | Not processed |
| 90 | Memoriaal | 5 | 1 | 6 | Partially processed |
| 94 | Memoriaal uitgestelde omzet/kosten | 24 | 25 | 49 | Partially processed |
| 95 | Activamutaties | 121 | 0 | 121 | Not processed |
| **Total** | | **237** | **65** | **302** | **21.5% verwerkt** |

### Task Results

| # | Task | Owner | Done | Notes |
|---|---|---|---|---|
| 1.1 | Verify all sales invoices synced from Zoho Books | Claude Code | [x] | **EXCEPTION: Zoho Books: 20 invoices. Exact Online dagboek 70: 29 entries (17+12). DELTA = +9 in Exact.** Exact has 9 MORE entries than Zoho. See exception detail below. |
| 1.2 | Review sales invoice sync exceptions | Claude Code | [x] | **1 sync exception identified.** 9 extra Exact entries require investigation. |
| 1.3 | Confirm all purchase invoices processed | Finance Lead | [ ] | 49 total (22 te verwerken + 27 verwerkt). **22 still unprocessed.** |
| 1.4 | Confirm all bank statements imported and matched | Finance Lead | [ ] | 45 + 2 = 47 bank entries. **ALL 47 unprocessed (0 verwerkt).** Bank import status must be verified through 31-01-2026. |
| 1.5 | Review bank matching exceptions | Finance Lead | [ ] | Depends on 1.4 — after processing. |
| 1.6 | Review open exception items | Claude Code | [x] | No exception issues in GitHub prior to this close. 1 new exception identified (task 1.1). |

### Sync Exception: 9 Extra Entries in Exact Online

**Zoho Books has 20 invoices for January 2026. Exact Online dagboek 70 has 29 entries. Delta = +9 (Exact has more).**

This is the opposite pattern from period 2 (where Zoho had 3 more than Exact).

**Likely causes for extra Exact entries:**
- Credit notes booked in dagboek 70 (Verkoopboek also handles credit notes)
- Invoices from December 2025 booked into January 2026 period
- Manual corrections or reclassifications
- Entries not originating from Zoho Books

**Required action by Finance Lead:**
1. List all 29 entries in dagboek 70 period 1 (12 verwerkt + 17 te verwerken)
2. Match each to a Zoho Books invoice number
3. Identify the 9 entries without Zoho match
4. For each: classify as credit note, prior period, correction, or other
5. Document findings

### Verwerken Status — Partially Processed

Unlike period 2 (0% verwerkt), period 1 is **partially processed (21.5%)**:
- Dagboek 60 (inkoop): 55% verwerkt (27/49)
- Dagboek 70 (verkoop): 41% verwerkt (12/29)
- Dagboek 94 (uitgestelde omzet): 51% verwerkt (25/49)
- Dagboek 20/22 (bank): 0% verwerkt
- Dagboek 95 (activa): 0% verwerkt

**Required action by Finance Lead:**
1. Process remaining entries: Financieel > Boekingen > Verwerken, period 1
2. Verify all dagboeken show 0 "Te verwerken" for period 1

### Blockers

**Blocker 1: Sync exception** — 9 extra Exact entries vs Zoho must be investigated.

**Blocker 2: Verwerken** — 237 entries still unprocessed across all dagboeken.

### Pre-Close Sign-Off

**Pre-close sign-off:** __________________ Date: __________

> Cannot be signed off until sync exception is investigated and all entries are processed.

---

## Phase 2: Controlled Close

**Status: BLOCKED — waiting for Phase 1 sign-off + verwerken**

| # | Task | Owner | Done | Notes |
|---|---|---|---|---|
| 2.1 | Post recurring journal entries | Finance Lead | [ ] | |
| 2.2 | Post salary accruals (vakantiegeld, 13e maand) | Finance Lead | [ ] | |
| 2.3 | Post cost accruals (accountant, energy, etc.) | Finance Lead | [ ] | |
| 2.4 | Reverse prior period cost accruals | Finance Lead | [ ] | N/A for January (first month of fiscal year) |
| 2.5 | Run fixed asset depreciation (preview → review → post) | Finance Lead | [ ] | 121 activamutaties, 0 verwerkt. |
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
| 3.2 | P&L review — compare to prior period | Finance Lead | [ ] | Compare to December 2025 (period 12 prior year) |
| 3.3 | VAT reconciliation | Finance Lead | [ ] | |
| 3.4 | Bank balance reconciliation | Finance Lead | [ ] | GL balance vs bank statement at 31-01-2026 |
| 3.5 | Debtor balance review | Finance Lead | [ ] | |
| 3.6 | Creditor balance review | Finance Lead | [ ] | |
| 3.7 | Variance analysis — explain material items | Finance Lead | [ ] | |
| 3.8 | Control checklist review | Finance Lead | [ ] | |

**Review close sign-off:** __________________ Date: __________

---

## Phase 4: Final Close

**Status: BLOCKED — waiting for Phase 3**

| # | Task | Owner | Done | Notes |
|---|---|---|---|---|
| 4.1 | Finance Lead approval | Finance Lead | [ ] | |
| 4.2 | CFO approval (if required) | CFO | [ ] | |
| 4.3 | Close period in Exact Online — verify status = "Closed" | Finance Lead | [ ] | |
| 4.4 | Archive close package in close/archive/2026-01/ | Finance Lead | [ ] | |
| 4.5 | Document lessons learned | Finance Lead | [ ] | |
| 4.6 | Create improvement issues in GitHub | Finance Lead | [ ] | |

**Final close sign-off:** __________________ Date: __________

---

## Lessons Learned

1. **Period 1 is partially processed (21.5%)**, unlike period 2 (0%). This suggests some processing was done earlier but not completed.
2. **Dagboek 70 has MORE entries than Zoho Books** (29 vs 20). The delta direction is opposite from period 2 (where Zoho had more). This likely includes credit notes or prior-period entries.
3. **Bank accounts (dagboek 20/22) are 0% processed** even though other dagboeken are partially processed.

## Improvement Items
<!-- List improvement issues created -->

---

## Comparison: Period 1 vs Period 2

| Metric | Period 1 (Jan) | Period 2 (Feb) |
|---|---|---|
| Zoho Books invoices | 20 | 28 |
| Exact dagboek 70 entries | 29 | 25 |
| Delta | +9 (Exact has more) | -3 (Zoho has more) |
| Verwerken status | 21.5% processed | 0% processed |
| Total entries all dagboeken | 302 | 313 |
| Bank entries processed | 0/47 | 0/37 |
