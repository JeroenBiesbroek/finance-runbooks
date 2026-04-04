# RUN-001: Apply labels to finance-runbooks

**Repo:** finance-runbooks
**Owner type:** Technical Lead
**Labels:** `type:tech-debt`, `area:configuration`, `system:github`, `priority:critical`
**Milestone:** foundation-baseline

## Objective

Create the full label set so issues can be properly categorized.

## Scope

Run the label creation script against this repository. Same 40 labels as all finance repos.

## Dependencies

None.

## Acceptance Criteria

- [ ] All 40 labels created

## Definition of Done

`gh label list -R {owner}/finance-runbooks` returns 40 labels.

## Execution

Same script as GOV-001, replace `REPO="{owner}/finance-runbooks"`.
