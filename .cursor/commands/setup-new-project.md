# Setup New Project

Get your brand new Next.js project ready to go! I'll check everything you need, install all the packages, set up your database connection, and make sure you're ready to start building. Just run this command and I'll handle all the technical setup automatically!

## What This Does

1. **Check your tools** - Make sure Node.js, Git, and Vercel CLI are installed (I'll help install them if needed!)
2. **Install all packages** - Get everything from your tech stack ready to use, including all the UI components
3. **Set up Supabase** - Connect your database and get your credentials configured
4. **Show you what's ready** - Give you a clear summary of everything that's set up

**Note:** This command gets everything ready, but doesn't start your server or customize your design system - we'll do those separately!

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

### 3. Check/Install Vercel CLI & Verify Connection

**Check if Vercel CLI is installed:**
- Run `vercel --version` to see if it's there
- If not installed: I'll install it with `npm install -g vercel` or `pnpm add -g vercel`
- If installed but outdated: I'll update it to the latest version

**Verify MCP connection to Vercel:**
- I'll check if I can connect to Vercel using `mcp_vercel_list_deployments`
- If successful: Great! Everything is connected and ready
- If connection fails: I'll let you know that the MCP Vercel connection needs to be configured

**Don't proceed until everything is ready:**
- I'll make sure Vercel CLI is installed and I can connect to it
- This lets us deploy your app later without any issues!

### 4. Install All Tech Stack Packages

I'll install all the packages you need for your project:

```bash
# Styling Utilities
pnpm add clsx tailwind-merge

# State Management
pnpm add zustand nuqs

# Forms & Validation
pnpm add react-hook-form zod @hookform/resolvers

# Animations
pnpm add framer-motion

# AI SDK
pnpm add ai @ai-sdk/react
npx ai-elements@latest

# Database
pnpm add @supabase/supabase-js @supabase/ssr

# Internationalization
pnpm add next-intl

# Email
pnpm add resend react-email @react-email/components

# Utilities
pnpm add date-fns

# Development Tools
pnpm add -D prettier eslint-config-prettier

# UI Components (shadcn/ui)
# First initialize shadcn/ui
pnpm dlx shadcn@latest init

# Then install all components
pnpm dlx shadcn@latest add --all --yes
```

**What happens:**
- The `shadcn@latest init` command sets up shadcn/ui configuration (creates `components.json`, updates CSS, etc.)
- The `add --all --yes` command installs all available components from the registry
- Components are added to `components/ui/` directory and all dependencies are automatically installed
- This gives you a complete set of beautiful, accessible UI components ready to use!

### 5. Set Up Supabase

**Install Supabase client via shadcn:**
```bash
pnpm dlx shadcn@latest add @supabase/supabase-client-nextjs
```

**Retrieve credentials via MCP:**
- I'll get your project URL using `mcp_supabase_get_project_url`
- I'll get your anon key using `mcp_supabase_get_publishable_keys`
- These are like your database's address and password - I'll handle them securely!

**Configure environment:**
- I'll create a `.env.local` file if it doesn't exist (this is where we store secrets)
- I'll add your Supabase credentials:
  ```
  SUPABASE_URL=<project_url_from_mcp>
  SUPABASE_ANON_KEY=<anon_key_from_mcp>
  ```
- This file stays on your computer and never gets shared - it's safe!

**Verify everything is set up:**
- I'll confirm `.env.local` was created/updated with the correct values
- Your database connection is now ready to use!

### 6. Summary

At the end, I'll give you a clear summary of everything that's ready:

```
✅ Setup Complete

What was installed:
- Node.js: [version]
- Git: [version]
- Vercel CLI: [version]
- State Management: Zustand, Nuqs
- Forms: React Hook Form, Zod
- Animations: Framer Motion
- AI SDK: Vercel AI SDK (ai, @ai-sdk/react, ai-elements)
- Database: Supabase client (@supabase/supabase-js, @supabase/ssr, @supabase/supabase-client-nextjs)
- i18n: next-intl
- Email: Resend, React Email
- Utilities: date-fns, clsx, tailwind-merge
- Development Tools: Prettier, ESLint config
- UI Components: All shadcn/ui components

Environment configured:
- `.env.local` created with Supabase credentials (SUPABASE_URL, SUPABASE_ANON_KEY)
```

---

## What to Tell the User

**When starting:**
- "Let me set up your new project! I'll check everything you need and install all the packages."
- "First, let me make sure you have all the tools installed..."
- "Checking Node.js, Git, and Vercel CLI..."

**When checking tools:**
- "Great! Node.js is installed ([version])"
- "I see pnpm isn't installed yet - let me install it for you!"
- "Git looks good! Let me check if it's configured..."
- "I need to set up your Git name and email - this helps save your work properly"

**When installing packages:**
- "Now I'll install all the packages you need - this might take a minute!"
- "Installing state management tools..."
- "Setting up forms and validation..."
- "Installing AI SDK and AI elements..."
- "Installing all the UI components - this gives you beautiful buttons, forms, and more!"
- "Almost done! Just setting up a few more things..."

**When setting up Supabase:**
- "Now let me connect your database..."
- "Getting your Supabase credentials..."
- "Setting up your environment file - this keeps your secrets safe!"
- "Perfect! Your database is connected and ready to use!"

**When done:**
- "All set! Your project is ready to go! 🎉"
- "Here's everything I set up for you:"
- **Show the summary clearly**
- "You're all ready to start building! Want me to help you add your first feature?"

**If something needs user help:**
- "I need your help with one thing..."
- "Could you install Node.js from nodejs.org? It's free and takes just a few minutes!"
- "I need to set up your Git name and email - what should I use?"
- "The MCP Vercel connection needs to be configured - here's how to fix it..."

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
- [ ] Checked Vercel CLI installation (`vercel --version`)
- [ ] Installed Vercel CLI if needed
- [ ] Verified MCP connection to Vercel (checked last deployment via `mcp_vercel_list_deployments`)
- [ ] Installed all tech stack packages (including shadcn/ui components)
- [ ] Installed Supabase client via shadcn
- [ ] Retrieved Supabase credentials via MCP
- [ ] Configured `.env.local` with Supabase credentials
- [ ] Provided summary of what was installed

---

## Important Notes

- **Prerequisites:** Node.js (LTS), pnpm, Git, and Vercel CLI must be installed before proceeding - but don't worry, I'll help you install them if needed!
- **Git Authentication:** Git needs to know who you are - I'll help you set this up if it's not already configured
- **MCP Vercel Connection:** I need to be able to connect to Vercel - if this isn't set up, I'll let you know how to fix it
- **Package Manager:** I'll use `pnpm` for everything (it's faster!) - I'll install it if you don't have it
- **No Server Start:** This command gets everything ready, but doesn't start your development server - you can do that separately!
- **No Customization:** This command doesn't customize your design system - we'll do that in another step!
- **Summary Required:** I'll always show you a clear summary at the end so you know exactly what's ready
- **Note:** This assumes you're already in a Next.js project directory - make sure you're in your project root when you run this!
