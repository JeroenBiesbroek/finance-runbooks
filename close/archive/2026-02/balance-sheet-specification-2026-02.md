# Balance Sheet Specification

## Period: 2026-02 (period 2 — February 2026)
## Prepared by: <!-- Finance Lead -->
## Date: <!-- YYYY-MM-DD — populate after Phase 2 completion -->

**Status: BLOCKED — requires Exact Online trial balance after verwerken completion**

> This file is the instantiated balance sheet specification for period 2.
> Populate all sections after Phase 2 is complete and trial balance is exported.
> Thresholds per MONTH_END_REPORTING_DOSSIER_STANDARD.md:
> - Explanation threshold: balance > EUR 5.000 or change > EUR 2.500
> - Material item: > EUR 10.000 requires individual evidence
> Evidence references: use E-codes from `supporting-evidence-index-2026-02.md`

---

## Tangible Fixed Assets (0xxx)

### Rollforward

| Category | Opening (= P1 closing) | Investments | Disinvestments | Depreciation | Closing |
|---|---|---|---|---|---|
| Machines / Powerhub | | | | | |
| Powerbox | | | | | |
| Software / AI | | | | | |
| Bedrijfsinventaris | | | | | |
| Transport | | | | | |
| **Total** | | | | | |

> **Known data:** 124 activamutaties in dagboek 95, 0 verwerkt.
> **Opening balances** depend on Period 1 close — use P1 closing values.
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

### Aging at period end

| Aging bucket | Amount | # of invoices | Notes |
|---|---|---|---|
| Current (0-30 days) | | | |
| 31-60 days | | | |
| 61-90 days | | | |
| > 90 days | | | |
| **Total** | | | |

> **Known data:** 28 Zoho invoices for February. 25 Exact dagboek 70 entries (0 verwerkt).
> **MATERIAL EXCEPTION:** INV-000269 AsfaltNu Amsterdam I (EUR 86.394) — debtor not in Exact. Must be created and booked before debtor aging is complete.
> Sales ledger reconciliation: see E-01.

### Post-period cash collection review

| Customer | Open amount at period end | Collected after period end | Remaining open | Notes |
|---|---|---|---|---|
| | | | | |

> Review first 10 business days after 28-02-2026.

### Major open items (> EUR 5.000)

| Customer | Invoice | Amount | Age | Status | Action |
|---|---|---|---|---|---|
| AsfaltNu Amsterdam I | INV-000269 | EUR 86.394,00 | N/A — not yet booked | Exception #1 | Create debtor in Exact, book invoice |

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

> **Known data:** 36 entries dagboek 20, 1 entry dagboek 22 — all 37 unprocessed.
> **Blocked by:** E-02 (bank import confirmation), E-03 (verwerken)

### Reconciling items detail

| # | Description | Amount | Expected resolution |
|---|---|---|---|
| | | | |

### Evidence
- [ ] Bank statement(s) at 28-02-2026
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

> **Known data:** 71 entries dagboek 60, 0 verwerkt.

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
- [ ] BTW-aangifte for February 2026 (or Q1 if quarterly)
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
> **Known data:** 49 entries dagboek 94, 0 verwerkt — deferred revenue/costs.

**Conclusion:** <!-- Populate after data available -->

---

## Accrued Liabilities (1770-1899)

### Balance detail

| GL account | Description | Opening (= P1 closing) | Additions | Releases | Closing | Calculation basis |
|---|---|---|---|---|---|---|
| 1770 | Reservering 13e maand | | | | | 8.33% of gross salary |
| 1780 | Reservering vakantiegeld | | | | | 8% of gross salary |
| 1884 | Nog te betalen huur | | | | | Monthly rent amount |
| 1887 | Nog te betalen accountant | | | | | Estimated monthly fee |
| 1889 | Nog te betalen overig | | | | | |

> Specify only if closing balance > EUR 5.000 or movement > EUR 2.500.
> Opening balances depend on Period 1 close.

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

> February is month 2 — equity should normally show no movement unless capital events occurred.

**Conclusion:** <!-- No movement / Movement explained -->
