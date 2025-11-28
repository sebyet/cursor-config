# Test App

Automatically tests your React Native application! First tests the last feature you worked on, gives you feedback, then tests the entire app. Perfect for catching bugs before they reach production!

## What This Does

1. **Identify the last feature**
   - Check git history to find the most recent feature or changes
   - Look at recent commits, changed files, and branch names
   - Identify what was last worked on

2. **Test the last feature first**
   - Run unit tests for the feature if they exist
   - Test key interactions and flows
   - Check for errors, broken functionality, and UX issues
   - Provide detailed feedback on what works and what doesn't

3. **Test the full app**
   - Run all unit tests
   - Test complete user flows from start to finish
   - Verify navigation, forms, interactions, and critical paths
   - Check for regressions and broken functionality
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

### 2. Run Unit Tests

**Check if tests exist:**
```bash
# Look for test files
find . -name "*.test.ts" -o -name "*.test.tsx" -o -name "*.spec.ts" -o -name "*.spec.tsx"

# Check Jest configuration
cat package.json | grep -A 10 "jest"
```

**Run tests:**
```bash
# Run all tests
pnpm test
# or
npm test

# Run tests in watch mode (for development)
pnpm test --watch

# Run tests with coverage
pnpm test --coverage
```

**For React Native Testing Library:**
- Tests should use `@testing-library/react-native`
- Test user interactions, not implementation details
- Use accessibility queries when possible

### 3. Test the Last Feature First

**Run feature-specific tests:**
- Run tests for files related to the last feature
- Test key interactions specific to that feature
- Verify expected behaviors work correctly

**Check for issues:**
- Look for test failures
- Check for console errors
- Verify visual elements render correctly
- Test responsive behavior if applicable

**Document findings:**
- Note what works correctly
- List any bugs or issues found
- Record steps to reproduce issues

### 4. Test the Full App

**Run all tests:**
- Run complete test suite
- Verify all tests pass
- Check for any regressions

**Test complete flows:**
- Navigation flows
- Form submissions
- Data display and updates
- Error handling
- Edge cases

**Verify integration:**
- Ensure features work together
- Check for broken navigation
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

**When running tests:**
- "Running tests for your latest feature..."
- "Checking [specific interaction]..."
- "Verifying [specific behavior]..."

**When providing feedback:**
- "✅ [Feature] is working correctly!"
- "⚠️ Found an issue: [description]"
- "🔍 Testing complete! Here's what I found:"
  - List all test results
  - Highlight any issues
  - Offer to fix problems

**When testing full app:**
- "Now testing the complete app..."
- "Verifying all features work together..."
- "Checking navigation and flows..."

**When done:**
- "All tests complete! Here's the summary:"
  - Feature test results
  - Full app test results
  - Overall status
- "Everything looks good!" or "Found [X] issues that need attention"
- "Would you like me to fix any issues I found?"

---

## Important Notes

- **Test framework:** React Native uses Jest for unit testing. React Native Testing Library for component testing.
- **E2E testing:** For end-to-end testing, consider Detox or Maestro (separate from this command).
- **Git history:** We use git to identify the last feature. Make sure changes are committed for better tracking.
- **Test scope:** We test both the specific feature and the full app to catch both feature-specific bugs and integration issues.
- **Feedback format:** Results are provided in clear, actionable format - what works, what doesn't, and how to fix it.
- **Automatic fixes:** If issues are found, we can automatically fix them if you'd like!
- **Platform testing:** Consider testing on both iOS and Android simulators/emulators for platform-specific issues.

---

## Example Test Scenarios

**For a login feature:**
- Test form validation
- Test successful login
- Test error handling
- Verify navigation after login
- Test logout functionality

**For a form feature:**
- Test all form fields
- Test validation
- Test form submission
- Verify success/error states
- Test form reset

**For a navigation feature:**
- Test all navigation links
- Verify screens load correctly
- Test back navigation
- Check active states
- Verify tab navigation (if applicable)

**For a data display feature:**
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









