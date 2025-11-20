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
1. **First time?** Use `@setup-new-project` - I'll guide you through everything step-by-step
2. **Want to add something?** Use `@add-feature` - Just describe what you want
3. **Something broken?** Use `@fix-everything` - I'll find and fix it
4. **Ready to share?** Use `@publish-feature` - Get a preview URL
5. **Ready to go live?** Use `@publish-production` - Make your site public

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
  - **Recommended:** `@add-feature` → "Add a contact form"
  - **Why:** Automatically handles feature development end-to-end, including tests and documentation

- `@help` → "Something is broken"
  - **Recommended:** `@fix-everything` → "The button doesn't work"
  - **Why:** Intelligently diagnoses and fixes all types of issues automatically

**Complex requests:**
- `@help` → "I want to set up a new project"
  - **Recommended:** `@setup-new-project` → "Create my new app"
  - **Why:** Handles complete project setup including Supabase, GitHub, Vercel, and design system customization

- `@help` → "I want to deploy my app to production"
  - **Recommended:** `@publish-production` → "Go live"
  - **Why:** Runs all quality checks (security, accessibility, performance, tests) automatically before deploying

**Discovery requests:**
- `@help` → "What commands are available?"
  - **Recommended:** List all 10 core commands with brief descriptions
  - **Why:** Shows the complete workflow from setup to production

**Planning requests:**
- `@help` → "I want to plan my product flow"
  - **Recommended:** `@plan-product` → "Generate user flow for my platform"
  - **Why:** Generates comprehensive user flows with system setup, user interactions, and acceptance criteria

## Command Recommendation Logic

### Core Commands (Essential Workflow)

I prioritize **10 core commands** that cover everything you need:

1. **`@setup-new-project`** - When you need to:
   - Set up a brand new project from scratch
   - Configure Supabase database and authentication
   - Connect to GitHub and Vercel
   - Customize your design system

2. **`@add-feature`** - When you need to:
   - Add new features (including login/auth flows)
   - Build complete features end-to-end
   - Automatically test and document

3. **`@delete-feature`** - When you need to:
   - Remove existing features safely
   - Clean up related code and references

4. **`@customize-design-system`** - When you need to:
   - Customize colors, fonts, and styles
   - Make your app look exactly how you want

5. **`@publish-feature`** - When you need to:
   - Create a preview URL to share
   - Test features before going live

6. **`@publish-production`** - When you need to:
   - Deploy to production and go live
   - Run all quality checks automatically

7. **`@fix-everything`** - When you need to:
   - Fix bugs, errors, and issues
   - Resolve Git problems
   - Clean up code quality
   - Remove AI-generated slop

8. **`@run-tests`** - When you need to:
   - Run tests explicitly
   - Verify everything works

9. **`@test-automated`** - When you need to:
   - Automatically test the last feature you worked on
   - Test the complete user journey
   - Get comprehensive feedback on what works and what doesn't
   - Catch bugs before they reach production

10. **`@plan-product`** - When you need to:
   - Generate comprehensive user flows for your platform
   - Map out system setup and user interactions
   - Create product documentation with acceptance criteria
   - Plan product features before building

11. **`@help`** - When you need to:
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
- "add", "create", "build", "implement" → `@add-feature`
- "fix", "broken", "error", "bug" → `@fix-everything`
- "test", "check", "verify" → `@run-tests` or `@test-automated`
- "automated test", "playwright", "e2e", "end-to-end", "test journey" → `@test-automated`
- "deploy", "publish", "release", "go live" → `@publish-production` or `@publish-feature`
- "setup", "configure", "initialize", "new project" → `@setup-new-project`
- "delete", "remove" → `@delete-feature`
- "design", "colors", "fonts", "styles" → `@customize-design-system`
- "plan", "flow", "user flow", "product flow", "user story" → `@plan-product`

**Workflow keywords:**
- "start", "begin", "new" → `@setup-new-project`
- "feature", "add", "build" → `@add-feature`
- "preview", "share", "test" → `@publish-feature`
- "production", "live", "deploy" → `@publish-production`
- "broken", "error", "fix" → `@fix-everything`
- "plan", "flow", "user flow", "product flow" → `@plan-product`

**Complexity indicators:**
- Simple requests → Core commands (`@add-feature`, `@fix-everything`, etc.)
- Multi-step tasks → Sequence of commands (e.g., setup → add-feature → publish-feature → publish-production)

## See Also

- **[Add Feature](add-feature.md)**: Build features
- **[Fix Everything](fix-everything.md)**: Fix problems
- **[Run Tests](run-tests.md)**: Test and quality
- **[Automated Testing](test-automated.md)**: Automated testing with Playwright
- **[Publish Production](publish-production.md)**: Deploy to production
- **[Publish Feature](publish-feature.md)**: Deploy preview
- **[Setup New Project](setup-new-project.md)**: Set up projects
- **[Plan Product](plan-product.md)**: Generate user flows

