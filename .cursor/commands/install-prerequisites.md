# Install Prerequisites

**For non-developers:** This guide will walk you through everything you need to set up before starting your project. Follow these steps in order - they're organized to make everything work smoothly!

## Overview: What You'll Do

1. **Create accounts** (GitHub, Vercel, Supabase) - You can use Google login!
2. **Install software** (Node.js, pnpm, Git, Cursor)
3. **Create projects** (Vercel project linked to GitHub, Supabase project)
4. **Clone repository** (Get your code on your computer)
5. **Configure Cursor layout and settings** (Set up the interface for easy use)
6. **Setup .Cursor** (Sync config from https://github.com/sebyet/cursor-config)
7. **Configure MCPs** (Add your credentials to connect Vercel & Supabase - MCPs are already included!)
8. **Run setup** (Install packages and dependencies with `@setup-project`)

---

## Part 1: Create Accounts

You'll need accounts on three services. **Good news:** All of them support Google login, so you can sign in with your Google account if you prefer!

### 1. Create GitHub Account

1. Go to [github.com](https://github.com) in your web browser
2. Click **"Sign up"** in the top right
3. Choose one of these options:
   - **Option A:** Sign up with email (create username, enter email, set password)
   - **Option B:** Click **"Continue with Google"** to use your Google account
4. Complete the verification steps (check your email if needed)
5. **Verify it worked:** You should see your GitHub dashboard

### 2. Create Vercel Account

1. Go to [vercel.com](https://vercel.com) in your web browser
2. Click **"Sign Up"** in the top right
3. Choose one of these options:
   - **Option A:** Sign up with email
   - **Option B:** Click **"Continue with Google"** to use your Google account
   - **Option C:** Click **"Continue with GitHub"** to use your GitHub account
4. Complete the setup steps
5. **Verify it worked:** You should see your Vercel dashboard

### 3. Create Supabase Account

1. Go to [supabase.com](https://supabase.com) in your web browser
2. Click **"Start your project"** or **"Sign in"**
3. Choose one of these options:
   - **Option A:** Sign up with email
   - **Option B:** Click **"Continue with Google"** to use your Google account
   - **Option C:** Click **"Continue with GitHub"** to use your GitHub account
4. Complete the setup steps
5. **Verify it worked:** You should see your Supabase dashboard

**✅ Checkpoint:** You now have accounts on GitHub, Vercel, and Supabase!

---

## Part 2: Install Software

### For Windows Users

#### 1. Install Node.js

1. Go to [nodejs.org](https://nodejs.org/) in your web browser
2. Click the big green **"LTS"** button (Long Term Support - the most stable version)
3. The file will download automatically (`node-v20.x.x-x64.msi`)
4. Find it in your Downloads folder and double-click it
5. Click **"Next"** through all steps (keep default options)
6. Click **"Install"** (you may need to allow changes)
7. Click **"Finish"**
8. **Verify:** In Cursor, open the terminal (`` Ctrl + ` ``), then type `node --version` - you should see a version number!

#### 2. Install pnpm

**What is pnpm?** It's a package manager (like npm, but faster). We'll use it to install all your project packages.

1. In Cursor, open the terminal (`` Ctrl + ` ``)
2. Run this command:
   ```bash
   npm install -g pnpm
   ```
3. Wait for it to finish installing
4. **Verify:** Type `pnpm --version` - you should see a version number!

#### 3. Install Git

1. Go to [git-scm.com/download/win](https://git-scm.com/download/win)
2. The download should start automatically (`Git-2.x.x-64-bit.exe`)
3. Find it in Downloads and double-click it
4. Click **"Next"** through all steps
5. **Important:** Keep **"Git from the command line and also from 3rd-party software"** checked
6. Click **"Install"** and wait
7. Click **"Finish"**
8. **Verify:** In Cursor, open the terminal (`` Ctrl + ` ``), then type `git --version` - you should see a version number!

#### 4. Install Cursor

1. Go to [cursor.sh](https://cursor.sh/) in your web browser
2. Click **"Download for Windows"**
3. Find the downloaded file (`Cursor-Setup.exe`) and double-click it
4. Click **"Next"** through the setup
5. Click **"Install"** and wait
6. Click **"Finish"**
7. **First time:** Cursor will open - sign in or create an account

---

### For macOS Users

#### 1. Install Node.js

1. Go to [nodejs.org](https://nodejs.org/) in your web browser
2. Click the big green **"LTS"** button
3. The file will download (`node-v20.x.x.pkg`)
4. Find it in Downloads and double-click it
5. Click **"Continue"** through all steps (keep default options)
6. Click **"Install"** (enter your Mac password)
7. Click **"Close"**
8. **Verify:** In Cursor, open the terminal (`` Command + ` ``), then type `node --version` - you should see a version number!

#### 2. Install pnpm

**What is pnpm?** It's a package manager (like npm, but faster). We'll use it to install all your project packages.

1. In Cursor, open the terminal (`` Command + ` ``)
2. Run this command:
   ```bash
   npm install -g pnpm
   ```
3. Wait for it to finish installing
4. **Verify:** Type `pnpm --version` - you should see a version number!

#### 3. Install Homebrew

**What is Homebrew?** It's a package manager for macOS that makes installing software easier. We'll use it to install Git.

1. In Cursor, open the terminal (`` Command + ` ``)
2. Run this command (it will ask for your Mac password):
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```
3. Follow the prompts:
   - It will ask for your Mac password (you won't see the characters as you type - that's normal!)
   - Press Enter after typing your password
   - It will show you what it's installing - this is normal
   - Wait for it to finish (this might take a few minutes)
4. **If you see a message about adding Homebrew to PATH:**
   - It will show you commands to run (something like `echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile`)
   - Copy and paste those commands into Cursor's terminal and press Enter
   - Or restart Cursor
5. **Verify:** In Cursor's terminal, type `brew --version` - you should see a version number!

#### 4. Install Git

Now we'll use Homebrew to install Git:

1. In Cursor, open the terminal (`` Command + ` ``)
2. Run this command:
   ```bash
   brew install git
   ```
3. Wait for it to finish installing (this might take a minute)
4. **Verify:** Type `git --version` - you should see a version number like `git version 2.x.x`!

#### 5. Install Cursor

1. Go to [cursor.sh](https://cursor.sh/) in your web browser
2. Click **"Download for macOS"**
3. The file will download (`Cursor.dmg`)
4. Find it in Downloads and double-click it
5. Drag the **Cursor** icon to your **Applications** folder
6. Open Applications and double-click **Cursor**
7. **First time:** If you see a security warning, go to System Settings → Privacy & Security → click **"Open Anyway"**
8. Sign in or create an account when prompted

**✅ Checkpoint:** You now have Node.js, pnpm, Homebrew, Git, and Cursor installed!

---

## Part 3: Create Projects

### 1. Create Vercel Project (This Creates GitHub Repository Automatically)

**The easiest way:** Vercel can create a new GitHub repository for you automatically! This is simpler than creating them separately.

1. Go to [vercel.com](https://vercel.com) and sign in
2. Click **"Add New..."** → **"Project"**
3. You'll see options to import or create a repository:
   - If you see **"Create Git Repository"** or **"Create a new repository"**, click that
   - If you see **"Import Git Repository"**, look for a **"Create Git Repository"** button or link
4. **Authorize Vercel to access GitHub** (if prompted):
   - Click **"Continue with GitHub"** or **"Authorize"**
   - You may need to sign in to GitHub and approve Vercel's access
5. **Create your repository:**
   - Repository name: Give it a name (e.g., "my-app")
   - Choose **"Public"** or **"Private"** (your choice)
   - Framework Preset: Select **"Next.js"** (or it may auto-detect)
   - Root Directory: Leave as **"."** (default)
   - Build Command: Leave default (or empty)
   - Output Directory: Leave default (or empty)
6. Click **"Create"** or **"Deploy"**
7. **What happens:**
   - Vercel creates a new GitHub repository for you automatically
   - It connects the repository to your Vercel project
   - It starts deploying your project
8. Wait for deployment to finish (this might take a minute)
9. **Save your repository URL:**
   - After deployment, you'll see your project
   - Click on the project settings or repository link
   - **Copy the GitHub repository URL** - you'll need this to clone it! (It looks like `https://github.com/yourusername/my-app.git`)
10. **Copy your Vercel project URL** - you'll see it when deployment completes!

**✅ Checkpoint:** Your GitHub repository is created automatically and connected to Vercel!

### 3. Create Supabase Project

1. Go to [supabase.com](https://supabase.com) and sign in
2. Click **"New Project"** (or **"Create a new project"**)
3. **Fill in the details:**
   - Name: Give your project a name (e.g., "my-app-db")
   - Database Password: Create a strong password (save this somewhere safe!)
   - Region: Choose the closest region to you
4. Click **"Create new project"**
5. Wait for the project to be created (this takes 1-2 minutes)
6. **Save your project details:**
   - You'll see your project URL and keys
   - Don't worry about copying them now - we'll get them later via MCP

**✅ Checkpoint:** You now have a Supabase project ready!

---

## Part 4: Clone Repository and Open in Cursor

### Option A: Using GitHub Desktop (Easier for non-developers)

1. Go to [desktop.github.com](https://desktop.github.com/) and download GitHub Desktop
2. Install it and sign in with your GitHub account
3. In GitHub Desktop, click **"File"** → **"Clone Repository"**
4. Find your repository in the list, or paste the repository URL
5. Choose where to save it (like your Documents folder)
6. Click **"Clone"**
7. In GitHub Desktop, right-click on your repository
8. Select **"Open in Cursor"** (or **"Open in External Editor"** → choose Cursor)

### Option B: Using Cursor Directly

1. Open **Cursor**
2. Click **"File"** → **"Clone Repository"** (or use `Command/Ctrl + Shift + P` and type "Clone")
3. Paste your GitHub repository URL
4. Choose where to save it
5. Click **"Clone"**
6. Cursor will ask if you want to open it - click **"Open"**

**Note:** If cloning doesn't work in Cursor, use GitHub Desktop (Option A) - it's more reliable for non-developers.

**✅ Checkpoint:** Your repository is cloned and open in Cursor!

---

## Part 5: Configure Cursor Layout and Settings

**Why this matters:** Setting up Cursor's layout and settings makes it much easier to use, especially if you're new to coding. We'll organize everything so you can find what you need quickly!

### 1. Understanding the Cursor Interface

When you first open Cursor, you'll see several areas:

- **Left Sidebar:** File explorer (shows your project files)
- **Main Editor:** Where you'll edit code
- **Right Sidebar:** Chat/command panel (where you'll talk to AI)
- **Bottom Panel:** Terminal (where commands run)
- **Top Menu:** Settings and options

### 2. Open Settings

1. Open the Command Palette:
   - **macOS:** `Command + Shift + P`
   - **Windows:** `Ctrl + Shift + P`
2. Type **"Preferences: Open Settings"** and select it
   - Or go to **"Cursor"** → **"Settings"** (macOS) or **"File"** → **"Preferences"** → **"Settings"** (Windows)

### 3. Essential Settings for Non-Developers

Here are the most important settings to configure:

#### A. Enable Word Wrap (Makes Long Lines Easier to Read)

1. In Settings, search for **"word wrap"**
2. Find **"Editor: Word Wrap"**
3. Set it to **"on"** (this makes long lines of code wrap to the next line instead of scrolling)

#### B. Show Line Numbers (Helps You Find Things)

1. In Settings, search for **"line numbers"**
2. Find **"Editor: Line Numbers"**
3. Set it to **"on"** (this shows numbers on the left side of code)

#### C. Enable Minimap (Shows Overview of Your File)

1. In Settings, search for **"minimap"**
2. Find **"Editor: Minimap Enabled"**
3. Make sure it's **checked** (this shows a small preview of your file on the right)

#### D. Set Font Size (Make Text Easier to Read)

1. In Settings, search for **"font size"**
2. Find **"Editor: Font Size"**
3. Set it to **14** or **16** (or whatever is comfortable for you)

#### E. Enable Auto Save (Saves Your Work Automatically)

1. In Settings, search for **"auto save"**
2. Find **"Files: Auto Save"**
3. Set it to **"afterDelay"** (saves automatically after you stop typing)
4. Set **"Files: Auto Save Delay"** to **1000** (saves after 1 second of inactivity)

### 4. Configure Layout and Panels

**Important:** All commands and verifications should be run in Cursor's built-in terminal, not in external terminals. This keeps everything in one place and makes it easier to work!

#### A. Open Cursor's Terminal

**To open the terminal (bottom panel):**
- **macOS:** `` Command + ` ``
- **Windows:** `` Ctrl + ` ``

**Tip:** The terminal opens at the bottom of Cursor. You'll use this for all commands - installing packages, running setup, and verifying installations.

#### B. Show/Hide Panels

**To toggle the terminal (bottom panel):**
- **macOS:** `` Command + ` ``
- **Windows:** `` Ctrl + ` ``

**To toggle the file explorer (left sidebar):**
- **macOS:** `Command + B`
- **Windows:** `Ctrl + B`

**To toggle the chat/command panel (right sidebar):**
- Click the chat icon in the top right, or use `Command/Ctrl + L` to open chat

#### C. Recommended Layout for Beginners

1. **Keep the file explorer open** (left sidebar) - you'll need to see your files
2. **Keep the terminal at the bottom** - you'll use it to run ALL commands (don't use external terminals!)
3. **Open the chat panel when needed** - use `Command/Ctrl + L` to open it
4. **Use split view for comparing files:**
   - Right-click a file → **"Open to the Side"** to see two files side-by-side

**Remember:** Always use Cursor's terminal (`` Command/Ctrl + ` ``) for running commands. This is where you'll verify installations, install packages, and run setup commands!

### 5. Configure Editor Appearance

#### A. Choose a Theme (Make It Easy on Your Eyes)

1. Open Command Palette (`Command/Ctrl + Shift + P`)
2. Type **"Preferences: Color Theme"**
3. Try these themes (pick what you like!):
   - **Light themes:** "Light+", "Quiet Light"
   - **Dark themes:** "Dark+", "Monokai", "One Dark Pro"
4. Click on a theme to apply it

#### B. Configure Tab Size (How Much Space Indentation Uses)

1. In Settings, search for **"tab size"**
2. Find **"Editor: Tab Size"**
3. Set it to **2** (this is standard for most projects)

### 6. Enable Helpful Features

#### A. Enable Bracket Pair Colorization (Makes Matching Brackets Easier to See)

1. In Settings, search for **"bracket pair"**
2. Find **"Editor: Bracket Pair Colorization Enabled"**
3. Make sure it's **checked**

#### B. Enable Format on Save (Automatically Fixes Code Formatting)

1. In Settings, search for **"format on save"**
2. Find **"Editor: Format On Save"**
3. Make sure it's **checked** (this automatically formats your code when you save)

#### C. Enable Suggest on Trigger Characters (Helps You Write Code)

1. In Settings, search for **"suggest on trigger"**
2. Find **"Editor: Quick Suggestions"**
3. Make sure it's **enabled**

### 7. Configure Git Integration (Version Control)

1. In Settings, search for **"git enabled"**
2. Find **"Git: Enabled"**
3. Make sure it's **checked** (this shows file changes in the file explorer)

### 8. Save Your Settings

Your settings are saved automatically! You don't need to do anything special.

**✅ Checkpoint:** Cursor is configured with a comfortable layout and helpful settings!

**Tip:** If you ever want to reset your settings, you can go back to Settings and change them anytime. Don't worry - you can't break anything by changing settings!

---

## Part 6: Configure Cursor

### 1. Login to GitHub in Cursor

1. In Cursor, open the Command Palette:
   - **macOS:** `Command + Shift + P`
   - **Windows:** `Ctrl + Shift + P`
2. Type **"Git: Sign in"** and select it
3. Follow the prompts to authenticate with GitHub
4. You may need to authorize Cursor in your browser

### 2. Setup Cursor Configuration

**What this does:** This fetches the Cursor configuration from [https://github.com/sebyet/cursor-config](https://github.com/sebyet/cursor-config) and copies it into your project. This gives you all the commands and rules you need!

1. In Cursor, open the terminal:
   - **macOS:** `` Command + ` ``
   - **Windows:** `` Ctrl + ` ``
2. Make sure you're in your project folder (you should see your project name in the terminal prompt)
3. Run this command to fetch and copy the Cursor config from https://github.com/sebyet/cursor-config:
   ```bash
   git clone --depth=1 https://github.com/sebyet/cursor-config.git cursor-config-temp && cp -r cursor-config-temp/.cursor . && rm -rf cursor-config-temp
   ```
   **What this does:** Downloads the config, copies the `.cursor` folder to your project, then cleans up the temporary files.
   
   **Note for Windows users:** If the `cp` command doesn't work, you can use this instead:
   ```bash
   git clone --depth=1 https://github.com/sebyet/cursor-config.git cursor-config-temp && xcopy /E /I cursor-config-temp\.cursor .cursor && rmdir /S /Q cursor-config-temp
   ```
4. Wait for it to complete (you should see messages about cloning and copying)
5. **Verify:** Check if you see a `.cursor` folder in your project:
   - In Cursor's file explorer (left sidebar), look for a `.cursor` folder
   - It should contain `commands/` and `rules/` folders
   - If you don't see it, try refreshing the file explorer (right-click → "Refresh")

**✅ Checkpoint:** Cursor configuration is synced from https://github.com/sebyet/cursor-config!

### 3. Configure MCPs (Model Context Protocols)

**Good news:** The MCPs are already included in the `.cursor` folder you just copied! You just need to add your credentials to connect them.

MCPs let Cursor connect to Vercel, Supabase, and other services. The configuration file (`mcp.json`) is already set up with Vercel, Supabase, Shadcn, and Playwright - you just need to add your URLs and tokens.

1. **Find the MCP configuration file:**
   - In Cursor's file explorer, open the `.cursor` folder
   - Look for `mcp.json` file
   - Open it (it should already have MCPs configured: Vercel, Supabase, Shadcn, Playwright)

2. **Get your Vercel credentials:**
   - Go to [vercel.com/account/tokens](https://vercel.com/account/tokens)
   - Click **"Create Token"**
   - Give it a name (e.g., "Cursor MCP")
   - Copy the token (you'll only see it once - save it somewhere safe!)

3. **Get your Supabase credentials:**
   - Go to your Supabase project dashboard
   - Click **"Settings"** → **"API"** (or go to your project settings)
   - Copy your **Project URL** (looks like `https://xxxxx.supabase.co`)
   - Copy your **Service Role Key** or create an **Access Token** in the Access Tokens section

4. **Update the mcp.json file:**
   - Open `.cursor/mcp.json` in Cursor
   - Find the Vercel section and add your token where it says to add credentials
   - Find the Supabase section and add your Project URL and access token
   - Save the file (`Command/Ctrl + S`)

5. **Connect/Reload MCPs:**
   - In Cursor, you may need to restart or reload the MCP connections
   - Try restarting Cursor, or use the Command Palette (`Command/Ctrl + Shift + P`) and search for "MCP" or "Reload"

**Note:** The exact format of mcp.json depends on the version, but it should be clear where to add your credentials. If you're unsure, you can continue - the `@setup-project` command will work, but some MCP features won't be available until credentials are added.

**✅ Checkpoint:** MCPs are configured (or you've noted what needs to be done)!

---

## Part 7: Run Setup Project

Now you're ready to run the setup command!

1. In Cursor, make sure your project folder is open
2. Open the chat/command interface
3. Type: `@setup-project`
4. The command will:
   - Check Node.js, pnpm, and Git
   - Install all packages from your tech stack
   - Set up Supabase connection
   - Install all UI components
   - Configure everything automatically
5. **At the end:** It will show you a summary of what was installed
6. **It will NOT start the server** - that's a separate step!

**✅ Checkpoint:** Your project is set up and ready!

---

## Summary Checklist

Before running `@setup-project`, make sure you have:

### Accounts Created
- [ ] GitHub account (signed in)
- [ ] Vercel account (signed in)
- [ ] Supabase account (signed in)

### Software Installed
- [ ] Node.js installed (verify with `node --version` in Cursor's terminal)
- [ ] pnpm installed (verify with `pnpm --version` in Cursor's terminal)
- [ ] Homebrew installed (macOS only - verify with `brew --version` in Cursor's terminal)
- [ ] Git installed (verify with `git --version` in Cursor's terminal)
- [ ] Cursor installed and signed in
- [ ] Cursor's terminal is set up and working (open with `` Command/Ctrl + ` ``)

### Projects Created
- [ ] Vercel project created (this automatically creates your GitHub repository)
- [ ] GitHub repository URL saved (from Vercel project settings)
- [ ] Supabase project created

### Configuration Done
- [ ] Repository cloned and open in Cursor
- [ ] Cursor layout and settings configured (word wrap, line numbers, theme, etc.)
- [ ] Logged into GitHub in Cursor
- [ ] Cursor config synced from https://github.com/sebyet/cursor-config (`.cursor` folder in project)
- [ ] MCPs configured (added Vercel token and Supabase credentials to `.cursor/mcp.json`)

### Ready to Go
- [ ] All checkboxes above are checked
- [ ] You're in your project folder in Cursor
- [ ] Ready to run `@setup-project`!

---

## Troubleshooting

### "I don't see 'Create Git Repository' in Vercel"
- **Option 1:** Make sure you've authorized Vercel to access GitHub (you may need to connect your GitHub account in Vercel settings first)
- **Option 2:** If you still don't see it, you can create the GitHub repository manually:
  1. Go to [github.com](https://github.com) and sign in
  2. Click the **"+"** icon → **"New repository"**
  3. Give it a name and create it
  4. Then go back to Vercel and click **"Import Git Repository"**
  5. Find your newly created repository and import it

### "I can't clone the repository"
- **Try GitHub Desktop instead** - it's more reliable for non-developers
- Make sure you're signed into GitHub
- Check that the repository URL is correct
- Make sure the repository was created (check on github.com)

### "MCP setup is confusing" or "I can't find mcp.json"
- Make sure you successfully copied the `.cursor` folder (check if `.cursor` folder exists in your project)
- The `mcp.json` file should be in `.cursor/mcp.json`
- If it's missing, try running the Cursor config setup command again
- You can skip MCP setup for now and add credentials later
- The `@setup-project` command will work without MCPs configured
- Some advanced features won't be available until MCPs are configured with your credentials

### "Git commands don't work"
- Make sure Git is installed (check with `git --version` in Cursor's terminal)
- **On Windows:** Make sure you selected "Git from the command line" during installation
- **On macOS:** Make sure Homebrew is installed first, then run `brew install git` in Cursor's terminal
- Try restarting Cursor
- Close and reopen Cursor's terminal (`` Command/Ctrl + ` ``)

### "Homebrew installation failed" or "brew command not found" (macOS only)
- Make sure you ran the Homebrew installation command correctly in Cursor's terminal
- If you see PATH errors, make sure to run the commands it tells you to add Homebrew to your PATH in Cursor's terminal
- Try restarting Cursor after installation
- Check if Homebrew is installed in Cursor's terminal: `brew --version`
- If it still doesn't work, you may need to install Xcode Command Line Tools first:
  - In Cursor's terminal, run: `xcode-select --install`
  - Wait for it to finish, then try installing Homebrew again in Cursor's terminal

### "Node.js commands don't work"
- Make sure Node.js is installed (check with `node --version` in Cursor's terminal)
- Try restarting Cursor
- Close and reopen Cursor's terminal (`` Command/Ctrl + ` ``)

### "pnpm commands don't work" or "pnpm is not recognized"
- Make sure Node.js is installed first (pnpm needs Node.js) - check in Cursor's terminal
- Make sure you ran `npm install -g pnpm` successfully in Cursor's terminal
- Try restarting Cursor
- Close and reopen Cursor's terminal (`` Command/Ctrl + ` ``)
- Try running `npm install -g pnpm` again in Cursor's terminal

---

## What's Next?

After completing all the steps above and running `@setup-project`:

1. **Test the server:** You can test starting the development server separately
2. **Customize your app:** Use `@customize-app` to change colors, fonts, and design
3. **Build features:** Use `@build-feature` to add new functionality
4. **Deploy:** Your Vercel project is already connected - push to GitHub and it will deploy automatically!

You're all set! 🎉
