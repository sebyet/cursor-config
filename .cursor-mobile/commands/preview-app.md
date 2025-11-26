# Preview App

Intelligently checks if everything is ready, then guides you through creating a preview build of your React Native app so you can test it and share it with others. Creates a preview build you can share - perfect for getting feedback before going live!

1. **Run basic checks (if needed)**
   - Check if project builds successfully
   - Check if there are obvious errors
   - **Run tests:** Make sure tests pass (if tests exist)
   - Only run checks that are needed - skip if already verified recently
   - Tell the user what you're checking

2. **Check if ready to create preview**
   - Check if project builds successfully
   - Check if code is saved to Git (commit if needed)
   - Check if Expo/EAS CLI is installed (for Expo projects)
   - Check if preview environment variables are set (if needed)
   - Tell the user what you found

3. **Fix issues if needed**
   - **If build fails:** Fix build issues
   - **If tests fail:** Fix test failures
   - **If code not saved:** Automatically commit changes to Git
   - **If Expo/EAS CLI not installed:** Guide them through setup (install, login, configure)

4. **Create preview build**
   - **For Expo projects:** Use EAS Build to create a preview build
     - `eas build --profile preview --platform ios`
     - `eas build --profile preview --platform android`
   - **For React Native CLI:** Create development build
     - iOS: Archive and create .ipa file
     - Android: Create APK or AAB file
   - **Push to TestFlight (iOS)** or **Internal Testing (Android)** if configured
   - Capture and display the preview build URL or installation instructions
   - Make sure their feature preview is accessible

5. **Verify preview works**
   - Test that the preview build works
   - Check for any obvious problems
   - Tell them their preview is ready to share!

6. **Document preview**
   - Create `doc/` folder if it doesn't exist
   - Create file: `doc/preview-{feature-name}-YYYY-MM-DD.md`
   - Document: preview details, date, build URL, platform, what was previewed
   - Extract feature name from context (lowercase with hyphens)
   - Include build status and installation instructions

## What to Tell the User

- Explain you're checking if everything is ready to create a preview
- List what you're checking (e.g., "Checking if it builds...")
- Only run checks that are needed - skip if already verified recently
- If you find problems, explain them simply and fix them
- Show progress of each check
- List what you found (e.g., "Build successful! Creating preview...")
- Automatically commit changes if needed
- Create preview build using EAS Build (Expo) or native build tools
- Only create preview if everything is ready - fix issues first if needed
- Guide them step-by-step through EAS CLI setup (if first time - login, configure project)
- Tell them their preview build URL or installation instructions when it's ready
- Explain that they can share this build with others to get feedback
- Explain that preview builds are for testing and won't affect production
- If something goes wrong, help them fix it
- Celebrate when preview is ready!

## Important Notes

- **Expo projects:** Use EAS Build for easy preview builds. Requires EAS account and configuration.
- **React Native CLI:** Requires manual build process with Xcode (iOS) or Android Studio (Android).
- **TestFlight (iOS):** For iOS previews, TestFlight is the easiest way to share builds.
- **Internal Testing (Android):** For Android previews, use Google Play Internal Testing or share APK directly.
- **Build time:** Preview builds can take 10-30 minutes depending on platform and project size.
- **EAS CLI:** For Expo projects, EAS CLI needs to be installed and configured: `npm install -g eas-cli`

## See Also

- **[Test App](test-app.md)**: Run tests before creating preview
- **[Fix Issues](fix-issues.md)**: Fix any issues before previewing
- **[Go Live](go-live.md)**: Deploy to production after preview



