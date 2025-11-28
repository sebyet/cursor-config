# Help / Recommend Command

**In plain English:** Not sure which command to use? Just describe what you want to do, and I'll recommend the best command(s) for your task.

## For Non-Technical Users (No Coding Experience Needed!)

**You don't need to know how to code!** These commands work in plain English. Just tell me what you want to build, and I'll handle all the technical details automatically.

### Simple Terms Glossary

When you see these words, here's what they mean in plain English:

- **Git** = Saves your work automatically (like auto-save in Google Docs)
- **GitHub** = Stores your project online so you can access it anywhere (like Google Drive for code)
- **Vercel** = Makes your website live on the internet (like publishing a blog post)
- **Supabase** = Stores your data and handles user accounts (like a database)
- **Preview** = A draft version you can share before going live (like a preview of a blog post)
- **Production** = Your live website that everyone can see (the final published version)
- **Branch** = A separate copy of your work for testing (like a draft document)
- **Code** = The instructions that make your website work (you don't need to write this - I do!)
- **Build** = Putting everything together so it works (like assembling furniture from instructions)
- **Deploy** = Making your website live on the internet (like publishing your blog)

### What You Need to Know:
- **You describe features in plain English** - Like "Add a contact form" or "Create a login page"
- **I handle all the code** - I write, test, and fix everything automatically
- **You just confirm it looks good** - I'll show you a preview, and you tell me if it's right
- **I explain everything simply** - If something goes wrong, I'll tell you what happened in simple terms

### What You DON'T Need to Worry About:
- ❌ Writing code yourself
- ❌ Understanding Git, GitHub, or technical terms
- ❌ Setting up complex tools (I'll guide you through the basics)
- ❌ Fixing errors (I'll fix them automatically)
- ❌ Testing (I'll test everything automatically)

### Getting Started:
1. **First time?** Use `@setup-project` - I'll guide you through everything step-by-step
2. **Want to add something?** Use `@build-feature` - Just describe what you want
3. **Something broken?** Use `@fix-issues` - I'll find and fix it
4. **Need to undo changes?** Use `@reset-to-last-version` - I'll restore your last commit
5. **Ready to share?** Use `@preview-app` - Get a preview URL
6. **Ready to go live?** Use `@go-live` - Make your site public

**Remember:** If you're ever confused, just ask! I'll explain everything in simple terms.

## What This Command Does

This command analyzes your request and recommends the most appropriate command(s) from your command set. It helps you:
- Find the right command when you're not sure
- Discover commands you might not know about
- Understand which commands work together
- Get started quickly without memorizing all commands

**Examples of what you can say:**
- "I want to add a new feature"
- "How do I test my code?"
- "I need to fix a bug"
- "I want to understand my users better"
- "How do I deploy to production?"
- "I need to optimize performance"
- "I want to plan my product flow"

## How It Works

1. **You describe what you want to do**
   - Just tell me in plain English what you're trying to accomplish
   - Examples: "Add a feature", "Fix a bug", "Test my app", "Deploy to production"

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
  - **Recommended:** `@build-feature` → "Add a contact form"
  - **Why:** Automatically handles feature development end-to-end, including tests and documentation

- `@help` → "Something is broken"
  - **Recommended:** `@fix-issues` → "The button doesn't work"
  - **Why:** Intelligently diagnoses and fixes all types of issues automatically

**Complex requests:**
- `@help` → "I want to set up a new project"
  - **Recommended:** `@setup-project` → "Create my new app"
  - **Why:** Handles complete project setup including Supabase, GitHub, Vercel, and design system customization

- `@help` → "I want to deploy my app to production"
  - **Recommended:** `@go-live` → "Go live"
  - **Why:** Runs all quality checks (security, accessibility, performance, tests) automatically before deploying

**Discovery requests:**
- `@help` → "What commands are available?"
  - **Recommended:** List all 15 core commands with brief descriptions
  - **Why:** Shows the complete workflow from setup to production

**Planning requests:**
- `@help` → "I want to plan my product flow"
  - **Recommended:** `@plan-app-flow` → "Generate user flow for my platform"
  - **Why:** Generates comprehensive user flows with system setup, user interactions, and acceptance criteria

## Command Recommendation Logic

### Core Commands (Essential Workflow)

I prioritize **15 core commands** that cover everything you need:

1. **`@setup-project`** - When you need to:
   - Set up a brand new project from scratch
   - Configure Supabase database and authentication
   - Connect to GitHub and Vercel
   - Customize your design system

2. **`@build-feature`** - When you need to:
   - Add new features (including login/auth flows)
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
   - Create a preview URL to share
   - Test features before going live

7. **`@go-live`** - When you need to:
   - Deploy to production and go live
   - Run all quality checks automatically

8. **`@fix-issues`** - When you need to:
   - Fix bugs, errors, and issues
   - Resolve Git problems
   - Clean up code quality
   - Remove AI-generated slop

9. **`@reset-to-last-version`** - When you need to:
   - Discard all uncommitted changes safely
   - Restore your working tree to the last commit
   - Undo experiments or messy states instantly

10. **`@start-app`** - When you need to:
   - Start your development server
   - View your app locally

11. **`@test-app`** - When you need to:
   - Automatically test the last feature you worked on
   - Test the complete user journey
   - Get comprehensive feedback on what works and what doesn't
   - Catch bugs before they reach production

12. **`@plan-app-flow`** - When you need to:
   - Generate comprehensive user flows for your platform
   - Map out system setup and user interactions
   - Create product documentation with acceptance criteria
   - Plan product features before building

13. **`@sync-configuration`** - When you need to:
   - Sync Cursor configuration from a repository
   - Update commands, rules, and reviews

14. **`@update-cursor-config`** - When you need to:
   - Update your `.cursor` folder with the latest version from the reference repository
   - Get the latest Cursor commands and rules
   - Sync with the latest best practices and configurations

15. **`@help`** - When you need to:
   - Find the right command
   - Understand what each command does

## What to Tell the User

**First time users:**
- "Hi! I can help you find the right command. Just describe what you want to do in plain English. For example: 'I want to add a feature' or 'How do I test my code?'"

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
- "add", "create", "build", "implement" → `@build-feature`
- "fix", "broken", "error", "bug" → `@fix-issues`
- "test", "check", "verify" → `@test-app`
- "automated test", "playwright", "e2e", "end-to-end", "test journey" → `@test-app`
- "deploy", "publish", "release", "go live" → `@go-live` or `@preview-app`
- "setup", "configure", "initialize", "new project" → `@setup-project`
- "delete", "remove" → `@remove-feature`
- "update", "modify", "change" → `@update-feature`
- "reset", "undo", "discard changes" → `@reset-to-last-version`
- "design", "colors", "fonts", "styles" → `@customize-app`
- "plan", "flow", "user flow", "product flow", "user story" → `@plan-app-flow`
- "start", "run", "launch" → `@start-app`
- "update cursor config", "sync cursor", "update .cursor", "get latest cursor config" → `@update-cursor-config`

**Workflow keywords:**
- "start", "begin", "new" → `@setup-project`
- "feature", "add", "build" → `@build-feature`
- "preview", "share", "test" → `@preview-app`
- "production", "live", "deploy" → `@go-live`
- "broken", "error", "fix" → `@fix-issues`
- "reset", "undo", "clean up workspace" → `@reset-to-last-version`
- "plan", "flow", "user flow", "product flow" → `@plan-app-flow`

**Complexity indicators:**
- Simple requests → Core commands (`@build-feature`, `@fix-issues`, etc.)
- Multi-step tasks → Sequence of commands (e.g., setup-project → build-feature → preview-app → go-live)

## See Also

- **[Build Feature](build-feature.md)**: Build features
- **[Remove Feature](remove-feature.md)**: Remove features
- **[Update Feature](update-feature.md)**: Update features
- **[Fix Issues](fix-issues.md)**: Fix problems
- **[Reset to Last Version](reset-to-last-version.md)**: Discard uncommitted changes
- **[Test App](test-app.md)**: Automated testing with Playwright
- **[Go Live](go-live.md)**: Deploy to production
- **[Preview App](preview-app.md)**: Create preview link
- **[Start App](start-app.md)**: Start development server
- **[Setup Project](setup-project.md)**: Set up projects
- **[Plan App Flow](plan-app-flow.md)**: Generate user flows
- **[Customize App](customize-app.md)**: Customize appearance
- **[Sync Configuration](sync-configuration.md)**: Sync Cursor config
- **[Update Cursor Config](update-cursor-config.md)**: Update `.cursor` folder from repository

