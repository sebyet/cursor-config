# Go Live

Intelligently checks quality (code cleanup, security, accessibility, code review), verifies everything is ready, then guides you through publishing your React Native app to the App Store and Google Play Store. Only checks what's needed and only publishes if ready!

1. **Run quality checks (if needed)**
   - Check if there are recent changes that need review
   - **If code changes made:** Remove AI-generated slop from code (extra comments, unnecessary checks)
   - **If security concerns:** Check for security problems (authentication, input validation, API security) and fix them
   - **If UI changes made:** Check accessibility (keyboard navigation, screen readers, color contrast) and fix issues
   - **If code changes made:** Review code quality (structure, best practices, potential bugs)
   - **Run tests:** Make sure all tests pass
   - **Check performance:** Verify app is fast (bundle sizes, image optimization, list virtualization)
   - **Audit dependencies:** Check for security vulnerabilities in packages
   - Only run checks that are needed - skip if already verified recently
   - Tell the user what you're checking in plain English

2. **Check if ready to publish to production**
   - Check if project builds successfully
   - Check if code is saved to Git
   - Check if code is uploaded to GitHub
   - Check if version numbers are bumped (package.json, app.json, Info.plist, build.gradle)
   - Check if App Store Connect / Google Play Console accounts are configured
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
   - **If version not bumped:** Bump version numbers automatically

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

5. **Build for production**
   - **For Expo projects:** Use EAS Build for production builds
     - `eas build --profile production --platform ios`
     - `eas build --profile production --platform android`
   - **For React Native CLI:** Create production builds
     - iOS: Archive and create .ipa file for App Store
     - Android: Create AAB file for Google Play Store
   - Verify builds are successful
   - Check build artifacts are ready

6. **Submit to App Stores**
   - **iOS (App Store):**
     - Upload to App Store Connect using Transporter or Xcode
     - Fill out App Store listing information
     - Submit for review
   - **Android (Google Play Store):**
     - Upload AAB to Google Play Console
     - Fill out Play Store listing information
     - Submit for review
   - Capture and display submission confirmation
   - Make sure their app is submitted for review

7. **Verify submission**
   - Confirm submission was successful
   - Check for any submission errors
   - Tell them their app is submitted for review!

8. **Document production publication**
   - Create `doc/` folder if it doesn't exist
   - Create file: `doc/go-live-production-{feature-name}-YYYY-MM-DD.md`
   - Document: quality checks performed, issues found and fixed, production publication details, date, version, platform, what was published
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
- Build production versions - Explain: "I'm creating the final versions of your app for the App Store and Play Store"
- Submit to App Stores - Explain: "I'm submitting your app to Apple and Google for review - this is like submitting a book to publishers. They'll review it and then make it available to everyone!"
- Only publish to production if everything is ready - fix issues first if needed
- Guide them step-by-step through App Store Connect / Google Play Console setup (if first time)
- Tell them their app submission status when it's submitted - Celebrate: "Your app is now submitted for review! Apple and Google will review it, and once approved, it will be available to everyone!"
- If something goes wrong, help them fix it - Explain: "Something went wrong, but don't worry - I'll fix it. Here's what happened: [simple explanation]"
- Celebrate when all checks pass and the app is submitted! - "🎉 Congratulations! Your app is now submitted for review!"

## Important Notes

- **App Store requirements:** iOS apps require Apple Developer account ($99/year), App Store Connect setup, and code signing certificates.
- **Google Play requirements:** Android apps require Google Play Developer account ($25 one-time), Google Play Console setup, and signing keys.
- **Review process:** Both stores have review processes that can take 1-7 days. Apps must meet their guidelines.
- **Version bumping:** Version numbers must be incremented for each release (semantic versioning recommended).
- **Build time:** Production builds can take 20-60 minutes depending on platform and project size.
- **EAS Build:** For Expo projects, EAS Build simplifies the build and submission process significantly.

## See Also

- **[Test App](test-app.md)**: Run tests explicitly when needed
- **[Fix Issues](fix-issues.md)**: Fix any issues before publishing
- **[Preview App](preview-app.md)**: Create preview before going live



