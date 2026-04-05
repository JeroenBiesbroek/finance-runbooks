# Sales Ledger Reconciliation — Period 2 (February 2026)

**Control:** CTRL-SI-001 (Sync completeness)
**Prepared by:** Claude Code (AI-assisted)
**Date:** 2026-04-05
**Status:** Zoho side populated. Exact side blocked — entries not verwerkt.

---

## Summary

| Source | Count | Status |
|---|---|---|
| Zoho Books invoices (February 2026) | 28 | Extracted |
| Exact Online dagboek 70 entries (period 2) | 25 (25 te verwerken + 0 verwerkt) | Not extractable at line level — entries must be verwerkt first |
| **Delta** | **-3 (Zoho has more)** | |

## Blocker

Same as period 1: Exact Online dagboek 70 line-level detail requires entries to be verwerkt before Transacties zoeken returns results.

**Required action:** Finance Lead must process (verwerken) all dagboek 70 period 2 entries.

---

## Zoho Books — February 2026 Invoices (28)

| # | Date | Invoice nr | Order/reference | Customer | Amount (incl BTW) | Status |
|---|---|---|---|---|---|---|
| 1 | 01-02-2026 | INV-000258 | POE24200 | Gebr. Van der Poel B.V. | 5.442,22 | Betaald |
| 2 | 01-02-2026 | INV-000252 | 4540046514 | BAM Energie & Water B.V. | 5.086,03 | Betaald |
| 3 | 01-02-2026 | INV-000251 | 4540046524 | BAM Energie & Water B.V. | 11.598,21 | Betaald |
| 4 | 01-02-2026 | INV-000247 | A3300 / 1000-51704 | GMB Civiel B.V. | 2.055,38 | Betaald |
| 5 | 01-02-2026 | INV-000248 | A3033 / 1000-70383 | GMB Civiel B.V. | 3.706,40 | Betaald |
| 6 | 01-02-2026 | INV-000246 | TD-OFF-20049 / 20073 | AsfaltNu C.V. | 27.104,00 | Betaald |
| 7 | 01-02-2026 | INV-000250 | 1226050021 / 12E032858 MeMa | Boskalis Nederland B.V. | 18.047,51 | Betaald |
| 8 | 01-02-2026 | INV-000253 | IO260119/23.022.09B/ON260080 | Sterk B.V. | 11.168,59 | Betaald |
| 9 | 01-02-2026 | INV-000249 | IO8042500397 | Comb. Dijkalliantie Neder-Betuwe v.o.f. | 4.699,59 | Betaald |
| 10 | 02-02-2026 | INV-000269 | ANA I - Biogas | AsfaltNu Amsterdam I | 86.394,00 | 32 dagen achterstallig |
| 11 | 04-02-2026 | INV-000259 | Powerbox Testgas | Bredenoord B.V. | 1.861,37 | Betaald |
| 12 | 04-02-2026 | INV-000270 | PO12600073 | Koninklijke Van Twist B.V. | 9.071,37 | Betaald |
| 13 | 10-02-2026 | INV-000276 | TD-OFF-20049 / 20073 | AsfaltNu C.V. | 532,40 | Betaald |
| 14 | 10-02-2026 | INV-000273 | 4540048414 | BAM Energie & Water B.V. | 4.759,79 | Betaald |
| 15 | 10-02-2026 | INV-000274 | IO260234 / 23.022.03 | Sterk B.V. | 1.540,15 | Betaald |
| 16 | 10-02-2026 | INV-000275 | 1226070015 / 12E032858 | Boskalis Nederland B.V. | 1.561,55 | Betaald |
| 17 | 17-02-2026 | INV-000255 | IO0826001398 / A.P. Deunhouwer | Hanab Energy Solutions B.V. | 7.221,17 | Betaald |
| 18 | 17-02-2026 | INV-000289 | 4540048981 | BAM Energie & Water B.V. | 842,49 | Betaald |
| 19 | 17-02-2026 | INV-000290 | IO260234 / 23.022.03 | Sterk B.V. | 125,94 | Betaald |
| 20 | 18-02-2026 | INV-000272 | POE24200 | Gebr. Van der Poel B.V. | 2.239,30 | Betaald |
| 21 | 18-02-2026 | INV-000271 | PO12600073 | Koninklijke Van Twist B.V. | 6.047,58 | 32 dagen achterstallig |
| 22 | 24-02-2026 | INV-000293 | POE24200 | Gebr. Van der Poel B.V. | 3.347,66 | Betaald |
| 23 | 24-02-2026 | INV-000254 | IO826001401 / A.P. Deunhouwer | Hanab Energy Solutions B.V. | 4.834,83 | Betaald |
| 24 | 24-02-2026 | INV-000300 | IO0826001403 / A.P. Deunhouwer | Hanab Energy Solutions B.V. | 947,79 | Betaald |
| 25 | 24-02-2026 | INV-000302 | 4540052929 | BAM Energie & Water B.V. | 952,05 | Betaald |
| 26 | 24-02-2026 | INV-000295 | 1226090007 / 12E032858 Mema | Boskalis Nederland B.V. | 702,07 | Betaald |
| 27 | 24-02-2026 | INV-000294 | IO260234 / 23.022.03 | Sterk B.V. | 1.193,51 | 10 dagen achterstallig |
| 28 | 26-02-2026 | INV-000325 | 1226090050 / 12E032858 Mema | Boskalis Nederland B.V. | 1.165,13 | 8 dagen achterstallig |

### Notable: INV-000269 (AsfaltNu Amsterdam I)

This is the EUR 86.394 invoice for a customer that is **unmatched in the debtor mapping** (CFG-004 exception — assigned to Thijs). This invoice may be one of the 3 missing from Exact Online period 2 if the debtor mapping doesn't exist yet.

---

## Exact Online — Dagboek 70 Period 2 (25 entries)

**Status: LINE-LEVEL DETAIL BLOCKED — all 25 entries are te verwerken (0 verwerkt)**

After Finance Lead processes all entries, populate this table:

| # | Date | Bkst.nr | GL account | Description | Debtor | Amount (Debet/Credit) | Match to Zoho | Exception type |
|---|---|---|---|---|---|---|---|---|
| 1 | | | | | | | | |
| ... | | | | | | | | |
| 25 | | | | | | | | |

---

## Likely Cause of -3 Delta (Zoho 28 > Exact 25)

Based on the debtor mapping analysis (CFG-004), the most likely cause is:

| Likely missing invoice | Customer | Amount | Reason |
|---|---|---|---|
| INV-000269 | AsfaltNu Amsterdam I | 86.394,00 | **Customer not mapped** in debtor mapping — no Exact debtor exists. Assigned to Thijs. |
| Unknown | Unknown | Unknown | 2 additional invoices to be identified after verwerken |

This hypothesis can be verified after dagboek 70 entries are processed and line-level matching is possible.

---

## Matching (to be completed after verwerken)

| Match status | Count | Notes |
|---|---|---|
| Matched (Zoho = Exact) | — | To be determined |
| In Zoho, missing in Exact | — | Expected: at least 3 (including INV-000269) |
| In Exact, missing in Zoho | — | To be determined |

## Exception Classification

Same classification scheme as period 1 reconciliation.

---

## Sign-Off Condition

Phase 1 sales invoice control (CTRL-SI-001) can be signed off when:
1. All dagboek 70 entries are verwerkt and line-level detail is extracted
2. Every Zoho invoice is matched to an Exact entry (or exception documented)
3. Every Exact entry without a Zoho match is classified by exception type
4. Each exception has an owner and required action
5. Material exceptions (> EUR 1.000) are individually investigated
6. Finance Lead approves the reconciliation
