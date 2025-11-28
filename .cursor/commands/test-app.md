# Test App

Automatically tests your application using Playwright! First tests the last feature you worked on, gives you feedback, then tests the entire user journey. Perfect for catching bugs before they reach production!

## What This Does

1. **Identify the last feature**
   - Check git history to find the most recent feature or changes
   - Look at recent commits, changed files, and branch names
   - Identify what was last worked on

2. **Test the last feature first**
   - Start the development server if needed
   - Navigate to the feature using Playwright
   - Test key interactions and flows
   - Check for errors, broken functionality, and UX issues
   - Provide detailed feedback on what works and what doesn't

3. **Test the full user journey**
   - Test complete user flows from start to finish
   - Verify navigation, forms, interactions, and critical paths
   - Check for regressions and broken links
   - Ensure everything works together

4. **Provide comprehensive feedback**
   - Summarize test results clearly
   - Highlight any issues found
   - Suggest fixes if problems are detected
   - Celebrate when everything passes!

---

## Technical Steps

### 1. Identify the Last Feature

**Check git history to find recent work:**
```bash
# Get the most recent commit message
git log -1 --pretty=format:"%s"

# Get recent changed files
git diff --name-only HEAD~1 HEAD

# Check current branch name (might indicate feature)
git branch --show-current

# Check recent commits with feature-related keywords
git log --oneline -10 | grep -i "feat\|feature\|add\|fix"
```

**Identify what was changed:**
- Look at commit messages for feature descriptions
- Check changed files to understand scope
- Review branch names for feature context
- Check `doc/` folder for recent feature documentation
- If unclear, ask user what they last worked on

**Determine test scope:**
- Map files to features/components
- Identify key user flows for that feature
- Plan test scenarios

### 2. Ensure Server is Running

**Check if server is running:**
```bash
# Check if port 3000 is in use
lsof -ti:3000 || echo "Port 3000 is free"

# Check for Next.js dev server
ps aux | grep "next dev" | grep -v grep
```

**Start server if needed:**
- If not running, start development server:
  ```bash
  # Check package manager
  [ -f pnpm-lock.yaml ] && pnpm dev || npm run dev
  ```
- Wait for server to be ready (look for "Ready" message)
- Note the URL (usually `http://localhost:3000`)

**Verify server is accessible:**
- Use Playwright to navigate to the base URL
- Check that the page loads successfully
- Confirm no critical errors

### 3. Test the Last Feature First

**Navigate to the feature:**
- Use Playwright MCP to navigate to the relevant page/route
- Take a snapshot to see the current state
- Identify key interactive elements

**Test key interactions:**
- Click buttons, links, and interactive elements
- Fill forms if applicable
- Test user flows specific to the feature
- Verify expected behaviors work correctly

**Check for issues:**
- Look for console errors (use browser_console_messages)
- Check network requests for failures (use browser_network_requests)
- Verify visual elements render correctly
- Test responsive behavior if applicable
- Check accessibility basics (focus, keyboard navigation)

**Document findings:**
- Note what works correctly
- List any bugs or issues found
- Capture screenshots of problems if needed
- Record steps to reproduce issues

### 4. Test the Full User Journey

**Identify critical user flows:**
- Homepage → Feature discovery
- Authentication flow (if applicable)
- Main feature interactions
- Navigation between pages
- Form submissions
- Data display and updates

**Test complete flows:**
- Start from the homepage
- Navigate through key pages
- Test end-to-end user scenarios
- Verify data persistence (if applicable)
- Check error handling
- Test edge cases

**Verify integration:**
- Ensure features work together
- Check for broken links or navigation
- Verify consistent UI/UX
- Test cross-feature interactions

### 5. Provide Comprehensive Feedback

**Summarize test results:**
- List all tests performed
- Show pass/fail status for each test
- Highlight critical issues vs minor issues
- Provide clear, actionable feedback

**If issues found:**
- Describe each issue clearly
- Provide steps to reproduce
- Suggest potential fixes
- Offer to fix issues automatically

**If all tests pass:**
- Celebrate success!
- Confirm feature is working correctly
- Note any observations or recommendations

---

## What to Tell the User

**When starting:**
- "Let me check what you last worked on, then I'll test it automatically!"
- "Checking git history to find your last feature..."

**When identifying the feature:**
- "Found your last feature: [feature name]"
- "I can see you worked on [description]. Let me test it now!"
- If unclear: "I see recent changes but want to confirm - what feature did you last work on?"

**When starting server:**
- "Making sure your server is running..."
- "Server is ready! Starting tests..."

**When testing the last feature:**
- "Testing your latest feature: [feature name]..."
- "Checking [specific interaction]..."
- "Verifying [specific behavior]..."

**When providing feedback:**
- "✅ [Feature] is working correctly!"
- "⚠️ Found an issue: [description]"
- "🔍 Testing complete! Here's what I found:"
  - List all test results
  - Highlight any issues
  - Offer to fix problems

**When testing full journey:**
- "Now testing the complete user journey..."
- "Verifying all features work together..."
- "Checking navigation and flows..."

**When done:**
- "All tests complete! Here's the summary:"
  - Feature test results
  - Full journey test results
  - Overall status
- "Everything looks good!" or "Found [X] issues that need attention"
- "Would you like me to fix any issues I found?"

**If server issues:**
- "I need to start your server first..."
- "Server is starting, just a moment..."
- "Server is ready! Now testing..."

**If Playwright MCP not available:**
- "I need Playwright MCP to run automated tests. Let me check if it's configured..."
- "Playwright MCP tools aren't available. Would you like me to help set it up?"

---

## Important Notes

- **Server dependency:** Tests require the development server to be running. We'll start it automatically if needed.
- **Git history:** We use git to identify the last feature. Make sure changes are committed for better tracking.
- **Playwright MCP:** This command requires Playwright MCP tools to be configured and available.
- **Test scope:** We test both the specific feature and the full journey to catch both feature-specific bugs and integration issues.
- **Feedback format:** Results are provided in clear, actionable format - what works, what doesn't, and how to fix it.
- **Automatic fixes:** If issues are found, we can automatically fix them if you'd like!
- **Screenshots:** We capture screenshots of issues when helpful for debugging.
- **Console errors:** We check browser console for JavaScript errors automatically.
- **Network issues:** We monitor network requests to catch API failures or slow responses.

---

## Example Test Scenarios

**For a login feature:**
- Navigate to login page
- Test form validation
- Test successful login
- Test error handling
- Verify redirect after login
- Test logout functionality

**For a form feature:**
- Navigate to form page
- Test all form fields
- Test validation
- Test form submission
- Verify success/error states
- Test form reset

**For a navigation feature:**
- Test all navigation links
- Verify pages load correctly
- Test back/forward navigation
- Check active states
- Verify mobile menu (if applicable)

**For a data display feature:**
- Navigate to data page
- Verify data loads correctly
- Test filtering/sorting (if applicable)
- Test pagination (if applicable)
- Verify empty states
- Test error states

---

## Integration with Other Commands

- **Before `@preview-app`:** Run this to ensure feature works before creating preview
- **After `@add-feature`:** Automatically test new features after building
- **Before `@go-live`:** Critical step to catch bugs before going live
- **With `@fix-issues`:** Use test results to identify what needs fixing

