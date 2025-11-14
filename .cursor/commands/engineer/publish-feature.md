# Publish Feature Preview

Intelligently checks if everything is ready, then guides you through publishing a preview of your feature so you can test it and share it with others. Creates a preview URL you can share - perfect for getting feedback before going live!

1. **Run basic checks (if needed)**
   - Check if project builds successfully
   - Check if there are obvious errors
   - **Run tests:** Use `run-tests.md` approach - make sure tests pass (if tests exist)
   - Only run checks that are needed - skip if already verified recently
   - Tell the user what you're checking

2. **Check if ready to publish preview**
   - Check if project builds successfully
   - Check if code is saved to Git (commit if needed)
   - Check if Vercel CLI is installed and user is logged in
   - Check if preview environment variables are set (if needed)
   - Tell the user what you found

3. **Fix issues if needed**
   - **If build fails:** Use `build-project.md` approach - fix build issues
   - **If tests fail:** Use `run-tests.md` approach - fix test failures
   - **If code not saved:** Automatically commit changes to Git
   - **If Vercel CLI not installed/logged in:** Guide them through Vercel CLI setup (install, login, link project)

4. **Publish preview (create shareable link)**
   - **Automatically push branch** - Push current branch to GitHub
   - **Deploy using Vercel CLI** - Use `vercel` command to deploy preview directly
   - **If first time:** Guide them through Vercel CLI setup (login, link project)
   - **If already linked:** Deploy preview using `vercel --yes` (non-interactive)
   - Capture and display the preview URL from Vercel CLI output
   - Make sure their feature preview is accessible via URL

5. **Verify preview works**
   - Test that the preview works
   - Check for any obvious problems
   - Tell them their preview URL is ready to share!

6. **Document preview**
   - Create `doc/` folder if it doesn't exist
   - Create file: `doc/preview-{feature-name}-YYYY-MM-DD.md`
   - Document: preview details, date, preview URL, branch/PR, what was previewed
   - Extract feature name from context (lowercase with hyphens)
   - Include build status and preview URL

## What to Tell the User

- Explain you're checking if everything is ready to create a preview
- List what you're checking (e.g., "Checking if it builds...")
- Only run checks that are needed - skip if already verified recently
- If you find problems, explain them simply and fix them
- Show progress of each check
- List what you found (e.g., "Build successful! Pushing branch...")
- Automatically push branch to GitHub
- Deploy preview using Vercel CLI (use `vercel --yes` for non-interactive deployment)
- Only create preview if everything is ready - fix issues first if needed
- Guide them step-by-step through Vercel CLI setup (if first time - login, link project)
- Tell them their preview URL when it's ready (from Vercel CLI output)
- Explain that they can share this URL with others to get feedback
- Explain that previews are temporary and won't affect production
- If something goes wrong, help them fix it
- Celebrate when preview is ready!

## See Also

- **[Run Tests](.cursor/commands/run-tests.md)**: Run tests before publishing preview
- **[Create PR](.cursor/commands/create-pr.md)**: Create pull request for code review
- **[Build Project](.cursor/commands/build-project.md)**: Build project before publishing