# Balance Sheet Specification

## Period: <!-- YYYY-MM -->
## Prepared by: <!-- Name -->
## Date: <!-- YYYY-MM-DD -->

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
- [ ] Depreciation preview/output from Exact Online
- [ ] Investment invoices (if any)
- [ ] Disinvestment approval (if any)
- [ ] Asset register export from Exact Online

**Conclusion:** <!-- Correct / Requires adjustment / Exception noted -->

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

### Post-period cash collection review

| Customer | Open amount at period end | Collected after period end | Remaining open | Notes |
|---|---|---|---|---|
| | | | | |

> Review first 10 business days after period end. If > 80% collected, debtors position is supported.

### Major open items (> EUR 5.000)

| Customer | Invoice | Amount | Age | Status | Action |
|---|---|---|---|---|---|
| | | | | | |

### Evidence
- [ ] Debtor aging report from Exact Online
- [ ] Post-period bank statements showing collections
- [ ] Correspondence for overdue items > 90 days

**Conclusion:** <!-- Correct / Provision needed / Exception noted -->

---

## Bank (1100-1199)

### Reconciliation per account

| Account | GL balance | Bank statement balance | Difference | Reconciling items |
|---|---|---|---|---|
| NL16 RABO 0352 7584 06 | | | | |
| NL74 RABO 3666 7097 88 | | | | |
| **Total** | | | | |

### Reconciling items detail

| # | Description | Amount | Expected resolution |
|---|---|---|---|
| 1 | | | |

### Evidence
- [ ] Bank statement(s) at period end date
- [ ] GL bank balance from Exact Online trial balance
- [ ] Reconciliation completed (use `reconciliation-template.md`)

**Conclusion:** <!-- Reconciled / Reconciled with exceptions / Not reconciled -->

---

## Creditors (1600-1699)

### Aging at period end

| Aging bucket | Amount | # of invoices | Notes |
|---|---|---|---|
| Current (0-30 days) | | | |
| 31-60 days | | | |
| > 60 days | | | |
| **Total** | | | |

### Major open items (> EUR 5.000)

| Supplier | Invoice | Amount | Age | Disputed? | Notes |
|---|---|---|---|---|---|
| | | | | | |

### Evidence
- [ ] Creditor aging report from Exact Online

**Conclusion:** <!-- Correct / Exception noted -->

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
| 1 | | |

### Evidence
- [ ] GL trial balance VAT accounts
- [ ] BTW-aangifte for the period (or quarterly if Q-end)
- [ ] Reconciliation completed

**Conclusion:** <!-- Reconciled / Exception noted -->

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

**Conclusion:** <!-- Correct / Exception noted -->

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
- [ ] Calculation basis per accrual
- [ ] Supporting contracts or invoices for material accruals

**Conclusion:** <!-- Correct / Exception noted -->

---

## Equity (0500-0999)

### Movement this period

| Item | Amount | Explanation |
|---|---|---|
| | | |

> Only specify if there is movement. If no movement: state "No movement this period."

**Conclusion:** <!-- No movement / Movement explained -->
