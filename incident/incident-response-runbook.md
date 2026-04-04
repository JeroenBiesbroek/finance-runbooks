# Incident Response Runbook

## Severity levels

| Level | Definition | Response time |
|---|---|---|
| Critical | Financial data at risk | < 30 min |
| High | Operations disrupted | < 2 hours |
| Medium | Degraded but functional | < 8 hours |
| Low | Minor, no operational impact | < 24 hours |

## Procedure

### 1. Detection and triage
1. Identify incident (alert, report, monitoring)
2. Assess severity
3. Assign incident owner
4. Create incident report in GitHub

### 2. Containment
1. Stop affected automation if applicable
2. Isolate affected data if applicable
3. Switch to manual processing if needed
4. Notify Finance Lead; if Critical: notify CFO

### 3. Investigation
1. Gather evidence (logs, reports, audit trail, recent changes)
2. Identify root cause
3. Determine scope: records, period, financial impact

### 4. Resolution
1. Develop fix or corrective action
2. Data corrections: identify records, prepare entries (Finance Lead approval)
3. System fixes: follow emergency change process
4. Restore normal operations

### 5. Verification
1. Confirm resolved
2. Verify data integrity restored
3. Finance Lead confirms normal operations

### 6. Post-incident
1. Complete incident report
2. Document timeline, root cause, actions, financial impact
3. Schedule review within 1 week
4. Identify preventive measures
5. Create improvement issues
6. Update runbooks if gaps found

## Escalation

| Condition | Escalate to |
|---|---|
| Critical severity | Finance Lead + CFO |
| Financial data affected | Finance Lead |
| Outage > 2 hours | Technical Lead + Finance Lead |
| Suspected unauthorized access | Finance Lead + CFO |
