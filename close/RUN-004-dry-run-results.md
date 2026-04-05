# RUN-004: Dry-Run Results — Month-End Close

**Date:** 2026-04-05
**Executed by:** Claude Code (AI-assisted review)
**Method:** Step-by-step walkthrough of runbook and operating model against current repo state and system access
**Status:** Complete — gaps documented

---

## Phase 1: Pre-Close — Dry-Run Results

### Entry Criteria Check

| Criterion | Verifiable? | Finding |
|---|---|---|
| Previous period is closed and archived | Yes — check Exact Online period status | OK. Clear instruction. |
| Close checklist created for the period | Yes — template exists at `templates/close-checklist-template.md` | OK. Template accessible and usable. |
| Task owners assigned | Yes — checklist has Owner column | OK. |
| Target close date confirmed | Yes — checklist has Target Close Date field | OK. |

### Task Walkthrough

| Task | Clear? | Gap? | Finding |
|---|---|---|---|
| 1.1 Verify sales invoices synced | Yes | **Gap 1** | Runbook says "Run sync report from finance-automation" — sync automation is scaffolding only, not operational. Manual count comparison needed until automation is live. |
| 1.2 Review sync exceptions | Yes | No | References GitHub exceptions. Clear. |
| 1.3 Verify purchase invoices processed | Yes | No | Check in Exact Online. Clear. |
| 1.4 Verify bank statements imported | Yes | No | Check in Exact Online. Clear. |
| 1.5 Match unmatched bank transactions | Yes | No | Standard Exact Online procedure. Clear. |
| 1.6 Review open exceptions | Yes | **Gap 2** | References "GitHub exceptions" but no exception issues exist yet. First close will have zero exceptions in GitHub — that's expected but the runbook should note this is normal for the first cycle. |

### Exit Criteria Check
All exit criteria are verifiable. No gaps.

### Evidence Check
- Sync report: **Gap 1** applies — no automated sync report yet. Manual comparison needed.
- Bank import confirmation: obtainable from Exact Online. OK.
- Exception register: GitHub issue list. OK once issues exist.
- Sign-off: name + date format. OK.

---

## Phase 2: Controlled Close — Dry-Run Results

### Entry Criteria Check
All criteria verifiable. Depends on Phase 1 sign-off. OK.

### Task Walkthrough

| Task | Clear? | Gap? | Finding |
|---|---|---|---|
| 2.1 Recurring entries | Yes | **Gap 3** | References `finance-config-catalog/journals/journal-templates.md` for recurring entry templates. File exists but contains generic templates (accruals, depreciation, prepaid). Finance Lead must populate with actual recurring amounts before first close. |
| 2.2 Accruals and deferrals | Yes | No | Standard procedure. Clear. |
| 2.3 Reverse prior period accruals | Yes | No | Clear. Not applicable for first close. |
| 2.4 Manual journals | Yes | No | Clear. Each journal needs support + approval. |
| 2.5 Fixed asset depreciation | Yes | No | Preview → review → post. Clear. |
| 2.6 Fixed asset additions/disposals | Yes | No | With approval. Clear. |
| 2.7 Deferred exceptions | Yes | No | Clear. |
| 2.8 Verify posted journals | Yes | No | Clear. |

### Exit Criteria Check
All verifiable. No gaps.

---

## Phase 3: Review Close — Dry-Run Results

### Entry Criteria Check
All verifiable. OK.

### Task Walkthrough

| Task | Clear? | Gap? | Finding |
|---|---|---|---|
| 3.1 Balance sheet review | Yes | No | Each account reviewed. Clear. |
| 3.2 P&L review vs budget | Yes | **Gap 4** | Says "compare to budget" — is there a budget loaded in Exact Online? If not, only prior period comparison is possible for first close. |
| 3.3 VAT reconciliation | Yes | No | Template at `templates/reconciliation-template.md`. OK. |
| 3.4 Bank reconciliation | Yes | No | Same template. OK. |
| 3.5 Debtor balance review | Yes | No | Clear. |
| 3.6 Creditor balance review | Yes | No | Clear. |
| 3.7 Variance analysis | Yes | No | Material items explained. Clear. |
| 3.8 Control checklist review | Yes | No | Template at `templates/control-assessment-template.md`. OK. |

---

## Phase 4: Final Close — Dry-Run Results

### Entry Criteria Check
All verifiable. OK.

### Task Walkthrough

| Task | Clear? | Gap? | Finding |
|---|---|---|---|
| 4.1 Finance Lead approval | Yes | No | Clear. |
| 4.2 CFO approval | Yes | No | "If required" — clear. |
| 4.3 Close period in Exact | Yes | No | Verify status = "Closed". Clear. |
| 4.4 Archive close package | Yes | **Gap 5** | Says "archive close package" but does not specify where or how. Is it a folder in Exact? A PDF export? A GitHub commit? |
| 4.5 Lessons learned | Yes | No | Clear. |
| 4.6 Improvement issues | Yes | No | Create in GitHub. Clear. |

---

## Gap Summary

| # | Gap | Phase | Severity | Resolution |
|---|---|---|---|---|
| 1 | Sync report not automated — finance-automation is scaffolding | Pre-close (1.1) | Medium | Add manual workaround note to runbook: "Until automation is live, manually compare Zoho Books invoice count to Exact Online posted sales invoice count." |
| 2 | No exception issues in GitHub for first close | Pre-close (1.6) | Low | Add note: "For the first governed close, an empty exception register is expected." |
| 3 | Recurring journal templates not populated with actual amounts | Controlled close (2.1) | High | Finance Lead must populate `finance-config-catalog/journals/journal-templates.md` with actual recurring entry amounts before first close. |
| 4 | Budget availability not confirmed | Review close (3.2) | Medium | Add note: "If no budget is loaded, compare to prior period only." |
| 5 | Close package archive location not specified | Final close (4.4) | Medium | Specify archive location (e.g., "save completed close checklist and evidence as a commit in finance-runbooks/close/archive/YYYY-MM/") |

---

## Template Usability Check

| Template | Exists | Usable as-is | Notes |
|---|---|---|---|
| Close checklist | Yes | Yes | All phases, tasks, sign-off fields present |
| Reconciliation | Yes | Yes | Source A/B, reconciling items, sign-off |
| Control assessment | Yes | Yes | All fields present |
| Exception analysis | Yes | Yes | Full investigation workflow |

---

## Recommendations

1. **Apply Gap 1 fix now** — add manual workaround to runbook (safe, immediate)
2. **Apply Gap 2 fix now** — add first-close note (safe, immediate)
3. **File issue for Gap 3** — journal templates need Finance Lead data input
4. **Apply Gap 4 fix now** — add budget note (safe, immediate)
5. **Apply Gap 5 fix now** — specify archive method (safe, immediate)
