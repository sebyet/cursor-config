# Publish to Production (Go Live)

Intelligently checks quality (code cleanup, security, accessibility, code review), verifies everything is ready, then guides you through publishing your website to production and making it live. Only checks what's needed and only publishes if ready!

1. **Run quality checks (if needed)**
   - Check if there are recent changes that need review
   - **If code changes made:** Use `deslop.md` approach - remove AI-generated slop from code
   - **If security concerns:** Use `check-security.md` approach - check for security problems and fix them
   - **If UI changes made:** Use `accessibility-audit.md` approach - check accessibility and fix issues
   - **If code changes made:** Use `code-review.md` approach - review code quality
   - **Run tests:** Use `run-tests.md` approach - make sure all tests pass
   - **Check performance:** Use `check-performance.md` approach - verify site is fast
   - **Audit dependencies:** Use `audit-dependencies.md` approach - check for security vulnerabilities
   - Only run checks that are needed - skip if already verified recently
   - Tell the user what you're checking

2. **Check if ready to publish to production**
   - Check if project builds successfully
   - Check if code is saved to Git
   - Check if code is uploaded to GitHub
   - Check if Vercel CLI is installed and user is logged in
   - Check if production environment variables are set (if needed)
   - Tell the user what you found

3. **Fix issues if needed**
   - **If AI slop found:** Use `deslop.md` approach - remove AI-generated slop from code first
   - **If security issues found:** Fix security problems first
   - **If accessibility issues found:** Fix accessibility problems first
   - **If code quality issues found:** Fix code quality problems first
   - **If tests fail:** Use `run-tests.md` approach - fix test failures first
   - **If performance issues found:** Use `check-performance.md` approach - fix performance problems
   - **If dependency vulnerabilities found:** Use `audit-dependencies.md` approach - fix security issues
   - **If build fails:** Use `build-project.md` approach - fix build issues
   - **If code not saved:** Save changes to Git first
   - **If not on GitHub:** Upload to GitHub first
   - **If Vercel CLI not installed/logged in:** Guide them through Vercel CLI setup (install, login, link project)

4. **Merge to main branch**
   - Check what branch we're currently on
   - **If not on main:** Merge current branch into main
     - Ensure all changes are committed first
     - Switch to main branch: `git checkout main`
     - Merge current branch into main: `git merge <branch-name>`
     - **If merge conflicts:** Help resolve conflicts, then complete merge
   - **If already on main:** Verify main branch is up to date
   - Push merged main branch to GitHub: `git push origin main`
   - Tell the user the branch has been merged to main

5. **Publish to production (make it live)**
   - **Ensure on main branch** - Verify we're on main/master before deploying
   - **Deploy using Vercel CLI** - Use `vercel --prod` command to deploy to production directly
   - **If first time:** Guide them through Vercel CLI setup (login, link project)
   - **If already linked:** Deploy to production using `vercel --prod --yes` (non-interactive)
   - Capture and display the production URL from Vercel CLI output
   - Make sure their production site goes live on the internet

6. **Verify it's live**
   - Test that the website works
   - Check for any problems
   - Tell them their website is ready!

7. **Document production publication**
   - Create `doc/` folder if it doesn't exist
   - Create file: `doc/go-live-production-{feature-name}-YYYY-MM-DD.md`
   - Document: quality checks performed, issues found and fixed, production publication details, date, version, URL, what was published
   - Extract feature name from context (lowercase with hyphens)
   - Include deslop, security, accessibility, code review, build, and production publication status

## What to Tell the User

- Explain you're running quality checks and verifying everything is ready to publish to production
- List what you're checking (e.g., "Checking code cleanup, security, accessibility, building...")
- Only run checks that are needed - skip if already verified recently
- If you find problems, explain them simply and fix them
- Show progress of each check
- List what you found (e.g., "All checks passed! Code is saved, on GitHub, builds successfully - ready to go live to production!")
- **Merge current branch to main** - Check current branch, merge to main if needed, handle conflicts if any
- Push merged main branch to GitHub
- Deploy to production using Vercel CLI (use `vercel --prod --yes` for non-interactive deployment)
- Only publish to production if everything is ready - fix issues first if needed
- Guide them step-by-step through Vercel CLI setup (if first time - login, link project)
- Tell them their production website address when it's live (from Vercel CLI output)
- If something goes wrong, help them fix it
- Celebrate when all checks pass and the website goes live to production!

## See Also

### Workflow
- **[Build](../build.md)**: Build features before deploying
- **[Test](../test.md)**: Test before deploying
- **[Fix](../fix.md)**: Fix issues before deploying
- **[Deploy](../deploy.md)**: Main deploy command

### Quality Checks
- **[Run Tests](run-tests.md)**: Run tests before going live
- **[Check Security](../devops/check-security.md)**: Security checks
- **[Accessibility Audit](../design/accessibility-audit.md)**: Accessibility checks
- **[Code Review](code-review.md)**: Code quality review
- **[Check Performance](../devops/check-performance.md)**: Performance checks
- **[Audit Dependencies](../devops/audit-dependencies.md)**: Dependency security checks