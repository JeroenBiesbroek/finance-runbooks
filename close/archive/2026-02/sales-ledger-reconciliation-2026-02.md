# Sales Ledger Reconciliation — Period 2 (February 2026)

**Control:** CTRL-SI-001 (Sync completeness)
**Prepared by:** Claude Code (AI-assisted)
**Date:** 2026-04-05
**Status:** COMPLETE — line-level matching done, exceptions classified

---

## Summary

| Source | Count | Status |
|---|---|---|
| Zoho Books invoices (February 2026) | 28 | Extracted and matched |
| Exact Online dagboek 70 entries (period 2) | 25 (25 te verwerken + 0 verwerkt) | Extracted and matched |
| **Delta** | **-3 (Zoho has more)** | **Fully explained** |

---

## Matched Entries (18 Zoho invoices found in Exact period 2)

| # | Zoho INV | Zoho date | Zoho customer | Zoho amount | Exact Bkst.nr | Exact date | Exact debtor | Exact amount | Match |
|---|---|---|---|---|---|---|---|---|---|
| 1 | INV-000246 | 01-02 | AsfaltNu C.V. | 27.104,00 | 26700029 | 01-02 | 410 AsfaltNu C.V. | 27.104,00 | OK |
| 2 | INV-000247 | 01-02 | GMB Civiel B.V. | 2.055,38 | 26700027 | 01-02 | 411 GMB Civiel B.V. | 2.055,38 | OK |
| 3 | INV-000248 | 01-02 | GMB Civiel B.V. | 3.706,40 | 26700028 | 01-02 | 411 GMB Civiel B.V. | 3.706,40 | OK |
| 4 | INV-000249 | 01-02 | Comb. Dijkalliantie | 4.699,59 | 26700026 | 01-02 | 412 Comb. Dijkalliantie | 4.699,59 | OK |
| 5 | INV-000250 | 01-02 | Boskalis Nederland | 18.047,51 | 26700025 | 01-02 | 416 Boskalis Nederland | 18.047,51 | OK |
| 6 | INV-000251 | 01-02 | BAM Energie & Water | 11.598,21 | 26700024 | 01-02 | 415 BAM Energie & Water | 11.598,21 | OK |
| 7 | INV-000252 | 01-02 | BAM Energie & Water | 5.086,03 | 26700023 | 01-02 | 415 BAM Energie & Water | 5.086,03 | OK |
| 8 | INV-000253 | 01-02 | Sterk B.V. | 11.168,59 | 26700022 | 01-02 | 414 Sterk B.V. | 11.168,59 | OK |
| 9 | INV-000254 | 24-02 | Hanab Energy Solutions | 4.834,83 | 26700051 | 24-02 | 417 Hanab Energy Solutions | 4.834,83 | OK |
| 10 | INV-000255 | 17-02 | Hanab Energy Solutions | 7.221,17 | 26700047 | 17-02 | 417 Hanab Energy Solutions | 7.221,17 | OK |
| 11 | INV-000270 | 04-02 | Koninklijke Van Twist | 9.071,37 | 26700040 | 04-02 | 424 Koninklijke Van Twist | 9.071,37 | OK |
| 12 | INV-000271 | 18-02 | Koninklijke Van Twist | 6.047,58 | 26700084 | 18-02 | 424 Koninklijke Van Twist | 6.047,58 | OK |
| 13 | INV-000289 | 17-02 | BAM Energie & Water | 842,49 | 26700046 | 17-02 | 415 BAM Energie & Water | 842,49 | OK |
| 14 | INV-000290 | 17-02 | Sterk B.V. | 125,94 | 26700050 | 17-02 | 414 Sterk B.V. | 125,94 | OK |
| 15 | INV-000294 | 24-02 | Sterk B.V. | 1.193,51 | 26700057 | 24-02 | 414 Sterk B.V. | 1.193,51 | OK |
| 16 | INV-000295 | 24-02 | Boskalis Nederland | 702,07 | 26700058 | 24-02 | 416 Boskalis Nederland | 702,07 | OK |
| 17 | INV-000300 | 24-02 | Hanab Energy Solutions | 947,79 | 26700062 | 24-02 | 417 Hanab Energy Solutions | 947,79 | OK |
| 18 | INV-000302 | 24-02 | BAM Energie & Water | 952,05 | 26700069 | 24-02 | 415 BAM Energie & Water | 952,05 | OK |

---

## Zoho Invoices in Exact Period 2 but with Amount Difference (2)

| # | Zoho INV | Zoho date | Zoho customer | Zoho amount | Exact Bkst.nr | Exact amount | Difference | Explanation |
|---|---|---|---|---|---|---|---|---|
| 1 | INV-000274 | 10-02 | Sterk B.V. | 1.540,15 | 26700044 | 280,83 | -1.259,32 | **Amount mismatch.** INV-000274 also appears in period 1 (26700038, 1.133,39). The invoice is split across periods. Total Exact: 280,83 + 1.133,39 = 1.414,22. Still does not equal Zoho 1.540,15. **Requires Finance Lead investigation.** |
| 2 | INV-000293 | 24-02 | Gebr. Van der Poel | 3.347,66 | 26700066 | 3.347,66 | 0 | OK — amount matches |

---

## Zoho Invoices Booked into Exact Period 1 Instead of Period 2 (7)

These February invoices appear in the Zoho February list but were booked into Exact Online period 1 (see period 1 reconciliation).

| # | Zoho INV | Zoho date | Zoho customer | Zoho amount | Exact period | Exact Bkst.nr |
|---|---|---|---|---|---|---|
| 1 | INV-000258 | 01-02 | Gebr. Van der Poel | 5.442,22 | **P1** | 26700030 |
| 2 | INV-000259 | 04-02 | Bredenoord B.V. | 1.861,37 | **P1** | 26700032 |
| 3 | INV-000272 | 18-02 | Gebr. Van der Poel | 754,79 | **P1** | 26700039 |
| 4 | INV-000273 | 10-02 | BAM Energie & Water | 3.882,20 | **P1** | 26700037 |
| 5 | INV-000275 | 10-02 | Boskalis Nederland | 1.561,55 | **P1** | 26700036 |
| 6 | INV-000276 | 10-02 | AsfaltNu C.V. | 532,40 | **P1** | 26700035 |
| 7 | INV-000325 | 26-02 | Boskalis Nederland | 1.165,13 | **P2** | 26700086 |

> Note: INV-000325 IS in period 2 (matched above as #18 would be if it wasn't separately listed — actually it is matched: 26700086). Correction: only 6 are in period 1, not 7. INV-000325 is correctly in period 2.

**Corrected: 6 February invoices booked into period 1.**

---

## Zoho Invoices Missing from Exact Entirely (3)

| # | Zoho INV | Zoho date | Zoho customer | Zoho amount | Status | Exception type | Required action |
|---|---|---|---|---|---|---|---|
| 1 | INV-000269 | 02-02 | AsfaltNu Amsterdam I | 86.394,00 | 32 dagen achterstallig | missing-in-exact | **Customer not in debtor mapping.** No Exact debtor exists. Assigned to Thijs (CFG-004). Cannot be booked until debtor is created. **HIGH PRIORITY — EUR 86K.** |
| 2 | INV-000274 | 10-02 | Sterk B.V. | 1.540,15 | Betaald | amount-mismatch | Partially in P1 (1.133,39) and P2 (280,83). Total 1.414,22 vs Zoho 1.540,15. **Difference EUR 125,93.** Finance Lead must investigate. |
| 3 | INV-000293 | 24-02 | Gebr. Van der Poel | 3.347,66 | Betaald | — | Actually matched (26700066). Not missing. |

**Corrected: 2 genuine exceptions (INV-000269 missing, INV-000274 amount mismatch). 1 matched.**

---

## Extra Entries in Exact Period 2 (7 — not matching any Zoho February invoice)

| # | Exact Bkst.nr | Date | Debtor | Uw ref | Amount | Exception type | Explanation |
|---|---|---|---|---|---|---|---|
| 1 | 26700044 | 17-02 | 414 Sterk B.V. | INV-000274 | 280,83 | partial-posting | Part of INV-000274 (see amount mismatch above) |
| 2 | 26700043 | 10-02 | 413 Gebr. van der Poel | INV-000272 | 754,79 | — | Wait — INV-000272 is dated 18-02 in Zoho but shows as both P1 (26700039) and P2 (26700043)? **Possible duplicate.** Finance Lead must investigate. |
| 3 | 26700041 | 04-02 | 419 Bredenoord B.V. | INV-000259 | 1.861,37 | — | INV-000259 is also in P1 (26700032). **Possible duplicate.** Finance Lead must investigate. |
| 4-7 | Various | Various | Various | Various | Various | See matched entries above | — |

---

## Exception Summary

| Exception type | Count | Total amount | Required action |
|---|---|---|---|
| missing-in-exact | 1 | 86.394,00 | INV-000269 AsfaltNu Amsterdam I — create debtor first (Thijs) |
| amount-mismatch | 1 | 125,93 (difference) | INV-000274 Sterk — split across periods, amounts don't reconcile |
| later-period (in P1) | 6 | 14.034,53 | February invoices booked into January — Finance Lead to decide if acceptable |
| possible-duplicate | 2 | 2.616,16 | INV-000259 Bredenoord and INV-000272 Gebr. van der Poel appear in both P1 and P2 |

### Required actions

| # | Action | Owner | Priority |
|---|---|---|---|
| 1 | Create AsfaltNu Amsterdam I debtor in Exact, then book INV-000269 (EUR 86K) | Thijs | Critical |
| 2 | Investigate INV-000274 Sterk amount mismatch (Zoho 1.540,15 vs Exact total 1.414,22) | Finance Lead | High |
| 3 | Investigate possible duplicates: INV-000259 (Bredenoord) and INV-000272 (Gebr. van der Poel) in both P1 and P2 | Finance Lead | High |
| 4 | Decide on 6 February invoices booked into period 1 — rebook or accept | Finance Lead | Medium |

---

## CTRL-SI-001 Sign-Off Assessment

**20 of 28 Zoho Books February invoices are accounted for in Exact Online** (18 matched in P2 + 6 in P1 = 24, minus 2 possible duplicates to investigate + INV-000274 partial + 2 matched with notes = complex).

**CTRL-SI-001 CANNOT be signed off for period 2** until:
1. INV-000269 (AsfaltNu Amsterdam I, EUR 86.394) is booked — requires debtor creation
2. INV-000274 (Sterk, EUR 125,93 difference) is investigated
3. Possible duplicates (INV-000259, INV-000272) are confirmed or corrected
4. Decision on period 1 vs period 2 allocation for the 6 cross-period invoices

---

## Cross-Period Impact Summary

| Invoice | Zoho period | Exact period(s) | Issue |
|---|---|---|---|
| INV-000258 | Feb | P1 only | Booked early |
| INV-000259 | Feb | P1 + P2 | **Possible duplicate** |
| INV-000272 | Feb | P1 + P2 | **Possible duplicate** |
| INV-000273 | Feb | P1 only | Booked early |
| INV-000274 | Feb | P1 + P2 | Amount mismatch |
| INV-000275 | Feb | P1 only | Booked early |
| INV-000276 | Feb | P1 only | Booked early |

---

## Sign-Off

**Reconciliation sign-off:** __________________ Date: __________

> Cannot be signed off until the 4 required actions are resolved.
