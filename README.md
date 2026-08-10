# Finance Runbooks

**Owner:** Finance Lead

Operational procedures and templates for finance operations. Follow a runbook step by step. If the runbook does not cover your situation, escalate.

## Runbooks

| Runbook | Folder | Primary user |
|---|---|---|
| Month-End Close | [close/](close/) | Finance Lead |
| Sales Invoice Sync Exceptions | [exceptions/](exceptions/) | Technical Lead |
| Bank Exceptions | [exceptions/](exceptions/) | Finance Lead |
| Purchase Exceptions | [exceptions/](exceptions/) | Finance Lead |
| Journal Handling | [operations/](operations/) | Finance Lead |
| Fixed Asset Controls | [operations/](operations/) | Finance Lead |
| Release | [release/](release/) | Technical Lead |
| Rollback | [rollback/](rollback/) | Technical Lead |
| Incident Response | [incident/](incident/) | Technical Lead |

## Key Documents

Month-end close documentation (operating model, runbook, reporting-stage
standard, dossier standard, and the archived closes for 2026-01/2026-02)
moved to the **Maandafsluiting** module in
[`Powercrumbs/forecast`](https://github.com/Powercrumbs/forecast/tree/main/docs/maandafsluiting),
which now also runs the checklist/exception tracking these documents
describe.

## Operational Templates

| Template | Purpose | Location |
|---|---|---|
| Close checklist | Period close task tracking | [Powercrumbs/forecast — docs/maandafsluiting/close-checklist-template.md](https://github.com/Powercrumbs/forecast/blob/main/docs/maandafsluiting/close-checklist-template.md) |
| Control assessment | Control effectiveness review | [templates/control-assessment-template.md](templates/control-assessment-template.md) |
| Exception analysis | Exception investigation and resolution | [templates/exception-analysis-template.md](templates/exception-analysis-template.md) |
| Reconciliation | Balance reconciliation (bank, VAT, debtor, creditor) | [templates/reconciliation-template.md](templates/reconciliation-template.md) |

## Usage

1. Identify the situation
2. Open the relevant runbook
3. Follow the steps in order
4. Use the appropriate template from `templates/`
5. Document the outcome
6. If the runbook does not cover your situation, escalate

## Maintenance

- Updated after each use if gaps are identified
- Reviewed after incidents
- Quarterly review cycle
- Changes require Finance Lead approval via PR
