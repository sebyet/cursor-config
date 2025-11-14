# Build Project

Prepares your project to go live online. Think of it like packaging your app so it works fast and smooth for everyone.

1. **Check if ready to build**
   - Check if all tools are installed
   - Check if dependencies are installed
   - Check for code errors (compilation errors)
   - Check if build was done recently (maybe skip if nothing changed)
   - Tell the user what you found

2. **Fix issues if needed**
   - **If tools missing:** Install missing tools
   - **If dependencies missing:** Install dependencies
   - **If code errors exist:** Use `fix-compile-errors.md` approach - fix errors first
   - **If build outdated:** Proceed with build

3. **Build it**
   - Package everything together
   - Tell the user what's happening
   - Wait for it to finish
   - Show progress

4. **Verify it worked**
   - Check that everything built correctly
   - Tell them if there are any warnings
   - Confirm it's ready to go live

## What to Tell the User

- Explain you're checking if everything is ready to build
- List what you found (e.g., "All tools installed, no errors found - ready to build!")
- Only build if ready - fix issues first if needed
- Show them the progress as it builds
- If there are errors, explain what they mean in simple words
- If it succeeds, tell them it's ready to deploy
- If it fails, explain what went wrong and how to fix it