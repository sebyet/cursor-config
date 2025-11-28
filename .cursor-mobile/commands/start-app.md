# Start App

Friendly, conversational React Native app startup. Kills any running Metro bundlers, starts your development server fresh, and launches your app on iOS or Android so you can see it in action right away!

## What This Does

1. **Stop any running Metro bundlers**
   - Check if there's already a Metro bundler running
   - Stop it so we can start fresh
   - Make sure nothing is blocking the way

2. **Start your Metro bundler**
   - Start up your Metro bundler so your app can load
   - Wait for it to be ready
   - Watch for when it's all set to go

3. **Launch your app**
   - Start your app on iOS simulator or Android emulator
   - Or connect to a physical device
   - Show you how to see your app running!

---

## Technical Steps

### 1. Stop Any Running Metro Bundlers

**Find and stop any Metro bundlers that might be running:**
```bash
# Stop anything on port 8081 (Metro's default port)
lsof -ti:8081 | xargs kill -9 2>/dev/null || true

# Stop any Metro bundlers
pkill -f "react-native start" 2>/dev/null || true
pkill -f "expo start" 2>/dev/null || true
pkill -f "metro" 2>/dev/null || true
```

**Make sure everything is clear:**
- Check that port 8081 is free
- If something is still running, try other ways to stop it

### 2. Start Your Metro Bundler

**Figure out which tool to use:**
- Check if you're using Expo (look for `app.json` or `app.config.js`)
- Check if you're using React Native CLI (look for `android/` and `ios/` folders)
- Check package manager (look for `pnpm-lock.yaml` or `package-lock.json`)

**Start the Metro bundler:**
```bash
# For Expo projects
npx expo start

# OR for React Native CLI projects
npx react-native start

# OR using pnpm/npm scripts
pnpm start
# or
npm start
```

**Wait for it to be ready:**
- Watch the output for "Metro waiting on..." message
- Look for the QR code (Expo) or "Metro Bundler ready" message
- It usually takes just a few seconds!

### 3. Launch Your App

**For Expo projects:**
- Show QR code in terminal
- Explain how to scan with Expo Go app on physical device
- Or press `i` for iOS simulator, `a` for Android emulator

**For React Native CLI projects:**

**iOS (macOS only):**
```bash
# Start iOS simulator
npx react-native run-ios

# OR specify a device
npx react-native run-ios --simulator="iPhone 15 Pro"

# OR using pnpm/npm scripts
pnpm ios
```

**Android:**
```bash
# Start Android emulator (make sure emulator is running first)
npx react-native run-android

# OR specify a device
npx react-native run-android --deviceId="device-id"

# OR using pnpm/npm scripts
pnpm android
```

**Wait for app to launch:**
- Watch for build progress
- Wait for app to appear on simulator/emulator
- Check for any errors in the terminal

---

## What to Tell the User

**When starting:**
- "Let me stop any Metro bundlers that might be running first, then I'll start yours up fresh!"
- "Checking if anything is already running..."

**When stopping Metro:**
- "Found a Metro bundler running, stopping it now..."
- "All clear! Ready to start fresh."

**When starting Metro:**
- "Starting your Metro bundler..."
- "Just a moment while it gets ready..."
- "Metro is ready! Now launching your app..."

**When launching iOS:**
- "Starting iOS simulator..."
- "Building your app for iOS..."
- "Your app should appear in the simulator soon!"

**When launching Android:**
- "Starting Android emulator..." (if needed)
- "Building your app for Android..."
- "Your app should appear in the emulator soon!"

**When app is ready:**
- "Perfect! Your app is running! 🎉"
- "You should see your app in the simulator/emulator now!"
- "The Metro bundler will keep running - you can stop it anytime with Ctrl+C"
- "Any changes you make will automatically reload in your app!"

**For Expo projects:**
- "I see you're using Expo! Here's your QR code - scan it with the Expo Go app on your phone!"
- "Or press 'i' for iOS simulator, 'a' for Android emulator"

**If something goes wrong:**
- Explain what happened in simple terms
- Help fix it right away
- Try again once it's fixed

---

## Important Notes

- **Port conflicts:** If port 8081 is busy, Metro will automatically try the next available port - we'll show you which one it uses!
- **Metro keeps running:** The Metro bundler runs in the foreground so you can see what's happening - press Ctrl+C when you want to stop it
- **Hot Reload:** Changes you make will automatically reload in your app - no need to restart!
- **Platform requirements:** iOS development requires macOS and Xcode. Android requires Android Studio.
- **Simulator/Emulator:** Make sure iOS Simulator or Android Emulator is installed and available
- **Physical devices:** For physical devices, make sure they're connected via USB and developer mode is enabled
- **Expo vs React Native CLI:** Expo projects use `expo start`, React Native CLI uses `react-native start` or `react-native run-ios/android`











