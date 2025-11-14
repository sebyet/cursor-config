# Rollback Deployment

Rollback to a previous deployment version when issues are detected.

## What This Command Does

Rolls back deployments by:
- Identifying previous stable version
- Reverting to previous deployment
- Verifying rollback success
- Documenting rollback reason
- Notifying stakeholders

## How It Works

1. **Understand Rollback Needs**
   - Ask about current issues
   - Identify target version
   - Understand deployment history
   - Determine rollback scope

2. **Execute Rollback**
   - Revert to previous version
   - Verify deployment
   - Check system health
   - Confirm rollback success

3. **Document and Notify**
   - Document rollback reason
   - Update deployment history
   - Notify team
   - Plan follow-up actions

## What to Tell the User

- "What version should we rollback to?"
- "What issues are you experiencing?"
- Execute rollback and verify
- "Rollback complete! Version: [previous]. Status: [verified]. Next steps: [list]"

## See Also

- **[Publish Production](publish-production.md)**: Deploy to production
- **[Canary Deployment](canary-deployment.md)**: Canary deployment strategy
- **[Analyze Incident](../devops/analyze-incident.md)**: Analyze deployment incidents

