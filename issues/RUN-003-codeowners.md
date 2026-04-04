# RUN-003: Create CODEOWNERS file

**Repo:** finance-runbooks
**Owner type:** Technical Lead
**Labels:** `type:tech-debt`, `area:configuration`, `system:github`, `priority:critical`
**Milestone:** foundation-baseline

## Objective

Auto-assign Finance Lead as reviewer for all PRs in this repo.

## Dependencies

RUN-002 (branch protection must be enabled).

## Acceptance Criteria

- [ ] `CODEOWNERS` file exists at repo root
- [ ] PRs automatically request review from Finance Lead

## Definition of Done

Open a test PR. Verify Finance Lead is auto-requested. Close test PR.

## File Content

```
# Finance runbooks — Finance Lead owns procedures
* @{finance-lead-username}

# Close procedures
/close/ @{finance-lead-username}

# Templates
/templates/ @{finance-lead-username}
```
