# P&L Specification

## Period: 2026-01 (period 1 — January 2026)
## Prepared by: <!-- Finance Lead -->
## Date: <!-- YYYY-MM-DD — populate after Phase 2 completion -->

**Status: BLOCKED — requires Exact Online trial balance after verwerken completion**

> This file is the instantiated P&L specification for period 1.
> Populate all sections after Phase 2 is complete and trial balance is exported.
> Thresholds per MONTH_END_REPORTING_DOSSIER_STANDARD.md:
> - P&L explanation threshold: variance > 10% AND > EUR 2.500
> - Material item: > EUR 10.000 requires individual evidence
> Note: January is the first month of FY 2026 — no prior month for month-over-month.
> Prior year comparison: January 2025 from Exact.
> Evidence references: use E-codes from `supporting-evidence-index-2026-01.md`

---

## Revenue (8000-8999)

### Revenue by category

| GL | Category | Current month | Prior month | Change | Change % | YTD | Prior year YTD | YTD change % |
|---|---|---|---|---|---|---|---|---|
| 8000 | Omzet binnenland hoog tarief | | | N/A (first month) | | | | |
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

> January 2026 is month 1 — "Prior month" is December 2025 (period 12 prior year).
> YTD = current month for January.

### Bronze — Preliminary Revenue from Zoho Source

| Source | Amount incl BTW | Invoices | Status |
|---|---|---|---|
| Zoho Books January invoices (matched to Exact) | **EUR 122.602,87** | 20 | Verified — all 20 matched in Exact dagboek 70 |
| Cross-period: 7 February invoices booked in P1 | EUR 15.167,92 | 7 | Pending Finance Lead decision (OI-P1-002) |
| Manual entry IO260054 Sterk B.V. | EUR 663,96 | 1 | Pending Finance Lead confirmation (OI-P1-001) |
| Credit note Buse Gas B.V. | EUR -1.612,24 | 1 | Non-Zoho customer, direct Exact entry |
| **Total dagboek 70 period 1** | **EUR 136.822,51** | **29** | Preliminary — amounts incl BTW, not yet split to GL |

> **Limitation:** These are invoice amounts incl BTW, not net revenue per GL. Actual P&L revenue (excl BTW) requires trial balance. The figures above confirm the revenue population in Exact dagboek 70 is complete.

### Revenue by customer (top 5 by month) — Bronze / Zoho source

| Customer | Current month (Zoho incl BTW) | Prior month | Change | Notes |
|---|---|---|---|---|
| 1. Hanab Energy Solutions | EUR 29.306,20 | — | N/A | 1 invoice (INV-000242) |
| 2. AsfaltNu C.V. | EUR 26.378,00 | — | N/A | 1 invoice (INV-000216) |
| 3. Boskalis Nederland | EUR 21.012,95 | — | N/A | 4 invoices |
| 4. BAM Energie & Water | EUR 18.464,99 | — | N/A | 4 invoices |
| 5. GMB Civiel B.V. | EUR 5.595,69 | — | N/A | 2 invoices |
| Other (7 customers) | EUR 21.845,04 | — | N/A | Gebr. vd Poel, Comb. Dijkalliantie, Kisjes, Kon. Van Twist, Sterk, Genpower |
| **Total (Zoho Jan)** | **EUR 122.602,87** | — | N/A | 20 invoices, all matched |

> **Source:** `sales-ledger-reconciliation-2026-01.md` — line-level matched data.
> **Prior month:** December 2025 not available at Bronze. Requires Exact trial balance (Silver).
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

| GL | Category | Current month | Prior month | Change | Change % | YTD | Prior year YTD |
|---|---|---|---|---|---|---|---|
| 7000 | Inkoopkosten grondstoffen | | | | | | |
| 7001 | Inkoopkosten gas | | | | | | |
| 7002 | Inkoopkosten transport | | | | | | |
| 7003 | Inkoopkosten onderhoud | | | | | | |
| 7004 | Inkoopkosten overig | | | | | | |
| | **Total direct costs** | | | | | | |

> **BRONZE NOTE — Direct cost GL structure:** The GL accounts above are placeholders based on the standard 7000-series. The actual GL accounts used by Powercrumbs in Exact must be confirmed from the trial balance at Silver. Finance Lead: verify and correct these account codes after verwerken.
> **Known data:** Dagboek 60 (Inkoopboek): 49 entries (22 te verwerken, 27 verwerkt). Purchase invoice amounts are not yet extracted at line level.

### Gross margin

| Item | Current month | Prior month | Change |
|---|---|---|---|
| Revenue | | | |
| Direct costs | | | |
| **Gross margin** | | | |
| **Gross margin %** | | | |

> If gross margin % change > 5 percentage points vs December 2025: explain.

### Material variance explanations

| Category | Variance | Explanation |
|---|---|---|
| | | |

**Conclusion:** <!-- Populate after data available -->

---

## Operating Expenses (4000-4999)

### Expenses by category

| GL range | Category | Current month | Prior month | Change | Change % | YTD | Prior year YTD |
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
> **Known data:** 121 activamutaties (dagboek 95), 0 verwerkt.

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
- [ ] Payroll summary for January 2026 → E-22
- [ ] Depreciation output reconciled to asset rollforward → E-07, E-08

**Conclusion:** <!-- Populate after data available -->

---

## Unusual or Manual Items

### Items this period

| Date | Description | GL account | Amount | Dagboek | Reason | Support attached |
|---|---|---|---|---|---|---|
| 22-01-2026 | IO260054 Sterk B.V. — manual sales entry, no Zoho origin | Dagboek 70 | EUR 663,96 | 70 | Direct Exact entry, ref "IO260054" (project order). OI-P1-001 | Pending Finance Lead confirmation |
| 20-01-2026 | Buse Gas B.V. — credit note, Transportkosten Week 47 | Dagboek 70 | EUR -1.612,24 | 70 | Non-Zoho customer (debtor 81). Direct Exact credit note | Not in Zoho — Buse Gas is Exact-only |

> **Known data:** Dagboek 90 (Memoriaal): 6 entries (5 te verwerken, 1 verwerkt). All manual memorial entries must be listed here once identified after verwerken.
> Dagboek 80 (Memoriaal Lonen): 1 entry, 0 verwerkt — salary journal to be reviewed after verwerken.

**Conclusion:** <!-- Populate after data available -->

---

## P&L Summary

| Item | Current month | Prior month | YTD | Prior year YTD |
|---|---|---|---|---|
| Total revenue | | | | |
| Total direct costs | | | | |
| **Gross margin** | | | | |
| Total operating expenses | | | | |
| **Operating result** | | | | |
| Financial income/expense | | | | |
| **Result before tax** | | | | |
