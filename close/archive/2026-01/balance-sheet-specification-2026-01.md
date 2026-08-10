# Balance Sheet Specification

## Period: 2026-01 (period 1 — January 2026)
## Prepared by: <!-- Finance Lead -->
## Date: <!-- YYYY-MM-DD — populate after Phase 2 completion -->

**Status: BLOCKED — requires Exact Online trial balance after verwerken completion**

> This file is the instantiated balance sheet specification for period 1.
> Populate all sections after Phase 2 is complete and trial balance is exported.
> Thresholds per MONTH_END_REPORTING_DOSSIER_STANDARD.md:
> - Explanation threshold: balance > EUR 5.000 or change > EUR 2.500
> - Material item: > EUR 10.000 requires individual evidence
> Evidence references: use E-codes from `supporting-evidence-index-2026-01.md`

---

## Tangible Fixed Assets (0xxx)

### Rollforward

| Category | Opening | Investments | Disinvestments | Depreciation | Closing |
|---|---|---|---|---|---|
| Machines / Powerhub | | | | | |
| Powerbox | | | | | |
| Software / AI | | | | | |
| Bedrijfsinventaris | | | | | |
| Transport | | | | | |
| **Total** | | | | | |

> **Known data:** 121 activamutaties in dagboek 95, 0 verwerkt. Depreciation run has not been executed.
> **Blocked by:** E-03 (verwerken), E-07 (depreciation preview), E-08 (depreciation posted)

### Investments this period

| Date | Asset | Amount excl BTW | Invoice ref | Supplier | Approval |
|---|---|---|---|---|---|
| | | | | | |

### Disinvestments this period

| Date | Asset | Book value | Proceeds | Result | Approval |
|---|---|---|---|---|---|
| | | | | | |

### Depreciation reconciliation

| Source | Amount | Notes |
|---|---|---|
| Exact Online depreciation run output | | Must match dagboek 95 for the period |
| Rollforward depreciation column | | Must match above |
| **Difference** | | Must be zero |

### Evidence
- [ ] Depreciation preview/output from Exact Online → E-07, E-08
- [ ] Investment invoices (if any)
- [ ] Disinvestment approval (if any)
- [ ] Asset register export from Exact Online → E-21

**Conclusion:** <!-- Populate after data available -->

---

## Debtors (1300-1399)

### Bronze — Preliminary Debtor Position from Zoho/Exact Source

> **BRONZE NOTE:** Aging buckets require processed debtor subledger from Exact (Silver). At Bronze, we show the known invoice population from the sales ledger reconciliation. Amounts are incl BTW.

| Source | Amount incl BTW | # of invoices | Notes |
|---|---|---|---|
| Zoho January invoices (matched in Exact) | EUR 122.602,87 | 20 | All matched — E-01 |
| Cross-period February invoices in P1 | EUR 15.167,92 | 7 | Pending allocation decision (OI-P1-002) |
| Manual entry IO260054 Sterk | EUR 663,96 | 1 | Pending confirmation (OI-P1-001) |
| Credit note Buse Gas B.V. | EUR -1.612,24 | 1 | Non-Zoho, reduces debtor balance |
| **Total dagboek 70 invoiced (incl BTW)** | **EUR 136.822,51** | **29** | Pre-verwerken; actual GL debtor balance may differ after payments and processing |

### Debtor population by customer — Bronze / Zoho source

| Customer | Debtor code | Amount incl BTW | # invoices | Notes |
|---|---|---|---|---|
| Hanab Energy Solutions | 417 | EUR 29.306,20 | 1 | Largest single invoice |
| AsfaltNu C.V. | 410 | EUR 26.378,00 | 1 | |
| Boskalis Nederland | 416 | EUR 21.012,95 | 4 | |
| BAM Energie & Water | 415 | EUR 18.464,99 | 4 | |
| Gebr. van der Poel | 413 | EUR 5.984,36 | 2 | |
| GMB Civiel B.V. | 411 | EUR 5.595,69 | 2 | |
| Comb. Dijkalliantie | 412 | EUR 4.574,13 | 1 | |
| Kisjes Transport | 56 | EUR 4.313,65 | 1 | |
| Sterk B.V. | 414 | EUR 2.849,85 | 2 | Excl IO260054 (EUR 663,96 pending) |
| Koninklijke Van Twist | 424 | EUR 2.768,87 | 1 | |
| Genpower B.V. | 421 | EUR 1.354,18 | 1 | |
| **Total Zoho matched** | | **EUR 122.602,87** | **20** | |

> **Source:** `sales-ledger-reconciliation-2026-01.md` — line-level matched data.
> **Limitation:** This shows invoiced amounts, not open debtor balances. Payments received during January reduce the actual debtor balance. Actual aging requires Exact debtor subledger export after verwerken.

### Aging at period end

| Aging bucket | Amount | # of invoices | Notes |
|---|---|---|---|
| Current (0-30 days) | | | |
| 31-60 days | | | |
| 61-90 days | | | |
| > 90 days | | | |
| **Total** | | | |

> Populate from Exact debtor aging export at Silver (E-18).

### Post-period cash collection review

| Customer | Open amount at period end | Collected after period end | Remaining open | Notes |
|---|---|---|---|---|
| | | | | |

> Review first 10 business days after 31-01-2026. Requires bank data (E-20). Silver.

### Major open items (> EUR 5.000)

| Customer | Invoice | Amount | Age | Status | Action |
|---|---|---|---|---|---|
| Hanab Energy Solutions | INV-000242 | EUR 29.306,20 | — | Invoiced 09-01, matched in Exact | Monitor collection |
| AsfaltNu C.V. | INV-000216 | EUR 26.378,00 | — | Invoiced 01-01, matched in Exact | Monitor collection |
| Boskalis Nederland | 4 invoices | EUR 21.012,95 | — | All matched in Exact | Monitor collection |
| BAM Energie & Water | 4 invoices | EUR 18.464,99 | — | All matched in Exact | Monitor collection |
| Gebr. van der Poel | INV-000226 | EUR 5.306,24 | — | Invoiced 01-01, matched in Exact | Monitor collection |
| GMB Civiel B.V. | 2 invoices | EUR 5.595,69 | — | All matched in Exact | Monitor collection |

> **Note:** Open amounts are preliminary (incl BTW, before payments). Actual open amounts at period end require processed subledger.

### Evidence
- [ ] Debtor aging report from Exact Online → E-18
- [ ] Post-period bank statements showing collections → E-20
- [ ] Correspondence for overdue items > 90 days

**Conclusion:** <!-- Populate after data available -->

---

## Bank (1100-1199)

### Reconciliation per account

| Account | GL balance | Bank statement balance | Difference | Reconciling items |
|---|---|---|---|---|
| NL16 RABO 0352 7584 06 | | | | |
| NL74 RABO 3666 7097 88 | | | | |
| **Total** | | | | |

> **Known data:** 45 entries dagboek 20, 2 entries dagboek 22 — all 47 unprocessed.
> **Blocked by:** E-02 (bank import confirmation), E-03 (verwerken)

### Reconciling items detail

| # | Description | Amount | Expected resolution |
|---|---|---|---|
| | | | |

### Evidence
- [ ] Bank statement(s) at 31-01-2026
- [ ] GL bank balance from Exact Online trial balance → E-12
- [ ] Reconciliation completed → E-16

**Conclusion:** <!-- Populate after data available -->

---

## Creditors (1600-1699)

### Aging at period end

| Aging bucket | Amount | # of invoices | Notes |
|---|---|---|---|
| Current (0-30 days) | | | |
| 31-60 days | | | |
| > 60 days | | | |
| **Total** | | | |

> **Known data:** 49 entries dagboek 60 (22 te verwerken, 27 verwerkt).

### Major open items (> EUR 5.000)

| Supplier | Invoice | Amount | Age | Disputed? | Notes |
|---|---|---|---|---|---|
| | | | | | |

### Evidence
- [ ] Creditor aging report from Exact Online → E-19

**Conclusion:** <!-- Populate after data available -->

---

## VAT / Tax (1500-1599, 1700-1749)

### VAT reconciliation

| Item | Amount |
|---|---|
| BTW te vorderen (input VAT) per GL | |
| BTW af te dragen (output VAT) per GL | |
| Net VAT position per GL | |
| Net VAT position per BTW-aangifte | |
| **Difference** | |

### Reconciling items

| # | Description | Amount |
|---|---|---|
| | | |

### Evidence
- [ ] GL trial balance VAT accounts → E-12
- [ ] BTW-aangifte for January 2026 (or Q1 if quarterly)
- [ ] Reconciliation completed → E-17

**Conclusion:** <!-- Populate after data available -->

---

## Prepayments and Accrued Assets (1450-1462)

### Balance detail

| GL account | Description | Opening | Additions | Releases | Closing | Evidence |
|---|---|---|---|---|---|---|
| 1450 | Vooruitbetaalde kosten | | | | | |
| 1451 | Vooruitbetaald machines | | | | | |
| 1460 | Overlopende activa | | | | | |
| 1462 | Nog te ontvangen subsidies | | | | | |

> Specify only if closing balance > EUR 5.000 or movement > EUR 2.500.
> **Known data:** 49 entries dagboek 94 (24 te verwerken, 25 verwerkt) — deferred revenue/costs.

**Conclusion:** <!-- Populate after data available -->

---

## Accrued Liabilities (1770-1899)

### Balance detail

| GL account | Description | Opening | Additions | Releases | Closing | Calculation basis |
|---|---|---|---|---|---|---|
| 1770 | Reservering 13e maand | | | | | 8.33% of gross salary |
| 1780 | Reservering vakantiegeld | | | | | 8% of gross salary |
| 1884 | Nog te betalen huur | | | | | Monthly rent amount |
| 1887 | Nog te betalen accountant | | | | | Estimated monthly fee |
| 1889 | Nog te betalen overig | | | | | |

> Specify only if closing balance > EUR 5.000 or movement > EUR 2.500.

### Evidence
- [ ] Calculation basis per accrual → E-09, E-10
- [ ] Supporting contracts or invoices for material accruals

**Conclusion:** <!-- Populate after data available -->

---

## Equity (0500-0999)

### Movement this period

| Item | Amount | Explanation |
|---|---|---|
| | | |

> January is the first month of fiscal year 2026. Opening equity = closing equity 2025. Verify no unexpected movements.

**Conclusion:** <!-- No movement / Movement explained -->
