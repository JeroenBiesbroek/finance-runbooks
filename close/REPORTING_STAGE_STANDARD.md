# Reporting Stage Standard — Bronze / Silver / Gold

**Owner:** Finance Lead
**Version:** v1.0 — 2026-04-06
**Status:** Active
**Applies to:** Every governed month-end close
**Builds on:** `MONTH_END_CLOSE_OPERATING_MODEL.md`, `MONTH_END_REPORTING_DOSSIER_STANDARD.md`

---

## Purpose

Each close period progresses through three reporting stages. The stages allow the close to produce value early — Bronze creates the dossier and captures known issues before all data is final — while maintaining a clear path to a stakeholder-ready Gold package.

Work done in each stage is additive. Silver builds on Bronze. Gold builds on Silver. No work is duplicated.

---

## Stage Overview

| Stage | Purpose | When | Sign-off |
|---|---|---|---|
| **Bronze** | First controlled close round — dossier created, known data populated, all open items captured | As soon as Phase 1 data extraction is complete | Finance Lead |
| **Silver** | Checked and reconciled internal version — all data processed, specifications populated, reconciliations done | After Phase 2 + Phase 3 completion | Finance Lead |
| **Gold** | Final external/stakeholder-ready version — period locked, dossier complete, archived | After Phase 4 completion | Finance Lead + CFO |

---

## Bronze — First Controlled Close

### Purpose
Get the reporting dossier in place and populate it as far as safely possible using available data. All items that cannot yet be completed are captured in the open-items register with clear owners, actions, and stage-blocking classification.

### Minimum Required Contents

| # | Deliverable | Source | Bronze requirement |
|---|---|---|---|
| 1 | Close checklist | Phase 1 tasks | Phase 1 tasks executed. Results documented. |
| 2 | Sales ledger reconciliation | CTRL-SI-001 | Zoho-to-Exact count comparison complete. Matches and exceptions documented. |
| 3 | Dossier shell files | Templates | All 6 dossier components instantiated for the period (BS spec, P&L spec, analytical review, evidence index, exception log, close-package-index). |
| 4 | Evidence index | Template | Initialized. Phase 1 evidence items filled. Remaining items tracked with status. |
| 5 | Exception / open-items register | Template | All known exceptions and open items logged with owner, action, deadline, and stage-blocking level. |
| 6 | Known data populated | Exact Online + Zoho | Dagboek summaries, invoice counts, verwerken status, any available balances entered into spec shells. |

### What May Still Be Open at Bronze
- Verwerken incomplete (entries unprocessed in Exact)
- CTRL-SI-001 confirmations pending
- Exception resolutions pending (Finance Lead / Thijs / external)
- Phase 2 journals not yet posted
- Trial balance not yet available
- BS/P&L specifications not yet populated with amounts
- Analytical review not yet started
- Reconciliations not yet done

### What Blocks Advancing to Silver
All items in the open-items register classified as `blocks-silver` must be resolved.

At minimum:
- [ ] All dagboek entries verwerkt (0 te verwerken)
- [ ] All close-blocking exceptions resolved or accepted with documented justification
- [ ] Phase 1 signed off
- [ ] Phase 2 completed and signed off (journals, accruals, depreciation)
- [ ] Trial balance exported

### Bronze Sign-Off

**Criteria:**
1. All Bronze minimum contents present
2. Open-items register complete — every known blocker has an owner and action
3. No undocumented issues

**Approver:** Finance Lead

---

## Silver — Checked and Reconciled

### Purpose
Produce a fully checked internal reporting version. All data is processed, all specifications are populated with actual numbers, all reconciliations are completed, and the analytical review is done. This is the version the Finance Lead uses for internal management reporting.

### Minimum Required Contents (additive to Bronze)

| # | Deliverable | Silver requirement |
|---|---|---|
| 1 | Close checklist | Phases 1-3 completed and signed off |
| 2 | Balance sheet specifications | All mandatory account areas populated with period-end balances from trial balance. Fixed asset rollforward complete. Bank reconciled. Debtor/creditor aging done. |
| 3 | P&L specifications | All categories populated. Revenue by category and customer top-5. Gross margin calculated. Depreciation and salary reconciliations done. |
| 4 | Analytical review | All 5 mandatory comparisons completed. All variances exceeding thresholds explained. |
| 5 | Reconciliations | Bank reconciliation complete (GL vs statement). VAT reconciliation complete (GL vs BTW-aangifte). |
| 6 | Evidence index | All Phase 1-3 evidence items present and referenced. |
| 7 | Exception log | All close-blocking exceptions resolved. Remaining items either resolved or accepted as immaterial with justification. |
| 8 | Open-items register | All `blocks-silver` items resolved. Any remaining items reclassified to `blocks-gold` or `carry-forward`. |

### What May Still Be Open at Silver
- CFO review/approval pending
- Period not yet locked in Exact Online
- Dossier not yet archived
- Immaterial exceptions accepted but not yet formally closed
- Improvement issues not yet created in GitHub
- Lessons learned not yet finalized

### What Blocks Advancing to Gold
All items in the open-items register classified as `blocks-gold` must be resolved.

At minimum:
- [ ] Phase 3 signed off
- [ ] Dossier completeness gate passed (per `MONTH_END_REPORTING_DOSSIER_STANDARD.md`)
- [ ] All material exceptions resolved or accepted with CFO approval
- [ ] No unexplained variances exceeding materiality thresholds

### Silver Sign-Off

**Criteria:**
1. All Silver minimum contents present
2. Dossier suitable for internal management reporting
3. Open-items register: no `blocks-silver` items remaining

**Approver:** Finance Lead

---

## Gold — Final / Stakeholder-Ready

### Purpose
Produce the final close package: period locked in Exact, dossier complete per standard, archived in GitHub. This is the version that would be shared with external parties (accountant, auditor, stakeholders) if requested.

### Minimum Required Contents (additive to Silver)

| # | Deliverable | Gold requirement |
|---|---|---|
| 1 | Close checklist | All 4 phases completed and signed off |
| 2 | CFO approval | Obtained (if required by materiality or policy) |
| 3 | Period lock | Period status = "Closed" in Exact Online. Screenshot as evidence. |
| 4 | Exception log | All items resolved or formally accepted. No open items. |
| 5 | Evidence index | All 29 evidence items present. Every specification references its evidence. |
| 6 | Lessons learned | Documented. Improvement issues created in GitHub. |
| 7 | Dossier archived | All files committed to `close/archive/YYYY-MM/` via PR and merged. |
| 8 | Open-items register | Empty — all items resolved. Any carry-forward items moved to next period's Bronze register. |

### What May Still Be Open at Gold
Nothing. Gold is complete.

### Gold Sign-Off

**Criteria:**
1. Dossier complete per `MONTH_END_REPORTING_DOSSIER_STANDARD.md`
2. Period locked in Exact Online
3. All exceptions resolved or formally accepted
4. Archived in GitHub

**Approver:** Finance Lead + CFO (if material exceptions exist)

---

## Stage Progression Rules

1. **Stages are sequential:** Bronze → Silver → Gold. No stage may be skipped.
2. **Work is additive:** Each stage adds to the prior stage. No duplication.
3. **Open items carry forward, not block:** Bronze captures all issues. Only items classified as `blocks-silver` prevent Silver. Only `blocks-gold` items prevent Gold.
4. **Each period tracks its own stage:** Period 1 and period 2 progress independently.
5. **Stage status lives in the close-package-index** for each period.
6. **Stage transitions require sign-off** in the close checklist.

---

## Open-Items Register

Each period maintains an open-items register (`open-items-register-YYYY-MM.md`) that tracks all unresolved work. This is the single controlled structure for items that cannot be completed in the current stage.

### Item Classification

| Classification | Meaning | Effect |
|---|---|---|
| `blocks-silver` | Must be resolved before Silver can be achieved | Prevents Silver sign-off |
| `blocks-gold` | Must be resolved before Gold can be achieved | Prevents Gold sign-off |
| `carry-forward` | Does not block current period close; carried to next period | Moved to next period's Bronze register |
| `resolved` | Completed | Moved to resolved section with date and resolution |

### Required Fields Per Item

| Field | Purpose |
|---|---|
| ID | Sequential per period (OI-P1-001, OI-P2-001) |
| Description | What is the issue |
| Amount | Financial impact (if applicable) |
| Owner | Who must resolve it |
| Required action | What must be done |
| Classification | `blocks-silver` / `blocks-gold` / `carry-forward` |
| Source | Where this was identified (Phase, evidence ID, exception #) |
| Created | Date identified |
| Target | When it should be resolved |

---

## How Stages Map to Close Phases

| Close phase | Stage work |
|---|---|
| Phase 1 (Pre-close) | **Bronze entry.** Data extraction, reconciliation, exception capture, dossier shell creation. |
| Phase 1 sign-off | **Bronze exit.** All Bronze criteria met. Open-items register complete. |
| Phase 2 (Controlled close) | Silver progression. Journals, accruals, depreciation. |
| Phase 3 (Review close) | **Silver exit.** Specifications populated, analytical review done, reconciliations complete. |
| Phase 4 (Final close) | **Gold exit.** Period locked, dossier archived, all items closed. |

> Note: Bronze can be signed off even when Phase 1 has pending confirmations — as long as those pending items are captured in the open-items register with `blocks-silver` classification.

---

## Relationship to Existing Standards

This standard extends but does not replace:
- **Close operating model:** The 4-phase structure remains. Stages are an overlay that allow partial progress to be recognized.
- **Reporting dossier standard:** The dossier completeness gate remains the Silver → Gold transition gate. Bronze creates the dossier structure; Silver populates it; Gold finalizes it.
- **Exception handling:** Existing exception types and paths remain. The open-items register adds stage-blocking classification on top.
