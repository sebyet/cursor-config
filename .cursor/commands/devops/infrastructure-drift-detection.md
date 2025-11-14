# Infrastructure Drift Detection

Detect and manage infrastructure drift to maintain Infrastructure as Code consistency.

## What This Command Does

Detects infrastructure drift by:
- Detecting infrastructure drift
- Comparing actual vs. desired state
- Generating drift reports
- Remediating drift issues
- Setting up drift monitoring

## How It Works

1. **Understand Drift Detection Needs**
   - Ask about infrastructure to monitor
   - Identify IaC tool (Terraform, CloudFormation, etc.)
   - Understand drift detection frequency
   - Determine remediation strategy
   - Get context on infrastructure state

2. **Set Up Drift Detection**
   - Configure drift detection tools
   - Set up state comparison
   - Configure drift detection schedules
   - Set up drift alerts
   - Document drift detection setup

3. **Detect and Analyze Drift**
   - Run drift detection scans
   - Compare actual vs. desired state
   - Identify drift causes
   - Categorize drift by severity
   - Generate drift reports

4. **Remediate Drift**
   - Plan drift remediation
   - Apply infrastructure changes
   - Verify drift resolution
   - Document remediation steps
   - Update infrastructure state

## What to Tell the User

- "What IaC tool are you using? (Terraform, CloudFormation, etc.)"
- "What infrastructure should be monitored for drift?"
- "What's your drift detection frequency?"
- Set up drift detection and generate reports
- "Drift detection setup complete! Monitoring: [configured]. Drift found: [count]. Remediation: [recommended]"

## See Also

- **[Setup Terraform](setup-terraform.md)**: Terraform setup for drift detection
- **[Manage Infrastructure](manage-infrastructure.md)**: Infrastructure management
- **[Setup Monitoring](setup-monitoring.md)**: Monitor drift detection

