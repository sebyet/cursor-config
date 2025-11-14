# Security Audit

Perform code-level security audit to identify vulnerabilities, insecure patterns, and security risks.

## What This Command Does

Audits security by:
- Scanning for common vulnerabilities
- Checking OWASP Top 10 issues
- Analyzing dependency security
- Reviewing authentication/authorization
- Checking input validation
- Identifying insecure patterns
- Generating security report

## How It Works

1. **Understand Security Context**
   - Ask about security concerns
   - Identify sensitive data
   - Understand authentication flow
   - Get context on user permissions

2. **Perform Security Scan**
   - Scan code for vulnerabilities
   - Check dependency security
   - Analyze authentication code
   - Review authorization logic
   - Check input validation
   - Identify insecure patterns
   - Check for exposed secrets

3. **Analyze Security Issues**
   - Categorize vulnerabilities
   - Assess risk levels
   - Identify attack vectors
   - Check compliance requirements
   - Review security best practices

4. **Generate Security Report**
   - Create security audit report
   - List vulnerabilities by severity
   - Provide remediation steps
   - Recommend security improvements
   - Include compliance checklist

5. **Implement Security Fixes**
   - Fix critical vulnerabilities
   - Add input validation
   - Secure authentication
   - Implement authorization checks
   - Remove exposed secrets
   - Apply security best practices

## What to Tell the User

- "What security concerns do you have?"
- "What sensitive data does your app handle?"
- Scan and analyze security
- "Security audit complete! Vulnerabilities found: [count]. Critical: [list]. Recommendations: [list]"
- Implement security fixes
- "Security fixes applied! Remaining issues: [list]"

## See Also

- **[Check Security](../devops/check-security.md)**: Infrastructure security
- **[Security Audit](../devops/security-audit.md)**: Comprehensive security audit
- **[Security Guidelines](mdc:.cursor/rules/security-guidelines.mdc)**: Security best practices
- **[Check Vulnerabilities](../devops/check-vulnerabilities.md)**: Dependency vulnerabilities

