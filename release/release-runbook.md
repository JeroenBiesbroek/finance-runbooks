# Release Runbook

**Owner:** Technical Lead

## When to use
When deploying approved changes to the Finance domain production environment.

## Pre-release
1. Verify all PRs merged (to `develop` for automation, or ready for merge)
2. Verify all test evidence attached
3. Verify control impact assessments completed
4. Verify documentation updated
5. Verify release notes drafted
6. Confirm no open blockers

## Approval
1. Present release to Finance Lead
2. Obtain Finance Lead + Technical Lead sign-off
3. Obtain CFO sign-off (if major release)
4. Document approvals in release issue

## Execution

**finance-automation:**
1. Create release PR from `develop` to `main`
2. Final review
3. Merge to `main`
4. Tag: `git tag -a vX.Y.Z -m "Release vX.Y.Z"` → push tag

**Other repositories:**
1. Merge approved PRs to `main`
2. Tag if significant

## Post-release
1. Verify deployment successful
2. Run smoke tests if applicable
3. Monitor for 24 hours
4. Publish release notes
5. Close related issues
6. Notify stakeholders

## Rollback triggers
- Critical production errors
- Data integrity issues
- Financial reporting discrepancies
- Finance Lead requests rollback

If triggered → follow [Rollback Runbook](../rollback/rollback-runbook.md)
