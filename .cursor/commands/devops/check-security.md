# Check Security

Checks your code for security problems before going live. Finds vulnerabilities, validates inputs, checks authentication, and makes sure your app is safe for users.

1. **Check for security issues**
   - Check for common vulnerabilities (SQL injection, XSS, CSRF)
   - Check authentication and authorization
   - Check input validation
   - Check sensitive data handling
   - Check API security
   - Check environment variables and secrets
   - Tell the user what you found

2. **Fix security problems**
   - Fix vulnerabilities found
   - Add missing validation
   - Secure authentication
   - Protect sensitive data
   - Fix API security issues
   - Secure environment variables

3. **Verify security**
   - Run security checks again
   - Make sure all issues are fixed
   - Confirm app is secure

4. **Document security checks**
   - Create `doc/` folder if it doesn't exist
   - Create file: `doc/security-check-YYYY-MM-DD.md`
   - Document: issues found, fixes applied, security status

## What to Tell the User

- Explain you're checking for security problems
- List what you're checking (e.g., "Checking authentication, input validation, and API security...")
- If you find problems, explain them clearly and fix them
- Show progress of each check
- Tell them when security checks pass
- Document all checks and fixes for the project history

## See Also

### Workflow
- **[Maintain](../engineer/maintain.md)**: Advanced maintenance command
- **[Deploy](../deploy.md)**: Deploy after security checks
- **[Fix](../fix.md)**: Fix security issues

### Security
- **[Security Audit](security-audit.md)**: Comprehensive security audit
- **[Check Vulnerabilities](check-vulnerabilities.md)**: Check for vulnerabilities
- **[Review Permissions](review-permissions.md)**: Review access controls
- **[Compliance Check](compliance-check.md)**: Check compliance