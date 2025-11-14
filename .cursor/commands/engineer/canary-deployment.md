# Canary Deployment

Set up canary deployments to gradually roll out changes to a subset of users.

## What This Command Does

Sets up canary deployments by:
- Configuring canary percentage
- Setting up traffic splitting
- Monitoring canary performance
- Automating promotion/rollback
- Documenting canary strategy

## How It Works

1. **Understand Canary Needs**
   - Ask about deployment strategy
   - Identify canary percentage
   - Understand monitoring requirements
   - Determine promotion criteria

2. **Design Canary Setup**
   - Configure traffic splitting
   - Set up monitoring
   - Define promotion criteria
   - Plan rollback triggers

3. **Generate Configuration**
   - Create canary config
   - Set up monitoring
   - Configure automation
   - Document setup steps

## What to Tell the User

- "What percentage of traffic should go to canary? (e.g., 5%, 10%)"
- "What metrics should we monitor for canary?"
- Generate canary deployment configuration
- "Canary deployment setup complete! Percentage: [%]. Monitoring: [configured]. Automation: [setup]"

## See Also

- **[Publish Production](publish-production.md)**: Deploy to production
- **[Blue Green Deployment](blue-green-deployment.md)**: Blue-green deployment
- **[Setup Feature Flags](../growth/setup-feature-flag.md)**: Feature flags

