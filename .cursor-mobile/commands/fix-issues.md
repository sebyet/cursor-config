# Fix Issues

Intelligently checks what's wrong with your React Native app and fixes only the problems that exist. Think of it as a smart "fix everything" button that only fixes what needs fixing!

1. **Check what's wrong first**
   - Look for code errors (compilation errors, TypeScript errors, syntax issues, missing imports, type mismatches)
   - Check for bugs (things not working, runtime errors, logic issues)
   - Check Git status (uncommitted changes, merge conflicts, branch issues, repository problems)
   - Check code quality (formatting/style issues, linting violations, code smells)
   - Check test status (failing tests, test errors)
   - Check for AI-generated slop (extra comments, defensive checks, unnecessary try/catch, type casts to any)
   - Check Metro bundler issues (cache problems, module resolution)
   - Check platform-specific issues (iOS pod issues, Android gradle issues)
   - Tell the user what you found

2. **Fix only what needs fixing**
   - **If compilation errors exist:** Fix TypeScript errors, syntax errors, missing imports, type mismatches, undefined references
   - **If bugs exist:** Reproduce bugs, analyze error logs, identify root causes, trace errors to source, fix code paths, add error handling
   - **If Git issues exist:** Commit or stash uncommitted changes, resolve merge conflicts, fix branch state, fix repository connection, abort rebase if needed
   - **If code quality issues:** Run linter, fix formatting automatically, fix style violations, apply project standards
   - **If AI slop exists:** Remove extra comments inconsistent with codebase, remove unnecessary defensive checks/try-catch blocks, remove casts to any, fix inconsistent styles
   - **If Metro bundler issues:** Clear Metro cache (`npx react-native start --reset-cache`), fix module resolution, reinstall dependencies
   - **If iOS pod issues:** Run `pod install` in ios directory, fix Podfile issues, update CocoaPods
   - **If Android gradle issues:** Clean gradle (`cd android && ./gradlew clean`), fix build.gradle issues, sync project

3. **Verify everything works**
   - Run tests to confirm fixes worked
   - Try building the app
   - Make sure nothing broke
   - Confirm everything is working

## What to Tell the User

**For Non-Technical Users:**
- Explain in simple terms: "Let me check what's wrong with your app..."
- List what problems you found in plain English (don't fix things that aren't broken!)
  - Instead of "TypeScript compilation errors", say "Some code isn't working correctly"
  - Instead of "Git merge conflicts", say "Some changes need to be combined"
  - Instead of "Linting violations", say "Some formatting needs to be cleaned up"
  - Instead of "Metro cache issues", say "The app builder needs to be refreshed"
- Fix only the problems that exist
- Skip steps that aren't needed (e.g., "Everything looks good with saving your work - no issues there!")
- Show what you're fixing in simple terms: "I'm fixing the code so it works properly..."
- Test that everything works: "Let me make sure everything works now..."
- Tell them when it's all fixed: "All done! Everything is working now. Here's what I fixed: [simple list]"

## Mobile-Specific Fixes

**Metro Bundler Issues:**
- Clear cache: `npx react-native start --reset-cache`
- Reset Metro: `npx react-native start --reset-cache --reset-metro`
- Reinstall dependencies: `rm -rf node_modules && pnpm install`

**iOS Issues:**
- Pod install: `cd ios && pod install && cd ..`
- Clean build: `cd ios && xcodebuild clean && cd ..`
- Reset simulator: Delete app from simulator, restart simulator

**Android Issues:**
- Clean gradle: `cd android && ./gradlew clean && cd ..`
- Rebuild: `cd android && ./gradlew assembleDebug && cd ..`
- Reset emulator: Wipe data in Android Studio AVD Manager

**Native Module Issues:**
- Rebuild native code: `npx react-native run-ios` or `npx react-native run-android`
- Check native module linking
- Verify platform-specific code is correct











