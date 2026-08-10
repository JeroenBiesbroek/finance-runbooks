# Analytical Review

## Period: 2026-02 (period 2 — February 2026)
## Prepared by: <!-- Finance Lead -->
## Date: <!-- YYYY-MM-DD — populate after Phase 3 start -->

**Reporting stage: BRONZE**

> Full analytical review (all 5 mandatory comparisons with trial balance data) is a Silver deliverable.
> At Bronze, this file documents what is already assessable and provides the first revenue-level observations.
> Prior month = January 2026 (period 1). Prior year = January-February 2025 from Exact.
> Evidence references: use E-codes from `supporting-evidence-index-2026-02.md`

---

## Bronze Scope — What Can and Cannot Be Assessed

### What Bronze can already assess

| Assessment | Source | Available |
|---|---|---|
| Revenue population completeness | Zoho Books + Exact dagboek 70 reconciliation | **Yes — E-01 complete** |
| Revenue by customer (incl BTW) | Zoho invoice data | **Yes — 28 invoices, EUR 221.885,98** |
| Revenue month-over-month (Zoho level) | P1 + P2 Zoho reconciliation data | **Yes — P2 EUR 221.886 vs P1 EUR 122.603 (+81%)** |
| Customer concentration risk | Zoho invoice data | **Yes — INV-000269 alone = 39% of Feb revenue** |
| Customer top-5 shift vs January | P1 + P2 Zoho data | **Yes — see below** |
| Cross-period booking impact | Reconciliation exception analysis | **Yes — 6 February invoices in P1 (EUR 14.034,53)** |
| Material missing items | Reconciliation exceptions | **Yes — INV-000269 (EUR 86K) not in Exact** |

### What Bronze cannot assess yet

| Assessment | Blocked by | Available at |
|---|---|---|
| Revenue by GL category (excl BTW) | Trial balance not available (E-12) | Silver |
| P&L month vs prior month (all lines) | Trial balance for both P1 and P2 | Silver |
| P&L YTD vs prior year YTD | Trial balance + Jan-Feb 2025 data | Silver |
| Balance sheet movement analysis | Trial balance | Silver |
| Gross margin % | Revenue + direct cost data from trial balance | Silver |
| Debtor aging comparison | Processed subledger | Silver |

### Bronze Revenue Observations — Period 2

1. **Total Zoho February revenue (incl BTW): EUR 221.885,98** from 28 invoices across 11 customers.
2. **Month-over-month (Zoho level): +EUR 99.283,11 (+81%) vs January.** This is a material increase that requires explanation.
3. **Key driver: INV-000269 AsfaltNu Amsterdam I (EUR 86.394,00)** — a single invoice that represents 39% of February revenue and 87% of the month-over-month increase. **This invoice is not yet in Exact.** Without it, February revenue would be EUR 135.492 vs January EUR 122.603, a much more moderate +10.5% increase.
4. **Customer concentration risk:** AsfaltNu group (C.V. + Amsterdam I) = EUR 114.030,40 = 51% of February revenue. This is extreme single-group concentration.
5. **Top-5 shift vs January:** Koninklijke Van Twist enters the top 5 (EUR 15.119 vs EUR 2.769 in January, +446%). GMB Civiel drops out. Hanab Energy Solutions drops from #1 (EUR 29K) to outside top 5 (EUR 13K).
6. **Cross-period impact:** EUR 14.034,53 (6 invoices) booked in P1 instead of P2. If rebooked, P2 Exact revenue would increase by EUR 14K.
7. **Exception exposure:** EUR 89.136,09 in unresolved exceptions (OI-P2-001 through OI-P2-004). Of this, EUR 86.394 is a single material item.

### Bronze Comparison — Revenue by Customer Top-5 Shift (Zoho, incl BTW)

| Rank Jan | Customer | Jan amount | Rank Feb | Feb amount | Change | Shift |
|---|---|---|---|---|---|---|
| — | AsfaltNu Amsterdam I | — | 1 | EUR 86.394,00 | New | **New #1 — material, unbooked** |
| 1 | Hanab Energy Solutions | EUR 29.306,20 | 7 | EUR 13.003,79 | -56% | **Dropped from #1 to outside top 5** |
| 2 | AsfaltNu C.V. | EUR 26.378,00 | 2 | EUR 27.636,40 | +5% | Stable |
| 3 | Boskalis Nederland | EUR 21.012,95 | 4 | EUR 21.476,26 | +2% | Stable |
| 4 | BAM Energie & Water | EUR 18.464,99 | 3 | EUR 22.360,98 | +21% | Moved up 1 position |
| 5 | GMB Civiel B.V. | EUR 5.595,69 | 9 | EUR 5.761,78 | +3% | **Dropped from #5 — displaced by Kon. Van Twist** |
| 10 | Koninklijke Van Twist | EUR 2.768,87 | 5 | EUR 15.118,95 | +446% | **Entered top 5** |

> **Explanation required at Silver:** Hanab Energy Solutions -56% (EUR -16K), Koninklijke Van Twist +446% (EUR +12K). These likely exceed the >10% AND >EUR 2.500 threshold.

---

## Mandatory Comparisons

| # | Comparison | Scope | Threshold for explanation | Status |
|---|---|---|---|---|
| 1 | Current month vs prior month | All P&L lines | > 10% AND > EUR 2.500 | Silver — requires trial balance |
| 2 | YTD vs prior year YTD | All P&L lines | > 10% AND > EUR 5.000 | Silver — requires trial balance |
| 3 | Current month BS vs prior month BS | All BS lines | Change > EUR 2.500 | Silver — requires trial balance |
| 4 | Gross margin % current vs prior month | Margin line | > 5 percentage points | Silver — requires trial balance |
| 5 | Revenue by customer — top 5 shift | Revenue | Customer drops from top 5 or new entry | **Done at Bronze (Zoho level)** — see above |

---

## Balance Sheet Analytical Review

| GL range | Account area | Prior month (Jan 2026) | Current month (Feb 2026) | Change | Change % | Explanation required? | Explanation |
|---|---|---|---|---|---|---|---|
| 0xxx | Fixed assets (net) | | | | | | |
| 1100-1199 | Bank | | | | | | |
| 1300-1399 | Debtors | | | | | **Yes (Bronze)** | INV-000269 (EUR 86K) will create material debtors movement once booked |
| 1450-1462 | Prepayments | | | | | | |
| 1600-1699 | Creditors | | | | | | |
| 1500-1599 | VAT positions | | | | | | |
| 1770-1899 | Accrued liabilities | | | | | | |

**Rule:** Explanation required if change > EUR 2.500.

---

## P&L Analytical Review — Current Month vs Prior Month

| GL range | Category | Prior month (Jan 2026) | Current month (Feb 2026) | Change | Change % | Explanation required? | Explanation |
|---|---|---|---|---|---|---|---|
| 8000-8999 | Revenue | | | | | | |
| 7000-7999 | Direct costs | | | | | | |
| — | **Gross margin** | | | | | | |
| — | **Gross margin %** | | | | | | |
| 4000-4099 | Salary costs | | | | | | |
| 4400-4499 | Depreciation | | | | | | |
| 4500-4999 | Other opex | | | | | | |
| — | **Operating result** | | | | | | |

**Rule:** Explanation required if change > 10% AND > EUR 2.500.

---

## P&L Analytical Review — YTD vs Prior Year YTD

| Category | Prior year YTD (Jan-Feb 2025) | Current YTD (Jan-Feb 2026) | Change | Change % | Explanation |
|---|---|---|---|---|---|
| Revenue | | | | | |
| Direct costs | | | | | |
| Gross margin | | | | | |
| Operating expenses | | | | | |
| Operating result | | | | | |

**Rule:** Explanation required if change > 10% AND > EUR 5.000.

---

## Revenue by Customer — Top 5 Shift Analysis

> **Bronze complete — see Bronze Scope section above for full top-5 shift analysis with actual Zoho data.**

**Rule:** If a customer drops from top 5 or a new customer enters: explain why.

**Bronze findings:**
- AsfaltNu Amsterdam I enters at #1 (EUR 86.394 — new customer, not yet in Exact)
- Hanab Energy Solutions drops from #1 to #7 (-56%, EUR -16K)
- Koninklijke Van Twist enters at #5 (+446%, EUR +12K)
- GMB Civiel B.V. drops from #5 to #9

> Full explanations to be documented at Silver after trial balance data confirms these movements in net revenue terms.

---

## Gross Margin Analysis

| Item | Prior month (Jan 2026) | Current month (Feb 2026) | Change |
|---|---|---|---|
| Revenue | | | |
| Direct costs | | | |
| Gross margin | | | |
| Gross margin % | | | |

**Rule:** If margin % change > 5 percentage points: explain the driver (pricing, mix, cost change).

Explanation: <!-- Populate after data available -->

---

## Analytical Review Conclusion

**Overall conclusion:** <!-- Populate after all comparisons completed -->

**Analytical review sign-off:** __________________ Date: __________
