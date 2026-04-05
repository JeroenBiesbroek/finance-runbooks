# Exception Resolution Pack — Period 2 (February 2026)

**Owner:** Finance Lead
**Date created:** 2026-04-05
**Status:** 4 exceptions open — CTRL-SI-001 blocked until resolved

Period 2 cannot proceed to Phase 2 until all 4 exceptions are resolved or accepted with documented justification.

---

## Exception 1: INV-000269 AsfaltNu Amsterdam I — Missing from Exact

| Attribute | Value |
|---|---|
| **Invoice** | INV-000269 |
| **Customer** | AsfaltNu Amsterdam I |
| **Amount** | EUR 86.394,00 (incl BTW) |
| **Zoho date** | 02-02-2026 |
| **Zoho status** | 32 dagen achterstallig |
| **Exact status** | Not entered — no debtor exists |
| **Exception type** | missing-in-exact |
| **Severity** | Critical — material amount |

### Likely cause
AsfaltNu Amsterdam I is not in the Exact Online debtor register. The debtor mapping (CFG-004) flagged this customer as unmatched and assigned resolution to Thijs. Without a debtor code, the invoice cannot be entered in dagboek 70.

### Owner
Thijs (debtor creation) → Finance Lead (invoice entry)

### Required decision
1. Thijs: decide whether AsfaltNu Amsterdam I maps to existing debtor 410 (AsfaltNu C.V.) or needs a new debtor code
2. Finance Lead: after debtor exists, enter INV-000269 in dagboek 70 period 2

### Required action
1. Create or assign debtor in Exact Online
2. Enter INV-000269 in dagboek 70 with correct debtor code, amount, VAT code, GL account
3. Verify entry appears in dagboek 70 period 2

### Evidence needed for closure
- Debtor creation/assignment confirmation
- Dagboek 70 entry showing INV-000269 with correct amount
- Updated reconciliation showing 26/28 → 27/28 matched

### Effect on CTRL-SI-001
Cannot sign off until this invoice is entered. EUR 86K is material.

---

## Exception 2: INV-000274 Sterk B.V. — Amount Mismatch

| Attribute | Value |
|---|---|
| **Invoice** | INV-000274 |
| **Customer** | Sterk B.V. |
| **Zoho amount** | EUR 1.540,15 |
| **Exact period 1** | 26700038 — EUR 1.133,39 (Uw ref: INV-000274) |
| **Exact period 2** | 26700044 — EUR 280,83 (Uw ref: INV-000274) |
| **Exact total** | EUR 1.414,22 |
| **Difference** | EUR 125,93 (Zoho > Exact) |
| **Exception type** | amount-mismatch |
| **Severity** | Medium |

### Likely cause
The invoice was split across period 1 (1.133,39) and period 2 (280,83). The combined Exact amount (1.414,22) does not equal the Zoho amount (1.540,15). The difference of EUR 125,93 may be a partial credit, line-level adjustment, or entry error.

### Owner
Finance Lead

### Required decision
1. Confirm which Exact entry is correct
2. Determine whether the EUR 125,93 difference is a legitimate adjustment or an error

### Required action
1. Open INV-000274 in Zoho Books — review line items and total
2. Open 26700038 (P1) and 26700044 (P2) in Exact — compare line items
3. If error: post correcting entry in the correct period
4. If intentional: document the reason

### Evidence needed for closure
- Side-by-side comparison of Zoho invoice lines vs Exact entry lines
- Correction entry (if error) or documented explanation (if intentional)
- Updated reconciliation

### Effect on CTRL-SI-001
Cannot sign off until the EUR 125,93 difference is explained or corrected.

---

## Exception 3: INV-000259 Bredenoord B.V. — Possible Duplicate

| Attribute | Value |
|---|---|
| **Invoice** | INV-000259 |
| **Customer** | Bredenoord B.V. |
| **Zoho amount** | EUR 1.861,37 |
| **Exact period 1** | 26700032 — EUR 1.861,37 (date 14-01-2026) |
| **Exact period 2** | 26700041 — EUR 1.861,37 (date 04-02-2026) |
| **Exception type** | possible-duplicate |
| **Severity** | High — if duplicate, revenue is double-booked |

### Likely cause
The same invoice appears in both period 1 and period 2 with identical amounts. The Zoho invoice date is 04-02-2026. The period 1 entry (26700032) has date 14-01-2026 — this was an early booking with an incorrect date. Period 2 entry (26700041) has the correct Zoho date.

### Owner
Finance Lead

### Required decision
1. Confirm this is a duplicate (same invoice entered twice)
2. Decide which entry to keep (period 2, correct date) and which to delete or reverse

### Required action
1. Open both entries in Exact Online and verify they reference the same invoice
2. Delete or reverse the duplicate entry
3. If period 1 entry is removed: period 1 reconciliation extra count drops from 9 to 8

### Evidence needed for closure
- Confirmation both entries reference the same invoice
- Deletion or reversal of the duplicate
- Updated reconciliation for both periods

### Effect on CTRL-SI-001
Cannot sign off for period 2 until duplicate status is confirmed and resolved. Also affects period 1 reconciliation.

---

## Exception 4: INV-000272 Gebr. van der Poel B.V. — Possible Duplicate

| Attribute | Value |
|---|---|
| **Invoice** | INV-000272 |
| **Customer** | Gebr. van der Poel B.V. |
| **Zoho amount** | EUR 754,79 |
| **Exact period 1** | 26700039 — EUR 754,79 (date 10-02-2026) |
| **Exact period 2** | 26700043 — EUR 754,79 (date 10-02-2026) |
| **Exception type** | possible-duplicate |
| **Severity** | High — if duplicate, revenue is double-booked |

### Likely cause
Same invoice appears in both period 1 and period 2 with identical amounts and identical dates. This is very likely a duplicate entry.

### Owner
Finance Lead

### Required decision
1. Confirm this is a duplicate
2. Decide which entry to keep (period 2) and which to delete or reverse (period 1)

### Required action
1. Open both entries in Exact Online
2. Delete or reverse the duplicate
3. If period 1 entry is removed: period 1 reconciliation extra count drops by 1

### Evidence needed for closure
- Confirmation both entries reference the same invoice
- Deletion or reversal of the duplicate
- Updated reconciliation for both periods

### Effect on CTRL-SI-001
Cannot sign off for period 2 until duplicate status is confirmed and resolved. Also affects period 1 reconciliation.

---

## Resolution Status Tracker

| # | Exception | Amount | Owner | Decision | Action | Status |
|---|---|---|---|---|---|---|
| 1 | INV-000269 AsfaltNu Amsterdam I | 86.394,00 | Thijs → FL | Pending | Create debtor, enter invoice | Open |
| 2 | INV-000274 Sterk amount mismatch | 125,93 diff | Finance Lead | Pending | Investigate line items | Open |
| 3 | INV-000259 Bredenoord duplicate | 1.861,37 | Finance Lead | Pending | Confirm + remove duplicate | Open |
| 4 | INV-000272 Gebr. van der Poel duplicate | 754,79 | Finance Lead | Pending | Confirm + remove duplicate | Open |

## CTRL-SI-001 Sign-Off Gate

CTRL-SI-001 for period 2 can be signed off when ALL of the following are true:
- [ ] Exception 1 resolved (INV-000269 entered in Exact)
- [ ] Exception 2 resolved (INV-000274 difference explained or corrected)
- [ ] Exception 3 resolved (INV-000259 duplicate confirmed and removed)
- [ ] Exception 4 resolved (INV-000272 duplicate confirmed and removed)
- [ ] Updated reconciliation shows all Zoho invoices accounted for
- [ ] Finance Lead sign-off on reconciliation
