# Rollback Runbook

## When to use
- Critical errors after release
- Data integrity issues from release
- Financial reporting discrepancies traced to release
- Finance Lead requests rollback

## Procedure

### 1. Decision
1. Identify the issue
2. Assess severity and financial impact
3. Determine rollback vs. hotfix
4. Finance Lead authorizes rollback

### 2. Communication
1. Notify Finance Lead + Technical Lead
2. Notify affected stakeholders

### 3. Execution

**finance-automation:**
1. Identify last known good version tag
2. Revert commits or deploy previous tag
3. Create PR for rollback, emergency review and merge
4. Verify rollback deployed

**Data corrections (if needed):**
1. Identify affected records
2. Prepare correcting entries (Finance Lead approval required)
3. Post corrections
4. Verify data integrity

### 4. Verification
1. Confirm rollback effective
2. Verify financial operations normal
3. Finance Lead confirms

### 5. Post-rollback
1. Create incident report in GitHub
2. Document root cause and actions
3. Schedule post-incident review (within 1 week)
4. Plan corrective release

## Escalation
- Rollback fails → Finance Lead immediately
- Material financial impact → CFO
