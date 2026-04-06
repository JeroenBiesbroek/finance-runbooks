# Month-End Close Operating Model

**Owner:** Finance Lead
**System of record:** Exact Online
**Frequency:** Monthly
**Start:** Business day -5 relative to month-end
**Target completion:** Business day +3 of next month

## Phase Overview

| Phase | Timing | Owner | Purpose |
|---|---|---|---|
| 1. Pre-close | BD -5 to BD -3 | Finance Lead | Completeness verification |
| 2. Controlled close | BD -2 to BD -1 | Finance Lead | Journals, accruals, depreciation |
| 3. Review close | BD +1 to BD +2 | Finance Lead | Reviews, reconciliations, controls |
| 4. Final close | BD +3 | Finance Lead + CFO | Approval, period lock, archival |

---

## Phase 1: Pre-Close

**Owner:** Finance Lead
**Timing:** BD -5 to BD -3

### Entry Criteria
- Previous period is closed and archived
- Close checklist created for the period (use `templates/close-checklist-template.md`)
- Task owners assigned
- Target close date confirmed

### Tasks

| # | Task | Owner | Source system |
|---|---|---|---|
| 1.1 | Verify all sales invoices synced from Zoho Books to Exact | Technical Lead | Exact + Zoho Books |
| 1.2 | Review and resolve sales invoice sync exceptions | Finance Lead | GitHub exceptions |
| 1.3 | Verify all purchase invoices processed | Finance Lead | Exact Online |
| 1.4 | Verify all bank statements imported through month-end | Finance Lead | Exact Online |
| 1.5 | Review and match unmatched bank transactions | Finance Lead | Exact Online |
| 1.6 | Review all open exceptions; resolve or defer with documentation | Finance Lead | GitHub exceptions |

### Exit Criteria
- All source data complete in Exact Online (sales invoices, purchases, bank)
- All dagboek entries for the period processed (verwerkt) — 0 te verwerken
- All exceptions triaged: resolved or deferred with documented justification
- Finance Lead sign-off on pre-close

### Required Evidence
- Sync report: Zoho Books invoice count (Verkoop > Facturen) = Exact Online dagboek 70 count
- Bank statement import confirmation (last import date per account >= period end date)
- Verwerken confirmation: screenshot or count showing 0 "te verwerken" entries for the period
- Exception register status (open/deferred/resolved counts)
- Pre-close sign-off (name + date)

### Exception Path
- If sales invoice sync completeness < 100%: document missing items, assess materiality, defer if immaterial (Finance Lead), escalate if material (CFO)
- If bank statements incomplete: contact bank, document gap, defer close if needed
- If open exceptions > 10: Finance Lead reviews whether close should proceed

---

## Phase 2: Controlled Close

**Owner:** Finance Lead
**Timing:** BD -2 to BD -1

### Entry Criteria
- Phase 1 completed with sign-off
- All source data confirmed complete
- **All dagboek entries for the period processed (verwerkt) in Exact Online** — verify via Financieel > Boekingen > Overzicht: "Aantal te verwerken" = 0 for all dagboeken in the period
- Journal entry templates available (from `finance-config-catalog/journals/`)

### Tasks

| # | Task | Owner | Approval required |
|---|---|---|---|
| 2.1 | Review and post recurring journal entries | Finance Lead | Finance Lead |
| 2.2 | Review and post accruals and deferrals | Finance Lead | Finance Lead |
| 2.3 | Reverse prior period accruals (if applicable) | Finance Lead | Finance Lead |
| 2.4 | Post manual journal entries with supporting documentation | Finance Lead | Finance Lead per entry |
| 2.5 | Run fixed asset depreciation (preview, review, post) | Finance Lead | Finance Lead |
| 2.6 | Process fixed asset additions and disposals | Finance Lead | Finance Lead |
| 2.7 | Handle deferred exceptions from pre-close | Finance Lead | Finance Lead |
| 2.8 | Verify all posted journals are correct | Finance Lead | — |

### Exit Criteria
- All recurring entries posted and verified against templates
- All accruals posted with supporting documentation
- Depreciation run completed and reviewed for reasonableness
- All manual journals have attached support and approval
- Finance Lead sign-off on controlled close

### Required Evidence
- Journal listing for the period
- Depreciation calculation output
- Journal approval records (per entry)
- Controlled close sign-off (name + date)

### Exception Path
- If journal amounts deviate > 10% from template: investigate before posting, document reason
- If depreciation output looks unreasonable: review asset register before posting
- If an exception cannot be resolved: assess materiality, defer with Finance Lead approval (immaterial) or CFO approval (material)

---

## Phase 3: Review Close

**Owner:** Finance Lead
**Timing:** BD +1 to BD +2

### Entry Criteria
- Phase 2 completed with sign-off
- All journals and entries posted
- Trial balance available in Exact Online

### Tasks

| # | Task | Owner | Template |
|---|---|---|---|
| 3.1 | Complete balance sheet specifications | Finance Lead | `templates/balance-sheet-specification-template.md` |
| 3.2 | Complete P&L specifications | Finance Lead | `templates/p-and-l-specification-template.md` |
| 3.3 | Complete analytical review | Finance Lead | `templates/analytical-review-template.md` |
| 3.4 | VAT reconciliation | Finance Lead | `templates/reconciliation-template.md` |
| 3.5 | Bank balance reconciliation (Exact vs statement) | Finance Lead | `templates/reconciliation-template.md` |
| 3.6 | Complete supporting evidence index | Finance Lead | `templates/supporting-evidence-index-template.md` |
| 3.7 | Control checklist review | Finance Lead | `templates/control-assessment-template.md` |
| 3.8 | Complete review sign-off and exception log | Finance Lead | `templates/review-signoff-and-exception-log-template.md` |

> **Dossier standard:** All specifications, analytical review, evidence index, and sign-off must meet the requirements in `close/MONTH_END_REPORTING_DOSSIER_STANDARD.md`.

### Exit Criteria
- All balance sheet accounts specified per dossier standard (including fixed asset rollforward, debtor aging, bank reconciliation, VAT reconciliation, accruals)
- All P&L lines specified with month, YTD, prior month, prior year comparisons
- Analytical review completed: all variances exceeding thresholds explained
- Evidence index complete — every specification traces to evidence
- Exception log: all items resolved or accepted with justification
- Finance Lead sign-off on review close

### Required Evidence
- Completed BS specifications with evidence per account area
- Completed P&L specifications with variance explanations
- Completed analytical review
- Completed evidence index
- Completed reconciliations (VAT, bank)
- Control assessment results
- Exception log (final)
- Review close sign-off (name + date)

### Exception Path
- If reconciliation shows unexplained differences: investigate before proceeding; if unresolvable, document and escalate to CFO
- If control failures identified: log as exception in GitHub, assess impact, determine if close can proceed
- If material issues found during review: return to Phase 2 for corrective entries

---

## Phase 4: Final Close

**Owner:** Finance Lead + CFO
**Timing:** BD +3

### Entry Criteria
- Phase 3 completed with sign-off
- Reporting dossier complete per `close/MONTH_END_REPORTING_DOSSIER_STANDARD.md`
- All reviews completed, no unresolved material issues
- Exception log: all close-blocking exceptions resolved or accepted

### Tasks

| # | Task | Owner | Approval required |
|---|---|---|---|
| 4.1 | Finance Lead approval of close | Finance Lead | — |
| 4.2 | CFO approval (if required by policy or materiality) | CFO | — |
| 4.3 | Close period in Exact Online (verify status = Closed) | Finance Lead | Finance Lead + CFO |
| 4.4 | Archive close package | Finance Lead | — |
| 4.5 | Document lessons learned | Finance Lead | — |
| 4.6 | Create improvement issues in GitHub (if applicable) | Finance Lead | — |

### Exit Criteria
- Period status = "Closed" in Exact Online
- Close package archived
- Lessons learned documented
- Improvement issues created (if any)

### Required Evidence — Reporting Dossier
- Close package = reporting dossier, containing:
  1. Completed close checklist (all 4 phases signed off)
  2. Balance sheet specifications (per BS specification template)
  3. P&L specifications (per P&L specification template)
  4. Analytical review (per analytical review template)
  5. Supporting evidence index (complete, all items present)
  6. Review sign-off and exception log (all exceptions resolved or accepted)
  7. Reconciliations (bank, VAT — completed templates)
  8. Control assessment results
  9. Approval evidence (Finance Lead + CFO)
  10. Lessons learned
- Period close confirmation from Exact Online
- Dossier archived in `close/archive/YYYY-MM/`

### Exception Path
- If CFO does not approve: document objections, return to relevant phase
- If period close fails technically: Technical Lead investigates, Finance Lead decides next steps

---

## Approval Boundaries

| Action | Approver |
|---|---|
| Pre-close sign-off | Finance Lead |
| Journal and accrual approval | Finance Lead (per entry) |
| Depreciation run | Finance Lead |
| Exception deferral (immaterial) | Finance Lead |
| Exception deferral (material) | CFO |
| Period close execution | Finance Lead + CFO |
| Close package release | Finance Lead |

**Hard boundary:** No automated process or AI assistant may execute period close without explicit human approval.

## Exception Handling During Close

| Scenario | Action | Approver |
|---|---|---|
| Can be resolved before close deadline | Resolve and document | Finance Lead |
| Cannot be resolved, immaterial | Defer with documentation | Finance Lead |
| Cannot be resolved, material | Escalate | CFO |
| New exception during review phase | Assess materiality, resolve or defer | Finance Lead |

## Reporting Stages

Each period progresses through three reporting stages (Bronze → Silver → Gold) as defined in `close/REPORTING_STAGE_STANDARD.md`. The stages overlay the 4-phase model:

| Close phase | Stage transition |
|---|---|
| Phase 1 complete | → **Bronze** (dossier created, open items captured) |
| Phases 2-3 complete | → **Silver** (specifications populated, reconciliations done) |
| Phase 4 complete | → **Gold** (period locked, dossier archived) |

Bronze allows the close to produce value early — creating the dossier and capturing all known issues — without waiting for all blocking items to be resolved. Open items are tracked in the period's open-items register (`open-items-register-YYYY-MM.md`).

## Related Documents

- Close checklist template: `templates/close-checklist-template.md`
- Reconciliation template: `templates/reconciliation-template.md`
- Control assessment template: `templates/control-assessment-template.md`
- Exception analysis template: `templates/exception-analysis-template.md`
- Open-items register template: `templates/open-items-register-template.md`
- Reporting stage standard: `close/REPORTING_STAGE_STANDARD.md`
- Exception catalog: `finance-config-catalog/exceptions/exception-catalog.md`
- Control matrix: `finance-config-catalog/controls/FINANCE_CONTROL_MATRIX.md`
