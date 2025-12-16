# Go Live → "Make it available"

Intelligently checks quality (code cleanup, security, accessibility, code review), verifies everything is ready, then guides you through publishing your website to production and making it live. Only checks what's needed and only publishes if ready!

1. **Run quality checks (if needed)**
   - Check if there are recent changes that need review
   - **If code changes made:** Remove AI-generated slop from code (extra comments, unnecessary checks)
   - **If security concerns:** Check for security problems (authentication, input validation, API security) and fix them
   - **If UI changes made:** Check accessibility (keyboard navigation, screen readers, color contrast) and fix issues
   - **If code changes made:** Review code quality (structure, best practices, potential bugs)
   - **Run tests:** Make sure all tests pass
   - **Check performance:** Verify site is fast (load times, bundle sizes, image optimization)
   - **Audit dependencies:** Check for security vulnerabilities in packages
   - Only run checks that are needed - skip if already verified recently
   - Tell the user what you're checking in plain English

2. **Check if ready to publish to production**
   - Check if project builds successfully
   - Check if code is saved to Git
   - Check if code is uploaded to GitHub
   - Check if Vercel CLI is installed and user is logged in
   - Check if production environment variables are set (if needed)
   - Tell the user what you found

3. **Fix issues if needed**
   - **If AI slop found:** Remove AI-generated slop from code first (clean up automatically)
   - **If security issues found:** Fix security problems first (explain in simple terms what was wrong)
   - **If accessibility issues found:** Fix accessibility problems first (explain why it matters)
   - **If code quality issues found:** Fix code quality problems first (clean up automatically)
   - **If tests fail:** Fix test failures first (explain what broke in simple terms)
   - **If performance issues found:** Fix performance problems (optimize images, reduce bundle size)
   - **If dependency vulnerabilities found:** Fix security issues (update vulnerable packages)
   - **If build fails:** Fix build issues (explain errors in simple terms)
   - **If code not saved:** Save changes automatically
   - **If not on GitHub:** Upload to GitHub automatically
   - **If Vercel CLI not installed/logged in:** Guide them step-by-step through setup (explain what Vercel is and why we need it)

4. **Merge to main branch** (combine your work with the main version)
   - Check what branch we're currently on
   - **Explain simply:** "I'm combining your work with the main version - like merging your draft document with the final version"
   - **If not on main:** Merge current branch into main
     - Ensure all changes are committed first
     - Switch to main branch: `git checkout main`
     - Merge current branch into main: `git merge <branch-name>`
     - **If merge conflicts:** Help resolve conflicts, then complete merge (explain: "Some changes need to be combined - I'll help you decide which version to keep")
   - **If already on main:** Verify main branch is up to date
   - Push merged main branch to GitHub: `git push origin main` (explain: "I'm saving everything online")
   - Tell the user the branch has been merged to main in simple terms: "All your work is now combined and saved!"

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
  - **Use analogies:** "I'm checking everything before we publish - like proofreading a blog post before hitting 'publish'"
- List what you're checking in simple terms (e.g., "Making sure everything works, checking security, making sure it's fast...")
- Only run checks that are needed - skip if already verified recently
- If you find problems, explain them simply and fix them
  - **Use analogies:** "Found a small issue - like finding a typo. I'll fix it quickly!"
- Show progress of each check in plain English
- List what you found (e.g., "All checks passed! Everything is saved, tested, and ready to go live!")
- **Merge current branch to main** - Explain: "I'm combining your work with the main version - like merging your draft with the final document"
- Push merged main branch to GitHub - Explain: "I'm saving everything online so it's backed up"
- Deploy to production using Vercel CLI - Explain: "I'm publishing your website now - like hitting 'publish' on a blog post. This will make it live on the internet!"
- Only publish to production if everything is ready - fix issues first if needed
- Guide them step-by-step through Vercel CLI setup (if first time - explain: "I need you to sign in to Vercel - this is the service that makes your website live. I'll open your browser for you.")
- Tell them their production website address when it's live (from Vercel CLI output) - Celebrate: "Your website is now live! Here's the address: [URL]"
- If something goes wrong, help them fix it - Explain: "Something went wrong, but don't worry - I'll fix it. Here's what happened: [simple explanation]"
- Celebrate when all checks pass and the website goes live to production! - "🎉 Congratulations! Your website is now live on the internet!"

## See Also

- **[Run Tests](run-tests.md)**: Run tests explicitly when needed
- **[Fix Issues](fix-issues.md)**: Fix any issues before publishing
- **[Preview App](preview-app.md)**: Create preview before going live