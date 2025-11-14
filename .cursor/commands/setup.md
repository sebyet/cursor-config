# Setup

**In plain English:** Need to set up a project? I'll help you get everything ready - whether it's a new project or an existing one.

## What This Command Does

**For non-technical users:** This helps you set up projects so you can start building. I'll:
- Set up a brand new project from scratch (if starting fresh)
- Set up an existing project (if you already have code)
- Customize your design system (colors, fonts, styles)
- Check what's missing and install it
- Connect everything together (GitHub, Vercel, etc.)

**Examples of what you can say:**
- "Set up a new project called 'my-app'"
- "Set up this existing project"
- "Customize the design system"
- "Check what's missing and set it up"
- "Install dependencies and configure everything"

## How It Works

1. **Ask what you need**
   - "New project" → Routes to `engineer/setup-new-project.md`, then customizes design system
   - "Existing project" → Checks and sets up what's missing
   - "Customize design" → Routes to `design/customize-design-system.md`
   - "Check what's needed" → Diagnoses what needs setup

2. **Set up automatically**
   - I check what's already done
   - I install what's missing
   - I configure everything needed
   - **I customize your design system** (colors, fonts, styles) - happens automatically for new projects
   - I connect services (GitHub, Vercel, etc.)

3. **Verify everything works**
   - I test that everything is set up correctly
   - I tell you what was done
   - I give you next steps

## Usage Examples

**New project:**
- `@setup` → "Set up a new project called 'my-app'"
- `@setup` → "Create a new project"

**Existing project:**
- `@setup` → "Set up this existing project"
- `@setup` → "Check what's missing and install it"
- `@setup` → "Install dependencies and configure everything"

**Check what's needed:**
- `@setup` → "What do I need to set up?"
- `@setup` → "Check if everything is configured"

## What to Tell the User

**First time users:**
- "Hi! I can help you set up projects. Are you:
  - **Starting a new project** - I'll create everything from scratch
  - **Setting up an existing project** - I'll check what's missing and install it
  - **Not sure** - I'll check what you have and guide you
  
  What would you like to do?"

**For new projects:**
- "I'll set up a brand new project for you. This will:
  - Create a new Next.js project with shadcn/ui
  - Install all components and dependencies
  - Set up Supabase
  - **Customize your design system** (colors, fonts, styles) - I'll guide you through this
  - Connect to GitHub and Vercel
  - Configure automatic deployments
  
  What would you like to name your project?"

**After project setup (for new projects):**
- "Great! Your project is set up. Now let me customize your design system - I'll ask you a few questions about colors and styles to make it look great!"
- Automatically route to `design/customize-design-system.md` after project setup

**For existing projects:**
- "Let me check what's already set up and what's missing..."
- "I found: [list what's set up]"
- "I need to set up: [list what's missing]"
- "Setting up [missing item]..."
- "Everything is set up! You're ready to start building."

**If prerequisites missing:**
- "Before we start, I need to check a few things..."
- "I found that [tool] is not installed. Let me help you install it..."
- "Once everything is installed, we can continue with the setup."

## Specialist Commands Used

- **[Setup New Project](engineer/setup-new-project.md)** - Set up a brand new project from scratch
- **[Customize Design System](design/customize-design-system.md)** - Customize colors, fonts, and styles (runs automatically for new projects)
- **[Build](build.md)**: Build features after setup
- **[Deploy](deploy.md)**: Deploy after setup

## See Also

- **[How to Start](how-to-start.md)**: Learn how to use the commands
- **[Build](build.md)**: Build features after setup
- **[Deploy](deploy.md)**: Deploy your project
- **[Fix](fix.md)**: Fix setup issues

