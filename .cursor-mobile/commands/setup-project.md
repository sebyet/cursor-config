# Setup Project

Get your brand new React Native project ready to go! I'll check everything you need, install all the packages, set up your development environment, and make sure you're ready to start building. Just run this command and I'll handle all the technical setup automatically!

## What This Does

1. **Check your tools** - Make sure Node.js, Git, and development tools are installed (I'll help install them if needed!)
2. **Set up React Native** - Initialize your React Native project with Expo or React Native CLI
3. **Install all packages** - Get everything from your tech stack ready to use, including navigation, state management, and UI libraries
4. **Set up platform dependencies** - Configure iOS (Xcode, CocoaPods) and Android (Android Studio, JDK) if needed
5. **Show you what's ready** - Give you a clear summary of everything that's set up

**Note:** This command gets everything ready, but doesn't start your app or customize your design system - we'll do those separately!

---

## Technical Steps

### 1. Check/Install Node.js & pnpm

**Check if Node.js is installed:**
- Run `node --version` to see if it's there
- If not installed: I'll guide you to install Node.js from nodejs.org (it's free and easy!)
- If installed but outdated: I'll recommend updating to the latest LTS version

**Check if pnpm is installed:**
- Run `pnpm --version` to see if it's there
- If not installed: I'll install it for you with `npm install -g pnpm`
- pnpm is faster than npm, so we'll use it for everything!

**Don't proceed until both are ready:**
- I'll make sure everything is installed before moving on
- If something needs your help, I'll tell you exactly what to do!

### 2. Check/Install Git

**Check if Git is installed:**
- Run `git --version` to see if it's there
- If not installed: I'll help you install it:
  - macOS: `brew install git`
  - Linux: Use your package manager (apt, yum, etc.)
  - Windows: Download from git-scm.com

**Check Git authentication:**
- Check if you've set up your name: `git config --global user.name`
- Check if you've set up your email: `git config --global user.email`
- If not authenticated: I'll help you configure it:
  - `git config --global user.name "Your Name"`
  - `git config --global user.email "your.email@example.com"`

**Don't proceed until Git is ready:**
- Git needs to know who you are to save your work properly
- I'll make sure everything is set up before moving on!

### 3. Initialize React Native Project

**Check if project already exists:**
- Check if `package.json` exists
- Check if React Native dependencies are installed
- If project exists: Skip initialization, proceed to package installation
- If no project: Initialize new React Native project

**Initialize with Expo (recommended):**
```bash
npx create-expo-app@latest . --template blank-typescript
```

**OR initialize with React Native CLI:**
```bash
npx react-native@latest init ProjectName --template react-native-template-typescript
```

**Choose based on:**
- Expo: Easier setup, managed workflow, great for most apps
- React Native CLI: More control, native modules, custom native code

### 4. Check/Install iOS Dependencies (macOS only)

**Check if Xcode is installed:**
- Run `xcodebuild -version` to check
- If not installed: Guide user to install from App Store (required for iOS development)
- Check if Xcode Command Line Tools are installed: `xcode-select -p`

**Check if CocoaPods is installed:**
- Run `pod --version` to check
- If not installed: Install with `sudo gem install cocoapods`
- CocoaPods manages iOS dependencies

**Don't proceed until iOS tools are ready (if targeting iOS):**
- iOS development requires macOS and Xcode
- I'll verify everything is set up before moving on!

### 5. Check/Install Android Dependencies

**Check if Android Studio is installed:**
- Check common installation paths
- If not installed: Guide user to install Android Studio
- Check if Android SDK is configured

**Check if JDK is installed:**
- Run `java -version` to check
- Check for JAVA_HOME environment variable
- If not installed: Guide user to install JDK (Java Development Kit)

**Configure Android environment:**
- Check ANDROID_HOME environment variable
- Verify Android SDK path is set correctly

**Don't proceed until Android tools are ready (if targeting Android):**
- Android development requires Android Studio and JDK
- I'll verify everything is set up before moving on!

### 6. Install All Tech Stack Packages

I'll install all the packages you need for your React Native project:

**For Expo projects (use Expo-compatible versions):**
```bash
# First, install Expo-compatible native modules (ensures correct versions for SDK)
npx expo install react-native-reanimated react-native-gesture-handler react-native-screens react-native-safe-area-context react-native-keyboard-controller react-native-web

# Then install other packages with pnpm
# Virtualized Lists (better than FlatList for dynamic heights)
pnpm add @legendapp/list

# Navigation
pnpm add @react-navigation/native @react-navigation/native-stack @react-navigation/bottom-tabs

# Native Menus (iOS)
pnpm add zeego react-native-ios-context-menu

# Data Fetching
pnpm add @tanstack/react-query

# State Management
pnpm add zustand

# Forms & Validation
pnpm add react-hook-form zod @hookform/resolvers

# Utilities
pnpm add date-fns clsx

# Development Tools
pnpm add -D prettier eslint-config-prettier @typescript-eslint/eslint-plugin @typescript-eslint/parser
```

**For React Native CLI projects:**
```bash
# Core React Native Libraries
pnpm add react-native-reanimated react-native-gesture-handler
pnpm add react-native-keyboard-controller react-native-web

# Virtualized Lists (better than FlatList for dynamic heights)
pnpm add @legendapp/list

# Navigation
pnpm add @react-navigation/native @react-navigation/native-stack @react-navigation/bottom-tabs
pnpm add react-native-screens react-native-safe-area-context

# Native Menus (iOS)
pnpm add zeego react-native-ios-context-menu

# Data Fetching
pnpm add @tanstack/react-query

# State Management
pnpm add zustand

# Forms & Validation
pnpm add react-hook-form zod @hookform/resolvers

# Utilities
pnpm add date-fns clsx

# Development Tools
pnpm add -D prettier eslint-config-prettier @typescript-eslint/eslint-plugin @typescript-eslint/parser
```

**Important for Expo projects:**
- Use `npx expo install` for native modules to ensure SDK-compatible versions
- `react-native-web` is required for web support in Expo
- `@legendapp/list` is the correct package name (not `legend-list`)
- **Styling:** For Expo Go compatibility, use a React Context-based theme system instead of `react-native-unistyles` (which requires native modules). See theme setup below.

**What happens:**
- All core libraries are installed
- Navigation is set up for stack and tab navigation
- State management and data fetching are ready
- Development tools are installed

**Note on Styling:**
- For Expo Go compatibility, we use a custom React Context-based theme system
- `react-native-unistyles` requires native modules and won't work in Expo Go
- Theme system setup and customization is handled by the `customize-app` command

### 7. Configure Metro Bundler

**For Expo projects:**
- Metro is pre-configured by Expo
- Create `metro.config.js` with default Expo config (don't add Reanimated transformer here - that goes in babel.config.js)
- Example:
```javascript
// Learn more https://docs.expo.dev/guides/customizing-metro
const { getDefaultConfig } = require('expo/metro-config');

/** @type {import('expo/metro-config').MetroConfig} */
const config = getDefaultConfig(__dirname);

module.exports = config;
```

**Important:** 
- Do NOT add `babelTransformerPath` for Reanimated in metro.config.js
- Reanimated is configured in babel.config.js only (see step 8)
- Metro uses the default Babel transformer, which reads from babel.config.js

**For React Native CLI projects:**
- Configure Metro for Reanimated and other libraries
- Set up asset extensions
- Configure transformer options as needed

### 8. Configure Babel

**Create or update babel.config.js:**

**For Expo projects:**
```javascript
module.exports = function(api) {
  api.cache(true);
  return {
    presets: ['babel-preset-expo'],
    plugins: [
      'react-native-reanimated/plugin', // Must be last
    ],
  };
};
```

**Important:**
- Reanimated plugin MUST be the last plugin in the plugins array
- This is where Reanimated is configured, NOT in metro.config.js

**For React Native CLI projects:**
- Configure babel.config.js with Reanimated plugin as the last plugin
- Add any other Babel plugins as needed

### 9. Set Up Platform-Specific Configuration

**iOS (if using React Native CLI):**
```bash
cd ios && pod install && cd ..
```

**Android:**
- Verify `android/gradle.properties` is configured
- Check `android/build.gradle` settings

**For Expo:**
- Platform setup is handled automatically
- Run `npx expo prebuild` if you need native code

### 10. Summary

At the end, I'll give you a clear summary of everything that's ready:

```
✅ Setup Complete

What was installed:
- Node.js: [version]
- Git: [version]
- React Native: [version]
- State Management: Zustand
- Navigation: React Navigation
- Forms: React Hook Form, Zod
- Animations: React Native Reanimated
- Keyboard Handling: React Native Keyboard Controller (Expo-compatible version)
- Virtualized Lists: @legendapp/list
- Styling: React Context-based theme system (Expo Go compatible)
- Data Fetching: Tanstack Query
- Native Menus: Zeego (iOS)
- Web Support: react-native-web
- Utilities: date-fns, clsx
- Development Tools: Prettier, ESLint

Platforms configured:
- iOS: [Ready/Not configured]
- Android: [Ready/Not configured]
```

---

## What to Tell the User

**When starting:**
- "Let me set up your new React Native project! I'll check everything you need and install all the packages."
- "First, let me make sure you have all the tools installed..."
- "Checking Node.js, Git, and development tools..."

**When checking tools:**
- "Great! Node.js is installed ([version])"
- "I see pnpm isn't installed yet - let me install it for you!"
- "Git looks good! Let me check if it's configured..."
- "I need to set up your Git name and email - this helps save your work properly"

**When setting up React Native:**
- "Setting up your React Native project..."
- "I'll use Expo for easier development - you can always switch later if needed!"
- "Initializing your project with TypeScript..."

**When checking platform dependencies:**
- "Checking iOS development tools..." (macOS only)
- "Checking Android development tools..."
- "Xcode looks good!" or "You'll need Xcode for iOS development - I'll guide you through installing it"
- "Android Studio looks good!" or "You'll need Android Studio for Android development"

**When installing packages:**
- "Now I'll install all the packages you need - this might take a minute!"
- "For Expo projects, I'll use `npx expo install` to ensure SDK-compatible versions..."
- "Installing Expo-compatible native modules..."
- "Installing navigation libraries..."
- "Setting up state management tools..."
- "Installing animation libraries..."
- "Setting up keyboard handling..."
- "Adding web support..."
- "Note: Using React Context for theming (works with Expo Go) instead of native modules..."
- "Almost done! Just setting up a few more things..."

**When done:**
- "All set! Your React Native project is ready to go! 🎉"
- "Here's everything I set up for you:"
- **Show the summary clearly**
- "You're all ready to start building! Want me to help you add your first feature?"

**If something needs user help:**
- "I need your help with one thing..."
- "Could you install Node.js from nodejs.org? It's free and takes just a few minutes!"
- "I need to set up your Git name and email - what should I use?"
- "You'll need Xcode for iOS development - here's how to install it..."
- "You'll need Android Studio for Android development - here's how to install it..."

**If something goes wrong:**
- "Hmm, I ran into an issue. Let me explain what happened..."
- "Don't worry, I'll help you fix this!"
- "Once that's fixed, we can continue!"

---

## Checklist

- [ ] Checked Node.js installation (`node --version`)
- [ ] Installed Node.js if needed
- [ ] Checked pnpm installation (`pnpm --version`)
- [ ] Installed pnpm if needed (`npm install -g pnpm`)
- [ ] Checked Git installation (`git --version`)
- [ ] Installed Git if needed
- [ ] Checked Git authentication (`git config --global user.name` and `git config --global user.email`)
- [ ] Configured Git authentication if needed
- [ ] Initialized React Native project (Expo or React Native CLI)
- [ ] Checked Xcode installation (macOS, iOS development)
- [ ] Checked CocoaPods installation (iOS development)
- [ ] Checked Android Studio installation (Android development)
- [ ] Checked JDK installation (Android development)
- [ ] Installed all tech stack packages (using `npx expo install` for Expo projects)
- [ ] Installed react-native-web for web support (Expo projects)
- [ ] Configured Metro bundler (default Expo config, no Reanimated transformer)
- [ ] Configured Babel with Reanimated plugin (must be last plugin)
- [ ] Set up iOS dependencies (pod install) if using React Native CLI
- [ ] Configured Android build settings if using React Native CLI
- [ ] Provided summary of what was installed

---

## Important Notes

- **Prerequisites:** Node.js (LTS), pnpm, Git must be installed before proceeding - but don't worry, I'll help you install them if needed!
- **Platform Setup:** iOS development requires macOS and Xcode. Android development requires Android Studio and JDK.
- **Expo vs React Native CLI:** Expo is recommended for easier setup and development. React Native CLI gives more control for native modules.
- **Git Authentication:** Git needs to know who you are - I'll help you set this up if it's not already configured
- **Package Manager:** I'll use `pnpm` for everything (it's faster!) - I'll install it if you don't have it
- **Expo Package Versions:** For Expo projects, use `npx expo install` for native modules to ensure SDK-compatible versions (especially react-native-keyboard-controller)
- **Metro Config:** For Expo projects, use default Metro config - Reanimated is configured in Babel, not Metro
- **Web Support:** react-native-web is installed for Expo projects to enable web platform support
- **Styling System:** For Expo Go compatibility, use React Context-based theme system instead of `react-native-unistyles` (which requires native modules). If you need native modules, use `expo-dev-client` for development builds.
- **Expo Go Limitations:** Expo Go doesn't support custom native modules. Use React Context for theming, or create a development build with `expo-dev-client` if you need native modules.
- **No App Start:** This command gets everything ready, but doesn't start your development server - you can do that separately!
- **No Customization:** This command doesn't customize your design system - we'll do that in another step!
- **Summary Required:** I'll always show you a clear summary at the end so you know exactly what's ready
- **Note:** This assumes you're in an empty directory or want to initialize a new project - make sure you're in the right place when you run this!



