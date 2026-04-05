# Sales Ledger Reconciliation — Period 1 (January 2026)

**Control:** CTRL-SI-001 (Sync completeness)
**Prepared by:** Claude Code (AI-assisted)
**Date:** 2026-04-05
**Status:** Zoho side populated. Exact side blocked — entries not verwerkt.

---

## Summary

| Source | Count | Status |
|---|---|---|
| Zoho Books invoices (January 2026) | 20 | Extracted |
| Exact Online dagboek 70 entries (period 1) | 29 (17 te verwerken + 12 verwerkt) | Not extractable at line level — entries must be verwerkt first |
| **Delta** | **+9 (Exact has more)** | |

## Blocker

Exact Online dagboek 70 line-level detail is not available via Transacties zoeken until entries are fully processed (verwerkt) to the GL. The Boekingen Overzicht shows 29 total entries but individual transaction detail is blocked.

**Required action:** Finance Lead must process (verwerken) all dagboek 70 period 1 entries. After processing, the line-level detail becomes available for matching.

---

## Zoho Books — January 2026 Invoices (20)

| # | Date | Invoice nr | Order/reference | Customer | Amount (incl BTW) | Status |
|---|---|---|---|---|---|---|
| 1 | 01-01-2026 | INV-000218 | A3033 / 1000-70383 | GMB Civiel B.V. | 3.603,22 | Betaald |
| 2 | 01-01-2026 | INV-000216 | TD-OFF-20049 I 20073 | AsfaltNu C.V. | 26.378,00 | Betaald |
| 3 | 01-01-2026 | INV-000217 | A3300 / 1000-51704 | GMB Civiel B.V. | 1.992,47 | Betaald |
| 4 | 01-01-2026 | INV-000221 | TD-OFF104 | BAM Energie & Water B.V. | 11.309,87 | Betaald |
| 5 | 01-01-2026 | INV-000222 | 4540044540 | BAM Energie & Water B.V. | 4.960,19 | Betaald |
| 6 | 01-01-2026 | INV-000226 | POE24200 | Gebr. Van der Poel B.V. | 5.306,24 | Betaald |
| 7 | 01-01-2026 | INV-000223 | ON260049 / 23.022.09B | Sterk B.V. | 2.475,42 | Betaald |
| 8 | 01-01-2026 | INV-000220 | 1226010008 | Boskalis Nederland B.V. | 19.145,83 | Betaald |
| 9 | 01-01-2026 | INV-000219 | 20035 / A3034 IJzendoorn | Comb. Dijkalliantie Neder-Betuwe v.o.f. | 4.574,13 | Betaald |
| 10 | 05-01-2026 | INV-000243 | 1226030008 | Boskalis Nederland B.V. | 419,34 | Betaald |
| 11 | 06-01-2026 | INV-000262 | 4540044905 | BAM Energie & Water B.V. | 838,70 | Betaald |
| 12 | 09-01-2026 | INV-000263 | 1226020035 | Boskalis Nederland B.V. | 698,91 | Betaald |
| 13 | 09-01-2026 | INV-000242 | IO825007550 / Robin Zijlmans | Hanab Energy Solutions B.V. | 29.306,20 | Betaald |
| 14 | 12-01-2026 | INV-000268 | 4540046378 | BAM Energie & Water B.V. | 1.356,23 | Betaald |
| 15 | 12-01-2026 | INV-000267 | POE24200 | Gebr. Van der Poel B.V. | 678,12 | Betaald |
| 16 | 13-01-2026 | INV-000265 | IO260118/23.022.03/ON260079 | Sterk B.V. | 374,43 | Betaald |
| 17 | 13-01-2026 | INV-000266 | 1226030025 | Boskalis Nederland B.V. | 748,87 | Betaald |
| 18 | 14-01-2026 | INV-000261 | Testgas | Genpower B.V. | 1.354,18 | Betaald |
| 19 | 14-01-2026 | INV-000260 | Testgas | Koninklijke Van Twist B.V. | 2.768,87 | Betaald |
| 20 | 18-01-2026 | INV-000264 | — | Kisjes Transport B.V. | 4.313,65 | 47 dagen achterstallig |

---

## Exact Online — Dagboek 70 Period 1 (29 entries)

**Status: LINE-LEVEL DETAIL BLOCKED — entries must be verwerkt**

After Finance Lead processes all entries, populate this table:

| # | Date | Bkst.nr | GL account | Description | Debtor | Amount (Debet/Credit) | Match to Zoho | Exception type |
|---|---|---|---|---|---|---|---|---|
| 1 | | | | | | | | |
| ... | | | | | | | | |
| 29 | | | | | | | | |

---

## Matching (to be completed after verwerken)

| Match status | Count | Notes |
|---|---|---|
| Matched (Zoho = Exact) | — | To be determined |
| In Zoho, missing in Exact | — | To be determined |
| In Exact, missing in Zoho | — | To be determined (likely explains the +9 delta) |

## Exception Classification (to be completed)

| Exception type | Definition |
|---|---|
| missing-in-exact | Invoice in Zoho Books but no corresponding entry in dagboek 70 |
| extra-in-exact | Entry in dagboek 70 with no corresponding Zoho invoice |
| credit-note | Credit note booked in dagboek 70 (negative amount) |
| correction | Corrective entry (reversal + re-entry) |
| prior-period | Entry dated in prior fiscal year but booked in period 1 |
| later-period | Zoho invoice dated in January but booked in a later Exact period |
| manual-journal | Manual entry not originating from Zoho sync |
| duplicate | Duplicate entry |
| unknown | Requires investigation |

---

## Sign-Off Condition

Phase 1 sales invoice control (CTRL-SI-001) can be signed off when:
1. All dagboek 70 entries are verwerkt and line-level detail is extracted
2. Every Zoho invoice is matched to an Exact entry (or exception documented)
3. Every Exact entry without a Zoho match is classified by exception type
4. Each exception has an owner and required action
5. Material exceptions (> EUR 1.000) are individually investigated
6. Finance Lead approves the reconciliation
