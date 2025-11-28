# Help / Recommend Command

**In plain English:** Not sure which command to use? Just describe what you want to do, and I'll recommend the best command(s) for your task.

## For Non-Technical Users (No Coding Experience Needed!)

**You don't need to know how to code!** These commands work in plain English. Just tell me what you want to build, and I'll handle all the technical details automatically.

### Simple Terms Glossary

When you see these words, here's what they mean in plain English:

- **Git** = Saves your work automatically (like auto-save in Google Docs)
- **GitHub** = Stores your project online so you can access it anywhere (like Google Drive for code)
- **App Store** = Apple's store where iOS apps are published (like the App Store on your iPhone)
- **Google Play Store** = Google's store where Android apps are published (like the Play Store on Android phones)
- **Metro** = The tool that builds your React Native app (like a compiler)
- **Simulator** = A virtual phone on your computer for testing iOS apps
- **Emulator** = A virtual phone on your computer for testing Android apps
- **Preview** = A test version you can share before going live (like a preview of an app)
- **Production** = Your live app that everyone can download (the final published version)
- **Branch** = A separate copy of your work for testing (like a draft document)
- **Code** = The instructions that make your app work (you don't need to write this - I do!)
- **Build** = Putting everything together so it works (like assembling furniture from instructions)
- **Deploy** = Publishing your app to the App Store or Play Store (like publishing your app)

### What You Need to Know:
- **You describe features in plain English** - Like "Add a login screen" or "Create a settings page"
- **I handle all the code** - I write, test, and fix everything automatically
- **You just confirm it looks good** - I'll show you a preview, and you tell me if it's right
- **I explain everything simply** - If something goes wrong, I'll tell you what happened in simple terms

### What You DON'T Need to Worry About:
- ❌ Writing code yourself
- ❌ Understanding Git, GitHub, or technical terms
- ❌ Setting up complex tools (I'll guide you through the basics)
- ❌ Fixing errors (I'll fix them automatically)
- ❌ Testing (I'll test everything automatically)
- ❌ Building for iOS/Android (I'll handle platform-specific details)

### Getting Started:
1. **First time?** Use `@setup-project` - I'll guide you through everything step-by-step
2. **Want to add something?** Use `@add-feature` - Just describe what you want
3. **Something broken?** Use `@fix-issues` - I'll find and fix it
4. **Ready to share?** Use `@preview-app` - Get a preview build
5. **Ready to go live?** Use `@go-live` - Publish to App Store and Play Store

**Remember:** If you're ever confused, just ask! I'll explain everything in simple terms.

## What This Command Does

This command analyzes your request and recommends the most appropriate command(s) from your command set. It helps you:
- Find the right command when you're not sure
- Discover commands you might not know about
- Understand which commands work together
- Get started quickly without memorizing all commands

**Examples of what you can say:**
- "I want to add a new feature"
- "How do I test my app?"
- "I need to fix a bug"
- "I want to understand my users better"
- "How do I publish to the App Store?"
- "I need to optimize performance"
- "I want to plan my app flow"

## How It Works

1. **You describe what you want to do**
   - Just tell me in plain English what you're trying to accomplish
   - Examples: "Add a feature", "Fix a bug", "Test my app", "Publish to App Store"

2. **I analyze your request**
   - I understand your intent and goals
   - I match it to relevant commands from your command set
   - I consider the context and complexity

3. **I recommend the best command(s)**
   - I suggest the most appropriate command(s) for your task
   - I explain why each command is recommended
   - I provide examples of how to use them
   - I suggest related commands that might help

4. **You use the recommended command**
   - Follow my recommendation
   - Or ask for alternatives if needed

## Usage Examples

**Simple requests:**
- `@help` → "I want to add a new feature"
  - **Recommended:** `@add-feature` → "Add a login screen"
  - **Why:** Automatically handles feature development end-to-end, including tests and documentation

- `@help` → "Something is broken"
  - **Recommended:** `@fix-issues` → "The button doesn't work"
  - **Why:** Intelligently diagnoses and fixes all types of issues automatically

**Complex requests:**
- `@help` → "I want to set up a new project"
  - **Recommended:** `@setup-project` → "Create my new React Native app"
  - **Why:** Handles complete project setup including dependencies, platform configuration, and design system

- `@help` → "I want to publish my app to the App Store"
  - **Recommended:** `@go-live` → "Go live"
  - **Why:** Runs all quality checks (security, accessibility, performance, tests) automatically before publishing

**Discovery requests:**
- `@help` → "What commands are available?"
  - **Recommended:** List all 13 core commands with brief descriptions
  - **Why:** Shows the complete workflow from setup to production

**Planning requests:**
- `@help` → "I want to plan my app flow"
  - **Recommended:** `@plan-app-flow` → "Generate user flow for my mobile app"
  - **Why:** Generates comprehensive user flows with system setup, user interactions, and acceptance criteria

## Command Recommendation Logic

### Core Commands (Essential Workflow)

I prioritize **13 core commands** that cover everything you need:

1. **`@setup-project`** - When you need to:
   - Set up a brand new React Native project from scratch
   - Configure iOS and Android development environments
   - Install all necessary packages and dependencies

2. **`@add-feature`** - When you need to:
   - Add new features (screens, components, navigation)
   - Build complete features end-to-end
   - Automatically test and document

3. **`@remove-feature`** - When you need to:
   - Remove existing features safely
   - Clean up related code and references

4. **`@update-feature`** - When you need to:
   - Modify existing features
   - Update functionality or behavior

5. **`@customize-app`** - When you need to:
   - Customize colors, fonts, and styles
   - Make your app look exactly how you want

6. **`@preview-app`** - When you need to:
   - Create a preview build to share
   - Test features before going live

7. **`@go-live`** - When you need to:
   - Publish to App Store and Google Play Store
   - Run all quality checks automatically

8. **`@fix-issues`** - When you need to:
   - Fix bugs, errors, and issues
   - Resolve Git problems
   - Clean up code quality
   - Fix Metro bundler or platform-specific issues

9. **`@start-app`** - When you need to:
   - Start your Metro bundler
   - Launch your app on simulator/emulator or device

10. **`@test-app`** - When you need to:
    - Automatically test the last feature you worked on
    - Test the complete app
    - Get comprehensive feedback on what works and what doesn't

11. **`@plan-app-flow`** - When you need to:
    - Generate comprehensive user flows for your mobile app
    - Map out system setup and user interactions
    - Create product documentation with acceptance criteria

12. **`@sync-configuration`** - When you need to:
    - Sync Cursor configuration from a repository
    - Update commands, rules, and reviews

13. **`@help`** - When you need to:
    - Find the right command
    - Understand what each command does

## What to Tell the User

**First time users:**
- "Hi! I can help you find the right command. Just describe what you want to do in plain English. For example: 'I want to add a feature' or 'How do I test my app?'"

**When analyzing:**
- "Let me analyze your request and find the best command(s) for you..."
- "Based on what you described, here are my recommendations..."

**When recommending:**
- "**Recommended:** `@command-name` → 'Your specific request'"
- "**Why:** [Clear explanation of why this command fits]"
- "**Alternative:** If you prefer direct access, you can use `@role/specific-command`"
- "**Related commands:** You might also want to use [related commands]"

**For complex tasks:**
- "For this task, I recommend a sequence:"
  1. "First, use `@command1` to [purpose]"
  2. "Then, use `@command2` to [purpose]"
  3. "Finally, use `@command3` to [purpose]"

**When multiple options exist:**
- "I found several options. Here's the best one for your situation:"
- "**Best for beginners:** `@simple-command`"
- "**Best for power users:** `@advanced-command`"
- "**Best for this specific case:** `@specific-command`"

## Command Matching Patterns

I match requests to commands based on:

**Intent keywords:**
- "add", "create", "build", "implement" → `@add-feature`
- "fix", "broken", "error", "bug" → `@fix-issues`
- "test", "check", "verify" → `@test-app`
- "deploy", "publish", "release", "go live", "app store", "play store" → `@go-live` or `@preview-app`
- "setup", "configure", "initialize", "new project" → `@setup-project`
- "delete", "remove" → `@remove-feature`
- "update", "modify", "change" → `@update-feature`
- "design", "colors", "fonts", "styles" → `@customize-app`
- "plan", "flow", "user flow", "product flow", "user story" → `@plan-app-flow`
- "start", "run", "launch", "simulator", "emulator" → `@start-app`

**Workflow keywords:**
- "start", "begin", "new" → `@setup-project`
- "feature", "add", "build" → `@add-feature`
- "preview", "share", "test" → `@preview-app`
- "production", "live", "deploy", "app store" → `@go-live`
- "broken", "error", "fix" → `@fix-issues`
- "plan", "flow", "user flow", "product flow" → `@plan-app-flow`

**Complexity indicators:**
- Simple requests → Core commands (`@add-feature`, `@fix-issues`, etc.)
- Multi-step tasks → Sequence of commands (e.g., setup-project → add-feature → preview-app → go-live)

## See Also

- **[Build Feature](add-feature.md)**: Build features
- **[Remove Feature](remove-feature.md)**: Remove features
- **[Update Feature](update-feature.md)**: Update features
- **[Fix Issues](fix-issues.md)**: Fix problems
- **[Test App](test-app.md)**: Automated testing
- **[Go Live](go-live.md)**: Publish to App Store and Play Store
- **[Preview App](preview-app.md)**: Create preview build
- **[Start App](start-app.md)**: Start Metro bundler and launch app
- **[Setup Project](setup-project.md)**: Set up React Native projects
- **[Plan App Flow](plan-app-flow.md)**: Generate user flows
- **[Customize App](customize-app.md)**: Customize appearance
- **[Sync Configuration](sync-configuration.md)**: Sync Cursor config












