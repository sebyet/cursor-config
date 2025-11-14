# Maintain

**Advanced command** for explicit code maintenance, optimization, and updates. For most users, maintenance happens automatically during `@build` and `@fix` workflows.

## When to Use This Command

**Most users don't need this command** - maintenance happens automatically:
- ✅ `@build` → Automatically maintains code quality
- ✅ `@fix` → Automatically prevents similar issues  
- ✅ `@deploy` → Automatically checks security/performance

**Use this command when:**
- You're a technical user who wants explicit control
- You want to refactor large sections proactively
- You want to run comprehensive audits manually
- You're doing code cleanup outside of normal workflows

## What This Command Does

This is an **advanced command for technical users** who want explicit control over maintenance. It automatically:
- Determines what maintenance you need (refactor, optimize, update, security audit)
- Routes to the appropriate specialist command
- Ensures code stays healthy and up-to-date

## How It Works

1. **Ask what you need**
   - "Refactor code" → Routes to `refactor-code.md`
   - "Optimize performance" → Routes to `../devops/check-performance.md`
   - "Update dependencies" → Routes to `../devops/audit-dependencies.md`
   - "Security audit" → Routes to `../devops/check-security.md`
   - "Add error handling" → Routes to `add-error-handling.md`
   - "Everything" → Runs all maintenance checks

2. **Execute the appropriate specialist command**
   - Uses the full workflow from the specialist command
   - Handles all steps automatically

3. **Report maintenance status**
   - Shows what was improved
   - Highlights any issues found
   - Suggests next maintenance tasks

## Usage Examples

- `@maintain` - "Refactor this code"
- `@maintain` - "Check and optimize performance"
- `@maintain` - "Audit dependencies for security"
- `@maintain` - "Run all maintenance checks"

## Specialist Commands Used

- **[Refactor Code](refactor-code.md)** - Refactor code safely
- **[Check Performance](../devops/check-performance.md)** - Optimize performance
- **[Audit Dependencies](../devops/audit-dependencies.md)** - Check dependency security
- **[Check Security](../devops/check-security.md)** - Security audit
- **[Add Error Handling](add-error-handling.md)** - Add error handling

## What to Tell the User

- "What would you like to maintain? (refactor, optimize, update dependencies, security audit, or check everything)"
- Based on their answer, route to the appropriate specialist command
- Execute the full workflow from that command
- Show improvements and any issues found
- "Maintenance complete! Your code is now [improved/optimized/secure]."

## See Also

- **[Build](../build.md)**: Build features (includes automatic maintenance)
- **[Fix](../fix.md)**: Fix issues (includes automatic maintenance)
- **[Deploy](../deploy.md)**: Deploy (includes automatic security/performance checks)
- **[Test](../test.md)**: Test after maintenance changes




