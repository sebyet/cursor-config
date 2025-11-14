# Audit Dependencies

Checks your project's dependencies (packages you use) for security problems, outdated versions, and unused packages. Keeps your project safe and up-to-date.

1. **Check dependencies**
   - Check for security vulnerabilities
   - Check for outdated packages
   - Check for unused dependencies
   - Check for duplicate dependencies
   - Check package licenses
   - Tell the user what you found

2. **Fix security issues**
   - Fix critical security vulnerabilities immediately
   - Fix high-severity vulnerabilities within 1 week
   - Update vulnerable packages
   - Test updates to make sure nothing broke
   - Don't proceed until critical issues are fixed

3. **Update dependencies (if needed)**
   - Update outdated packages safely
   - Update one major version at a time
   - Test updates to make sure nothing broke
   - Fix any breaking changes
   - Update lock files

4. **Clean up unused dependencies**
   - Remove unused packages
   - Consolidate duplicate dependencies
   - Clean up package.json

5. **Verify everything works**
   - Run tests to make sure updates didn't break anything
   - Build project to check for errors
   - Fix any problems if tests or build fail
   - Don't proceed until everything works

6. **Document dependency audit**
   - Create `doc/` folder if it doesn't exist
   - Create file: `doc/dependency-audit-YYYY-MM-DD.md`
   - Document: vulnerabilities found, packages updated, security status

## What to Tell the User

- Explain you're checking dependencies for security and updates
- List what you're checking (security, outdated packages, unused packages)
- Show security vulnerabilities found
- Fix critical security issues first
- Update packages safely and test them
- Remove unused dependencies
- Run tests to verify everything still works
- Tell them when dependency audit is complete
- Document all checks and updates

## See Also

### Workflow
- **[Maintain](../engineer/maintain.md)**: Advanced maintenance command
- **[Check Security](check-security.md)**: Security checks
- **[Check Vulnerabilities](check-vulnerabilities.md)**: Check for vulnerabilities
- **[Test](../test.md)**: Test after dependency updates
- **[Deploy](../deploy.md)**: Deploy after updates

### Security
- **[Security Audit](security-audit.md)**: Comprehensive security audit

### Guidelines
- **[Dependency Management](.cursor/rules/dependency-management.mdc)**: Dependency management best practices
- **[Security Guidelines](.cursor/rules/security-guidelines.mdc)**: Security best practices

