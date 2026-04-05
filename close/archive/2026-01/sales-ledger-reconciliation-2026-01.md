# Sales Ledger Reconciliation — Period 1 (January 2026)

**Control:** CTRL-SI-001 (Sync completeness)
**Prepared by:** Claude Code (AI-assisted)
**Date:** 2026-04-05
**Status:** COMPLETE — line-level matching done, exceptions classified

---

## Summary

| Source | Count | Status |
|---|---|---|
| Zoho Books invoices (January 2026) | 20 | Extracted and matched |
| Exact Online dagboek 70 entries (period 1) | 29 (17 te verwerken + 12 verwerkt) | Extracted and matched |
| **Delta** | **+9 (Exact has more)** | **Fully explained** |

---

## Matched Entries (20 — all Zoho invoices found in Exact)

| # | Zoho INV | Zoho date | Zoho customer | Zoho amount | Exact Bkst.nr | Exact date | Exact debtor | Exact amount | Exact period | Match |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | INV-000216 | 01-01 | AsfaltNu C.V. | 26.378,00 | 26700003 | 01-01 | 410 AsfaltNu C.V. | 26.378,00 | P1 te verw | OK |
| 2 | INV-000217 | 01-01 | GMB Civiel B.V. | 1.992,47 | 26700004 | 01-01 | 411 GMB Civiel B.V. | 1.992,47 | P1 verwerkt | OK |
| 3 | INV-000218 | 01-01 | GMB Civiel B.V. | 3.603,22 | 26700005 | 01-01 | 411 GMB Civiel B.V. | 3.603,22 | P1 verwerkt | OK |
| 4 | INV-000219 | 01-01 | Comb. Dijkalliantie | 4.574,13 | 26700006 | 01-01 | 412 Comb. Dijkalliantie | 4.574,13 | P1 verwerkt | OK |
| 5 | INV-000220 | 01-01 | Boskalis Nederland | 19.145,83 | 26700011 | 01-01 | 416 Boskalis Nederland | 19.145,83 | P1 verwerkt | OK |
| 6 | INV-000221 | 01-01 | BAM Energie & Water | 11.309,87 | 26700009 | 01-01 | 415 BAM Energie & Water | 11.309,87 | P1 verwerkt | OK |
| 7 | INV-000222 | 01-01 | BAM Energie & Water | 4.960,19 | 26700010 | 01-01 | 415 BAM Energie & Water | 4.960,19 | P1 verwerkt | OK |
| 8 | INV-000223 | 01-01 | Sterk B.V. | 2.475,42 | 26700008 | 01-01 | 414 Sterk B.V. | 2.475,42 | P1 te verw | OK |
| 9 | INV-000226 | 01-01 | Gebr. Van der Poel | 5.306,24 | 26700007 | 01-01 | 413 Gebr. van der Poel | 5.306,24 | P1 verwerkt | OK |
| 10 | INV-000242 | 09-01 | Hanab Energy Solutions | 29.306,20 | 26700016 | 31-12-2025 | 417 Hanab Energy Solutions | 29.306,20 | P1 verwerkt | OK — date diff: Zoho 09-01, Exact 31-12-2025 |
| 11 | INV-000243 | 05-01 | Boskalis Nederland | 419,34 | 26700013 | 12-01 | 416 Boskalis Nederland | 419,34 | P1 verwerkt | OK — date diff |
| 12 | INV-000260 | 14-01 | Koninklijke Van Twist | 2.768,87 | 26700048 | 14-01 | 424 Koninklijke Van Twist | 2.768,87 | P1 te verw | OK |
| 13 | INV-000261 | 14-01 | Genpower B.V. | 1.354,18 | 26700033 | 14-01 | 421 Genpower B.V. | 1.354,18 | P1 te verw | OK |
| 14 | INV-000262 | 06-01 | BAM Energie & Water | 838,70 | 26700015 | 06-01 | 415 BAM Energie & Water | 838,70 | P1 verwerkt | OK |
| 15 | INV-000263 | 09-01 | Boskalis Nederland | 698,91 | 26700014 | 09-01 | 416 Boskalis Nederland | 698,91 | P1 verwerkt | OK |
| 16 | INV-000264 | 18-01 | Kisjes Transport B.V. | 4.313,65 | 26700034 | 18-01 | 56 Kisjes Transport & Verhuur | 4.313,65 | P1 te verw | OK — name diff |
| 17 | INV-000265 | 13-01 | Sterk B.V. | 374,43 | 26700019 | 26-01 | 414 Sterk B.V. | 374,43 | P1 te verw | OK — date diff |
| 18 | INV-000266 | 13-01 | Boskalis Nederland | 748,87 | 26700020 | 13-01 | 416 Boskalis Nederland | 748,87 | P1 te verw | OK |
| 19 | INV-000267 | 12-01 | Gebr. Van der Poel | 678,12 | 26700042 | 12-01 | 413 Gebr. van der Poel | 678,12 | P1 te verw | OK |
| 20 | INV-000268 | 12-01 | BAM Energie & Water | 1.356,23 | 26700021 | 26-01 | 415 BAM Energie & Water | 1.356,23 | P1 te verw | OK — date diff |

**Result: All 20 Zoho Books January invoices matched to Exact Online dagboek 70 entries. Zero missing.**

---

## Extra Entries in Exact (9 — not in Zoho January)

| # | Exact Bkst.nr | Date | Debtor | Uw ref | Amount | Debet/Credit | Exception type | Explanation |
|---|---|---|---|---|---|---|---|---|
| 1 | 26700017 | 20-01-2026 | 81 Buse Gas B.V. | Transportkosten Week 47 | 1.612,24 | **Credit** | credit-note | Credit note for non-Zoho customer. Buse Gas is not in Zoho Books. Entered directly in Exact. |
| 2 | 26700018 | 22-01-2026 | 414 Sterk B.V. | IO260054 | 663,96 | Debet | manual-entry | No matching Zoho INV. Reference "IO260054" is a project order, not a Zoho invoice number. Entered directly in Exact. |
| 3 | 26700032 | 14-01-2026 | 419 Bredenoord B.V. | INV-000259 | 1.861,37 | Debet | later-period | **Zoho INV-000259 is dated 04-02-2026** (February). Booked into Exact period 1 with January date. Cross-period posting. |
| 4 | 26700030 | 01-02-2026 | 413 Gebr. van der Poel | INV-000258 | 5.442,22 | Debet | later-period | **Zoho INV-000258 is dated 01-02-2026** (February). Booked into Exact period 1. Cross-period posting. |
| 5 | 26700039 | 10-02-2026 | 413 Gebr. van der Poel | INV-000272 | 754,79 | Debet | later-period | **Zoho INV-000272 dated 18-02-2026.** Booked into period 1. |
| 6 | 26700038 | 10-02-2026 | 414 Sterk B.V. | INV-000274 | 1.133,39 | Debet | later-period | **Zoho INV-000274 dated 10-02-2026.** Booked into period 1. |
| 7 | 26700037 | 10-02-2026 | 415 BAM Energie & Water | INV-000273 | 3.882,20 | Debet | later-period | **Zoho INV-000273 dated 10-02-2026.** Booked into period 1. |
| 8 | 26700036 | 10-02-2026 | 416 Boskalis Nederland | INV-000275 | 1.561,55 | Debet | later-period | **Zoho INV-000275 dated 10-02-2026.** Booked into period 1. |
| 9 | 26700035 | 10-02-2026 | 410 AsfaltNu C.V. | INV-000276 | 532,40 | Debet | later-period | **Zoho INV-000276 dated 10-02-2026.** Booked into period 1. |

---

## Exception Analysis

| Exception type | Count | Total amount | Impact |
|---|---|---|---|
| later-period | 7 | 15.167,92 | February invoices booked into January. These will appear as "extra" in period 1 and "missing" in period 2. |
| credit-note | 1 | -1.612,24 | Legitimate credit note for non-Zoho customer. Does not affect Zoho reconciliation. |
| manual-entry | 1 | 663,96 | Direct Exact entry, not from Zoho. Legitimate if authorized. Finance Lead to confirm. |

### Root cause of +9 delta

The +9 delta is fully explained:
- **7 February Zoho invoices booked into Exact period 1** (later-period postings)
- **1 credit note** for Buse Gas B.V. (non-Zoho customer)
- **1 manual entry** (IO260054 for Sterk B.V., no Zoho origin)

### Required actions

| # | Action | Owner | Priority |
|---|---|---|---|
| 1 | Confirm whether the 7 later-period postings should be rebooked to period 2, or if period 1 booking is intentional | Finance Lead | High |
| 2 | Confirm IO260054 (Sterk, 663,96) is an authorized direct entry | Finance Lead | Medium |
| 3 | Confirm Buse Gas credit note is legitimate | Finance Lead | Low |

---

## CTRL-SI-001 Sign-Off Assessment

**All 20 Zoho Books January invoices are present in Exact Online dagboek 70.** Sync completeness = 100%.

The 9 extra entries are explained: 7 are February invoices booked early, 1 credit note, 1 manual entry. None represent missing Zoho invoices.

**CTRL-SI-001 can be signed off for period 1** once Finance Lead confirms:
1. The 7 later-period postings are acceptable or will be rebooked
2. The manual entry IO260054 is authorized

---

## Sign-Off

**Reconciliation sign-off:** __________________ Date: __________
