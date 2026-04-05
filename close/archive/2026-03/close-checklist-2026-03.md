# Month-End Close Checklist

## Period: 2026-03
## Close Owner: Finance Lead (Jeroen Biesbroek)
## Target Close Date: 2026-04-07
## Type: First governed close (retrospective)

> This is the first close executed under the governed close model.
> March 2026 is already past — this applies governance to an already-completed accounting period.
> Gaps and lessons learned are expected and valuable.

---

## Phase 1: Pre-Close

| # | Task | Owner | Done | Notes |
|---|---|---|---|---|
| 1.1 | Verify all sales invoices synced from Zoho Books | Finance Lead | [ ] | Manual comparison: Zoho Books invoice count vs Exact Online posted count for March 2026 |
| 1.2 | Review sales invoice sync exceptions | Finance Lead | [ ] | First governed close — empty exception register expected |
| 1.3 | Confirm all purchase invoices processed | Finance Lead | [ ] | Check in Exact Online: Inkoop > Overzicht, filter March 2026 |
| 1.4 | Confirm all bank statements imported and matched | Finance Lead | [ ] | Verify bank import through 31-03-2026 |
| 1.5 | Review bank matching exceptions | Finance Lead | [ ] | Check unmatched items in Exact Online |
| 1.6 | Review open exception items | Finance Lead | [ ] | Check GitHub issues for open exceptions |

**Pre-close sign-off:** __________________ Date: __________

## Phase 2: Controlled Close

| # | Task | Owner | Done | Notes |
|---|---|---|---|---|
| 2.1 | Post recurring journal entries | Finance Lead | [ ] | Use journal templates from finance-config-catalog/journals/journal-templates.md |
| 2.2 | Post salary accruals (vakantiegeld, 13e maand) | Finance Lead | [ ] | Template 2 — confirm amounts first |
| 2.3 | Post cost accruals (accountant, energy, etc.) | Finance Lead | [ ] | Template 3 — fill in estimated amounts first |
| 2.4 | Reverse prior period cost accruals | Finance Lead | [ ] | N/A for first close |
| 2.5 | Run fixed asset depreciation (preview → review → post) | Finance Lead | [ ] | Template 1 — use Exact Online depreciation run |
| 2.6 | Process fixed asset additions/disposals | Finance Lead | [ ] | With Finance Lead approval per item |
| 2.7 | Post any manual journal entries with support | Finance Lead | [ ] | Each entry needs documented support |
| 2.8 | Verify all journals posted correctly | Finance Lead | [ ] | Check journal listing for March 2026 |

**Controlled close sign-off:** __________________ Date: __________

## Phase 3: Review Close

| # | Task | Owner | Done | Notes |
|---|---|---|---|---|
| 3.1 | Balance sheet review — each account | Finance Lead | [ ] | |
| 3.2 | P&L review — compare to prior period | Finance Lead | [ ] | No budget loaded; compare to February 2026 |
| 3.3 | VAT reconciliation | Finance Lead | [ ] | Use templates/reconciliation-template.md |
| 3.4 | Bank balance reconciliation | Finance Lead | [ ] | Exact GL balance vs bank statement at 31-03-2026 |
| 3.5 | Debtor balance review | Finance Lead | [ ] | |
| 3.6 | Creditor balance review | Finance Lead | [ ] | |
| 3.7 | Variance analysis — explain material items | Finance Lead | [ ] | |
| 3.8 | Control checklist review | Finance Lead | [ ] | Use templates/control-assessment-template.md |

**Review close sign-off:** __________________ Date: __________

## Phase 4: Final Close

| # | Task | Owner | Done | Notes |
|---|---|---|---|---|
| 4.1 | Finance Lead approval | Finance Lead | [ ] | |
| 4.2 | CFO approval (if required) | CFO | [ ] | |
| 4.3 | Close period in Exact Online — verify status = "Closed" | Finance Lead | [ ] | Financieel > Periode-datumcontrole |
| 4.4 | Archive close package in close/archive/2026-03/ | Finance Lead | [ ] | Commit completed checklist + evidence via PR |
| 4.5 | Document lessons learned | Finance Lead | [ ] | |
| 4.6 | Create improvement issues in GitHub | Finance Lead | [ ] | |

**Final close sign-off:** __________________ Date: __________

---

## Lessons Learned
<!-- Document after close execution -->

## Improvement Items
<!-- List improvement issues created -->
