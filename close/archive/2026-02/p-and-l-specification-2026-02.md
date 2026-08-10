# P&L Specification

## Period: 2026-02 (period 2 — February 2026)
## Prepared by: <!-- Finance Lead -->
## Date: <!-- YYYY-MM-DD — populate after Phase 2 completion -->

**Status: BLOCKED — requires Exact Online trial balance after verwerken completion**

> This file is the instantiated P&L specification for period 2.
> Populate all sections after Phase 2 is complete and trial balance is exported.
> Thresholds per MONTH_END_REPORTING_DOSSIER_STANDARD.md:
> - P&L explanation threshold: variance > 10% AND > EUR 2.500
> - Material item: > EUR 10.000 requires individual evidence
> Prior month: January 2026 (period 1) — must have at minimum a preliminary trial balance.
> Evidence references: use E-codes from `supporting-evidence-index-2026-02.md`

---

## Revenue (8000-8999)

### Revenue by category

| GL | Category | Current month | Prior month (Jan) | Change | Change % | YTD | Prior year YTD | YTD change % |
|---|---|---|---|---|---|---|---|---|
| 8000 | Omzet binnenland hoog tarief | | | | | | | |
| 8050 | Omzet biogas premium | | | | | | | |
| 8051 | Omzet wholesale | | | | | | | |
| 8052 | Omzet groengas | | | | | | | |
| 8053 | Verhuur powerbox 20 | | | | | | | |
| 8054 | Verhuur powerbox 10 | | | | | | | |
| 8055 | Opbrengst transport | | | | | | | |
| 8056 | Subsidies/consultancy | | | | | | | |
| 8800 | Omzet honorarium | | | | | | | |
| | **Total revenue** | | | | | | | |

> **BRONZE NOTE — Revenue by GL category:** Category-level breakdown requires trial balance (Silver). The total below is derived from Zoho invoice amounts only. GL-level split will be populated after verwerken + trial balance export.

### Bronze — Preliminary Revenue from Zoho Source

| Source | Amount incl BTW | Invoices | Status |
|---|---|---|---|
| Zoho February invoices matched in Exact P2 | **EUR 115.404,51** | 18 | Verified — all matched in dagboek 70 |
| Zoho February invoices also matched in P2 (separate section) | EUR 3.347,66 | 1 | INV-000293, matched at correct amount |
| Zoho February invoice INV-000325 in P2 | EUR 1.165,13 | 1 | Matched in P2 |
| Cross-period: 6 February invoices booked in P1 | EUR 14.034,53 | 6 | Pending allocation decision (OI-P2-007) |
| INV-000274 Sterk partial in P2 | EUR 280,83 | 1 (partial) | Amount mismatch — Zoho total 1.540,15, see OI-P2-002 |
| **INV-000269 AsfaltNu Amsterdam I — MISSING** | **EUR 86.394,00** | **1** | **Not in Exact — debtor does not exist (OI-P2-001)** |
| **Total Zoho February invoices** | **EUR 221.885,98** | **28** | Preliminary — includes EUR 86K not yet in Exact |
| **Of which currently in Exact P2** | **EUR 120.198,13** | **21** | Excluding cross-period and missing |

> **Material risk:** EUR 86.394 (39% of total February revenue) is not yet booked in Exact. This single item dominates the revenue position.
> **Limitation:** Amounts are incl BTW, not net revenue per GL. Actual P&L revenue (excl BTW) requires trial balance.

### Revenue by customer (top 5 by month) — Bronze / Zoho source

| Customer | Current month (Zoho incl BTW) | Prior month (Jan — Zoho) | Change | Notes |
|---|---|---|---|---|
| 1. AsfaltNu Amsterdam I | EUR 86.394,00 | — (new customer) | N/A | **MISSING FROM EXACT** — OI-P2-001 |
| 2. AsfaltNu C.V. | EUR 27.636,40 | EUR 26.378,00 | +EUR 1.258,40 | Incl EUR 532,40 in P1 (cross-period) |
| 3. BAM Energie & Water | EUR 22.360,98 | EUR 18.464,99 | +EUR 3.896,00 | Incl EUR 3.882,20 in P1 |
| 4. Boskalis Nederland | EUR 21.476,26 | EUR 21.012,95 | +EUR 463,31 | Incl EUR 1.561,55 in P1 |
| 5. Koninklijke Van Twist | EUR 15.118,95 | EUR 2.768,87 | +EUR 12.350,08 | New in top 5 — displaces GMB Civiel |
| Other (6 customers) | EUR 48.899,39 | EUR 53.978,06 | -EUR 5.078,67 | Sterk, Hanab, Gebr. vd Poel, GMB, Comb. Dijkalliantie, Bredenoord |
| **Total (Zoho Feb)** | **EUR 221.885,98** | **EUR 122.602,87** | **+EUR 99.283,11** | **+81% — driven primarily by INV-000269 (EUR 86K)** |

> **Source:** `sales-ledger-reconciliation-2026-02.md` + `sales-ledger-reconciliation-2026-01.md`.
> **Key observation:** February Zoho revenue is EUR 99K higher than January. EUR 86K (87% of the increase) comes from a single unbooked invoice. Without INV-000269, February revenue would be EUR 135.492 vs January EUR 122.603 (+10.5%).
> **Amounts are incl BTW.** Net revenue figures will replace these at Silver.

### Material variance explanations (> 10% or > EUR 2.500)

| Category | Variance | Explanation |
|---|---|---|
| | | |

### Evidence
- [ ] Trial balance revenue section from Exact Online → E-12
- [ ] Customer revenue detail (if needed for explanation)

**Conclusion:** <!-- Populate after data available -->

---

## Direct Costs (7000-7999)

### Cost by category

| GL | Category | Current month | Prior month (Jan) | Change | Change % | YTD | Prior year YTD |
|---|---|---|---|---|---|---|---|
| 7000 | Inkoopkosten grondstoffen | | | | | | |
| 7001 | Inkoopkosten gas | | | | | | |
| 7002 | Inkoopkosten transport | | | | | | |
| 7003 | Inkoopkosten onderhoud | | | | | | |
| 7004 | Inkoopkosten overig | | | | | | |
| | **Total direct costs** | | | | | | |

> **BRONZE NOTE — Direct cost GL structure:** The GL accounts above are placeholders based on the standard 7000-series. The actual GL accounts used by Powercrumbs in Exact must be confirmed from the trial balance at Silver. Finance Lead: verify and correct these account codes after verwerken.
> **Known data:** Dagboek 60 (Inkoopboek): 71 entries, 0 verwerkt. Purchase invoice amounts are not yet extracted at line level.

### Gross margin

| Item | Current month | Prior month (Jan) | Change |
|---|---|---|---|
| Revenue | | | |
| Direct costs | | | |
| **Gross margin** | | | |
| **Gross margin %** | | | |

> If gross margin % change > 5 percentage points vs January 2026: explain.

### Material variance explanations

| Category | Variance | Explanation |
|---|---|---|
| | | |

**Conclusion:** <!-- Populate after data available -->

---

## Operating Expenses (4000-4999)

### Expenses by category

| GL range | Category | Current month | Prior month (Jan) | Change | Change % | YTD | Prior year YTD |
|---|---|---|---|---|---|---|---|
| 4000-4099 | Salariskosten | | | | | | |
| 4100-4199 | Sociale lasten | | | | | | |
| 4200-4299 | Pensioenkosten | | | | | | |
| 4300-4399 | Overige personeelskosten | | | | | | |
| 4400-4499 | Afschrijvingen | | | | | | |
| 4500-4599 | Huisvestingskosten | | | | | | |
| 4600-4699 | Verkoopkosten | | | | | | |
| 4700-4799 | Autokosten | | | | | | |
| 4800-4899 | Kantoorkosten | | | | | | |
| 4900-4999 | Algemene kosten | | | | | | |
| | **Total operating expenses** | | | | | | |

### Depreciation reconciliation

| Source | Amount |
|---|---|
| P&L depreciation (GL 4400-4499) | |
| BS rollforward depreciation | |
| **Difference** | |

> Must be zero. If not: investigate before sign-off.
> **Known data:** 124 activamutaties (dagboek 95), 0 verwerkt.

### Salary cost reconciliation

| Source | Amount |
|---|---|
| Gross salary per payroll | |
| Employer charges per payroll | |
| Salary accruals (vakantiegeld, 13e maand) | |
| **Total salary cost per P&L** | |
| GL 4000-4299 per trial balance | |
| **Difference** | |

> **Known data:** 1 entry dagboek 80 (Memoriaal Lonen), 0 verwerkt.

### Material variance explanations (> 10% or > EUR 2.500)

| Category | Variance | Explanation |
|---|---|---|
| | | |

### Evidence
- [ ] Trial balance expense section from Exact Online → E-12
- [ ] Payroll summary for February 2026 → E-22
- [ ] Depreciation output reconciled to asset rollforward → E-07, E-08

**Conclusion:** <!-- Populate after data available -->

---

## Unusual or Manual Items

### Items this period

| Date | Description | GL account | Amount | Dagboek | Reason | Support attached |
|---|---|---|---|---|---|---|
| | | | | | | |

> **Known data:** Dagboek 90 (Memoriaal): 6 entries, 0 verwerkt. All manual memorial entries must be listed here once identified.
> Dagboek 80 (Memoriaal Lonen): 1 entry, 0 verwerkt — salary journal to be reviewed.

**Conclusion:** <!-- Populate after data available -->

---

## P&L Summary

| Item | Current month | Prior month (Jan) | YTD | Prior year YTD |
|---|---|---|---|---|
| Total revenue | | | | |
| Total direct costs | | | | |
| **Gross margin** | | | | |
| Total operating expenses | | | | |
| **Operating result** | | | | |
| Financial income/expense | | | | |
| **Result before tax** | | | | |
