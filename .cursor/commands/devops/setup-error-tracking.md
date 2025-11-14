# Setup Error Tracking

Configure error tracking and exception monitoring (Sentry, Rollbar, Bugsnag, etc.).

## What This Command Does

Sets up error tracking by:
- Configuring error tracking service (Sentry, Rollbar, Bugsnag)
- Setting up source maps for JavaScript
- Creating error grouping and filtering rules
- Establishing alerting for critical errors
- Configuring release tracking

## How It Works

1. **Understand Error Tracking Needs**
   - Ask about error tracking service
   - Identify environments to track
   - Understand application stack
   - Determine alerting requirements

2. **Design Error Tracking Setup**
   - Choose error tracking tool
   - Configure source maps
   - Set up error grouping
   - Define alert thresholds

3. **Generate Configuration**
   - Create error tracking config
   - Set up SDK integration
   - Configure alerts
   - Document setup steps

## What to Tell the User

- "What error tracking service are you using? (Sentry, Rollbar, Bugsnag, etc.)"
- "What environments should we track? (development, staging, production)"
- Generate error tracking configuration
- "Error tracking setup complete! Service: [tool]. Alerts: [list]. Source maps: [configured]"

## See Also

- **[Setup Logging](setup-logging.md)**: Set up structured logging
- **[Setup APM](setup-apm.md)**: Set up Application Performance Monitoring
- **[Check Security](check-security.md)**: Security checks

