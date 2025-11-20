# Setup New Project

Set up a brand new project from scratch so you can start building your website or app.

**For Non-Technical Users:** Don't worry about the technical details below - I'll guide you through everything step-by-step in simple terms. Just follow along and I'll handle all the complicated stuff!

## What This Does (In Simple Terms)

I'm going to:
1. Check if you have the basic tools installed (like checking if you have a word processor)
2. Create a folder for your project (like creating a new folder on your computer)
3. Set up everything your website needs (like installing all the parts)
4. Connect it to online services (so you can save your work and make it live)
5. Make it look nice (customize colors and styles)

**You'll just need to:** Answer a few questions and sign in to some services when I ask.

---

## Technical Steps (I handle these automatically)

1. **Verify prerequisites before starting**
   - **Check if project name provided:** Ask the user what they want to name their project if not provided
   - **Verify Node.js is installed:** Check with `node --version` (if not, guide them: "I need to install the tools that run websites - this is like installing an app. I'll guide you through it.")
   - **Verify pnpm is installed:** Check with `pnpm --version` (if not, guide them: "I need to install a package manager - this helps organize all the parts your website needs. I'll install it for you.")
   - **Verify Git is installed:** Check with `git --version` (if not, guide them: "I need to install Git - this saves your work automatically so you don't lose anything. Think of it like auto-save in Google Docs.")
   - **Verify Git is latest stable version:** 
     - Get current version: `git --version`
     - Check latest stable version: On macOS with Homebrew, use `brew info git | grep "stable"` or check if outdated with `brew outdated git`
     - If outdated or not installed via Homebrew: Update with `brew upgrade git` (if installed via Homebrew) or install latest with `brew install git`
     - On other platforms: Check latest version from git-scm.com and guide manual update if needed
   - **Verify Git is authenticated:** Check with `git config --global user.name` and `git config --global user.email` (if not configured, help them set it up)
   - **Verify Vercel CLI is installed:** Check with `vercel --version` (if not, guide them: "I need to install Vercel - this makes your website live on the internet. Think of it like the tool that publishes your blog post so everyone can see it.")
   - **Verify Vercel CLI is latest stable version:**
     - Get current version: `vercel --version`
     - Check latest stable version: `npm view vercel version` or `pnpm view vercel version`
     - Compare versions and if outdated, update with `npm install -g vercel@latest` or `pnpm add -g vercel@latest`
   - **Verify Vercel is logged in:** Check with `vercel whoami` (if not logged in, use `expect` to automate login with Google - arrow down once from default GitHub option, then Enter)
   - **Verify GitHub CLI is installed:** Check with `gh --version` (if not, guide them: "I need to install GitHub - this stores your project online so you can access it from anywhere. Think of it like Google Drive for your website files.")
   - **Verify GitHub is logged in:** Check with `gh auth status` (if not logged in, guide them to log in with `gh auth login`)
  - **Do not proceed with installation until all prerequisites are met**
  - **If Vercel not logged in:** Automate login using `expect` to select Google:
    ```bash
    expect -c "
    set timeout 60
    spawn vercel login
    expect {
        \"Log in to Vercel\" {
            send \"\\033\[B\\r\"
        }
        timeout {
            puts \"Timeout waiting for login menu\"
            exit 1
        }
    }
    expect eof
    "
    ```
    - This automatically selects "Continue with Google" (arrow down once from default GitHub option, then Enter)
    - The browser will open for Google authentication - wait for user to complete authentication
  - Tell the user what you found and what needs to be installed/configured

2. **Get project name and initialize**
   - **If project name not provided:** Ask the user what they want to name their project
   - Navigate to or create the `Projects/sebastien/` folder
   - **Run the initialization with automated prompts:** Use `expect` inline to handle all interactive prompts automatically:
     ```bash
     cd /Users/sebastien.payet/Projects/sebastien
     expect -c "
     set timeout 60
     spawn pnpm dlx shadcn@latest init
     expect {
         \"Would you like to start a new project?\" {
             send \"\033\[B\r\"
         }
         timeout {
             puts \"Timeout waiting for project type prompt\"
             exit 1
         }
     }
     expect {
         \"What is your project named?\" {
             send \"$project_name\r\"
         }
         timeout {
             puts \"Timeout waiting for project name prompt\"
             exit 1
         }
     }
     expect {
         \"Which color would you like to use as the base color?\" {
             send \"neutral\r\"
         }
         timeout {
             puts \"Timeout waiting for color prompt\"
             exit 1
         }
     }
     expect eof
     "
     ```
     - Replace `$project_name` with the actual project name provided by the user
   - The initialization will automatically:
     - Detect that there's no package.json file in the current directory
     - Select "Next.js 16" (arrow down once from default "Next.js 15")
     - Enter the project name you provided
     - Choose "Neutral" as the base color
     - Create a new Next.js 16 project in a folder named after your project
     - Write `components.json` configuration file
     - Check the registry
     - Update CSS variables in `app/globals.css`
     - Install dependencies automatically
     - Create `lib/utils.ts` file

3. **Copy .cursor folder**
   - Navigate to the project folder (created in step 2)
   - Copy the `.cursor` folder from `/Users/sebastien.payet/Projects/sebastien/.cursor` to the newly created project folder
   - This includes all Cursor commands and rules that should be available in the new project
   - Use: `cp -r /Users/sebastien.payet/Projects/sebastien/.cursor /Users/sebastien.payet/Projects/sebastien/$project_name/`
   - Verify the `.cursor` folder was copied successfully

4. **Install all shadcn components**
   - Navigate to the project folder (created in step 2)
   - Install all available shadcn/ui components: `pnpm dlx shadcn@latest add --all --yes`
   - `--all`: Adds all available components from the registry
   - `--yes`: Skips confirmation prompts for each component
   - Verify installation completed successfully

5. **Set up Supabase**
   - Navigate to the project folder (created in step 2)
   - **Ask user to create/select Supabase project:** "Let's set up Supabase for your database and authentication. Please create a new project (or select an existing one) in the Supabase dashboard and update your MCP configuration with the project ID and access token."
   - **Install Supabase client:** Run `pnpm dlx shadcn@latest add @supabase/supabase-client-nextjs` automatically
   - **Retrieve credentials via MCP:** Use `mcp_supabase_get_project_url` and `mcp_supabase_get_publishable_keys` to get project URL and anon key
   - **Configure environment:** Automatically append both values to `.env.local` (create if it doesn't exist)
   - **Remind about deployment:** Remind user to mirror these values in every deployment secret store (Vercel, etc.)
   - Verify installation completed successfully

6. **Check project state**
   - Check if project already exists (if yes, ask if they want to start fresh)
   - Check if Git is already initialized in project (if yes, ask if they want to use it or start fresh)
   - Check if Vercel is already connected to project (if yes, ask if they want to use it or start fresh)

7. **Set up Git in project**
   - **If Git not initialized:** Initialize Git and create `.gitignore`
   - **If Git already initialized:** Ask if they want to use it or start fresh
   - Make the first save (commit) of your project

8. **Connect to GitHub**
   - Check if repository already exists
   - **If no repository:** Help them create a new repository on GitHub
   - Connect their local project to GitHub
   - Upload the first version to GitHub

9. **Connect to Vercel**
   - Check if Vercel project already exists
   - **If Vercel not connected:** Initialize Vercel project (`vercel init` or `vercel link`)
   - **If first time:** Guide them through Vercel setup step-by-step
   - Connect project to Vercel account
   - Set up automatic deployments from GitHub (connect GitHub repo to Vercel)
   - Configure project settings (framework preset, build settings, environment variables if needed)
   - Tell them their deployment URL once connected

10. **Verify dependencies**
   - Dependencies are automatically installed during `pnpm dlx shadcn@latest init --template next-16 --base-color neutral --yes`
   - shadcn/ui components were installed in step 4 using `pnpm dlx shadcn@latest add --all --yes`
   - Supabase dependencies were installed in step 5
   - Verify that all installations completed successfully
   - **If installation failed:** Run `pnpm install` manually to retry
   - **If already installed:** Verify everything is up to date
   - Tell them if anything goes wrong
   - Make sure everything installed correctly

11. **Customize design system** (automatic after project setup)
   - After project is set up, automatically route to `customize-design-system.md`
   - Guide user through customizing colors, fonts, and styles
   - This happens automatically - don't ask, just do it
   - Tell user: "Great! Your project is set up. Now let me customize your design system - I'll ask you a few questions about colors and styles to make it look great!"

12. **Test it works**
   - Try to start the project locally
   - Tell them if it works or if there are problems
   - Optionally trigger a test deployment to Vercel to verify everything works

13. **Document setup**
   - Create `doc/` folder if it doesn't exist
   - Create file: `doc/init-project-YYYY-MM-DD.md`
   - Document: project initialization, tools and versions used, configuration
   - Include setup details, what was installed (including all shadcn/ui components and Supabase), design system customization, initial configuration, GitHub repo URL, and Vercel deployment URL

## What to Tell the User

**For Non-Technical Users:**
- Start by asking for the project name if not provided
- **Explain what we're doing:** "I'm going to set up your new project. This will create all the files and folders needed for your website. I'll guide you through each step!"
- **Verify prerequisites FIRST:** Before starting, check what tools are installed. Explain in simple terms:
  - "Let me check if you have the basic tools installed..."
  - "I need to install [tool name] - this is like installing an app on your computer. I'll guide you through it."
  - **Never use technical jargon** - Instead of "Node.js", say "the programming language runtime" or just "the tools needed to run your website"
  - **Explain why we need each tool:**
    - Git = "Saves your work so you don't lose it"
    - GitHub = "Stores your project online so you can access it anywhere"
    - Vercel = "Makes your website live on the internet"
    - Supabase = "Stores your data and handles user accounts"
- **Check and update versions:** If tools are outdated, explain: "I need to update [tool] to the latest version - this ensures everything works smoothly"
- Do not proceed with project initialization until all prerequisites are met
- **Explain each step simply:**
  - "Now I'm creating your project folder..."
  - "I'm installing all the building blocks your website needs..."
  - "I'm connecting your project to GitHub so it's saved online..."
- Only set up what's needed - skip steps that are already done
- **If something needs user action:** Explain clearly what they need to do and why
  - "I need you to log into GitHub - this lets me save your project online"
  - "I'll open your browser for you to sign in - just follow the prompts"
- If there are errors, explain what they mean in simple terms: "Something went wrong with [X]. Here's what happened: [simple explanation]. I'll fix it by [action]"
- Celebrate when everything works: "All done! Your project is ready. You can now start building features!"

## Smart Setup Strategy

**Check in this order:**
1. Ask for project name if not provided
2. **Verify prerequisites (REQUIRED before proceeding):**
   - Check Node.js is installed (`node --version`)
   - Check pnpm is installed (`pnpm --version`)
   - Check Git is installed (`git --version`)
   - Check Git is latest stable version:
     - Get current version: `git --version`
     - Check latest: On macOS with Homebrew, use `brew outdated git` or `brew info git`
     - If outdated: Update with `brew upgrade git` (if via Homebrew) or install latest with `brew install git`
   - Check Git is authenticated (`git config --global user.name` and `git config --global user.email`)
   - Check Vercel CLI is installed (`vercel --version`)
   - Check Vercel CLI is latest stable version:
     - Get current version: `vercel --version`
     - Check latest: `npm view vercel version` or `pnpm view vercel version`
     - If outdated: Update with `npm install -g vercel@latest` or `pnpm add -g vercel@latest`
   - Check Vercel is logged in (`vercel whoami`)
   - Check GitHub CLI is installed (`gh --version`)
   - Check GitHub is logged in (`gh auth status`)
   - **Do not proceed until all prerequisites are met**
3. Navigate to `Projects/sebastien/` folder
4. Create project directory and initialize with shadcn/ui:
   - Create the project directory: `mkdir -p /Users/sebastien.payet/Projects/sebastien/$project_name`
   - Navigate into the project directory: `cd /Users/sebastien.payet/Projects/sebastien/$project_name`
   - Run initialization with CLI flags: `pnpm dlx shadcn@latest init --template next-16 --base-color neutral --yes`
   - The CLI will automatically detect if no package.json exists in current directory
   - Creates Next.js project, sets up configuration, and installs dependencies
5. Copy `.cursor` folder from parent directory to new project
6. Install all shadcn/ui components (`pnpm dlx shadcn@latest add --all --yes`)
7. Set up Supabase (install @supabase/supabase-js)
8. Project state (Git initialized in project, dependencies installed)
9. Repository (GitHub repo exists)
10. Deployment (Vercel project connected)

**Prerequisites must be met before starting:**
- If Node.js not installed → Guide installation, then stop
- If pnpm not installed → Guide installation (`npm install -g pnpm`), then stop
- If Git not installed → Guide installation, then stop
- If Git not latest stable version → Check latest version and update:
  - On macOS with Homebrew: Check with `brew outdated git`, update with `brew upgrade git` or install with `brew install git`
  - On other platforms: Check latest from git-scm.com and guide manual update
  - Then stop
- If Git not authenticated → Help configure (`git config --global user.name` and `git config --global user.email`), then stop
- If Vercel CLI not installed → Guide installation (`npm i -g vercel` or `pnpm add -g vercel`), then stop
- If Vercel CLI not latest stable version → Check latest with `npm view vercel version` or `pnpm view vercel version`, update with `npm install -g vercel@latest` or `pnpm add -g vercel@latest`, then stop
- If Vercel not logged in → Use `expect` to automate login with Google (arrow down once to select Google, then Enter), then wait for browser authentication, then stop
- If GitHub CLI not installed → Guide installation (`brew install gh` on macOS, or see github.com/cli/cli for other platforms), then stop
- If GitHub not logged in → Guide login (`gh auth login`), then stop

**Only set up what's needed:**
- If project already initialized → Ask if they want to use it or start fresh
- If Git already initialized in project → Ask if they want to use it
- If Vercel already connected to project → Ask if they want to use it
- If dependencies already installed → Skip or verify up to date

## Checklist

- [ ] Asked for project name (if not provided)
- [ ] **Verified prerequisites (BEFORE starting installation):**
  - [ ] Node.js is installed (`node --version`)
  - [ ] pnpm is installed (`pnpm --version`)
  - [ ] Git is installed (`git --version`)
  - [ ] Git is latest stable version (checked with `brew outdated git` on macOS, updated if needed)
  - [ ] Git is authenticated (`git config --global user.name` and `git config --global user.email`)
  - [ ] Vercel CLI is installed (`vercel --version`)
  - [ ] Vercel CLI is latest stable version (checked with `npm view vercel version` or `pnpm view vercel version`, updated if needed)
  - [ ] Vercel is logged in (`vercel whoami`) - if not, automated login with Google via expect
  - [ ] GitHub CLI is installed (`gh --version`)
  - [ ] GitHub is logged in (`gh auth status`)
- [ ] Navigated to `Projects/sebastien/` folder
- [ ] Initialized project with shadcn/ui using expect to automate `pnpm dlx shadcn@latest init`:
  - [ ] Used inline expect command to handle all prompts automatically
  - [ ] Selected "Next.js 16" via expect (arrow down once from default, then Enter)
  - [ ] Entered project name via expect
  - [ ] Selected "neutral" as base color via expect
  - [ ] Project folder created automatically with project name
  - [ ] Dependencies installed automatically
- [ ] Copied .cursor folder to new project
- [ ] Installed all shadcn/ui components:
  - [ ] Ran `pnpm dlx shadcn@latest add --all --yes`
  - [ ] Verified installation completed successfully
- [ ] Set up Supabase:
  - [ ] Installed @supabase/supabase-js
- [ ] Checked project state (project exists, Git initialized, Vercel connected)
- [ ] Git initialized in project
- [ ] Project files saved locally
- [ ] Connected to GitHub
- [ ] Connected to Vercel
- [ ] Automatic deployments configured (GitHub → Vercel)
- [ ] Project starts without errors locally
- [ ] Test deployment works (optional)
- [ ] Customized design system (automatically after project setup)
- [ ] Created documentation file: `doc/init-project-YYYY-MM-DD.md`

## Important Notes

- **Prerequisites Required:** Before starting any installation, verify that Node.js, pnpm, Git (latest stable), Vercel CLI (latest stable), and GitHub CLI are installed, and that Git, Vercel, and GitHub are authenticated/logged in. Do not proceed with project initialization until all prerequisites are met.
- **Git Version Check:** Verify Git is at the latest stable version. On macOS with Homebrew: Check with `brew outdated git`, update with `brew upgrade git` or install latest with `brew install git`. On other platforms: Check latest version from git-scm.com and guide manual update if needed.
- **Git Authentication:** Check with `git config --global user.name` and `git config --global user.email`. If not set, help configure with `git config --global user.name "Your Name"` and `git config --global user.email "your.email@example.com"`.
- **Vercel CLI Version Check:** Verify Vercel CLI is at the latest stable version. Check latest with `npm view vercel version` or `pnpm view vercel version`. Compare with current version from `vercel --version`. If outdated, update with `npm install -g vercel@latest` or `pnpm add -g vercel@latest`.
- **Vercel Authentication:** Check with `vercel whoami`. If not logged in, use `expect` to automate `vercel login` with Google selection (arrow down once from default GitHub option, then Enter). The browser will open for Google authentication - wait for user to complete authentication in the browser.
- **GitHub Authentication:** Check with `gh auth status`. If not logged in, guide user to run `gh auth login` before proceeding. GitHub CLI can be installed with `brew install gh` on macOS, or see github.com/cli/cli for other platforms.
- **Project Name:** Ask the user for the project name if not provided
- **Project Location:** Run from `Projects/sebastien/` folder - the tool will create the project folder automatically (typically `~/Projects/sebastien/{project-name}/` or `/Users/sebastien/Projects/sebastien/{project-name}/`)
- **Project Initialization Process:**
  - Use `expect` inline command to automate `pnpm dlx shadcn@latest init` - see step 2 for the complete expect command
  - The tool automatically checks if current directory has a package.json file
  - Expect handles all interactive prompts automatically:
    - **Project Type Selection:** Detects "Would you like to start a new project?" prompt, sends arrow down (ESC[B) to select "Next.js 16", then Enter
    - **Project Name:** Detects "What is your project named?" prompt, sends the project name and Enter
    - **Base Color:** Detects "Which color would you like to use as the base color?" prompt, sends "neutral" and Enter
  - The tool automatically creates Next.js 16 project with shadcn/ui configured
  - Creates `components.json`, updates `app/globals.css`, installs dependencies, creates `lib/utils.ts`
- **No User Interaction Required:** All prompts are handled automatically via expect - do not ask the user to interact with the terminal. The expect command handles arrow key navigation and text input programmatically.
- **Package Manager:** Use `pnpm` as the package manager (install with `npm install -g pnpm` if needed)
- **.cursor Folder:** Before installing shadcn components, copy the `.cursor` folder from `/Users/sebastien.payet/Projects/sebastien/.cursor` to the new project to include all Cursor commands and rules
- **shadcn Components:** After copying the `.cursor` folder, install all available shadcn/ui components using `pnpm dlx shadcn@latest add --all --yes`
- **Supabase Setup:** After installing all shadcn components, install the Supabase JavaScript client
- **Vercel Setup:** Vercel login is automated using `expect` to select Google authentication. The browser will open for Google OAuth - wait for user to complete authentication in the browser.
- **Automatic Deployments:** Once GitHub and Vercel are connected, pushes to main/master branch will automatically deploy
- **Deployment URL:** Vercel will provide a deployment URL (e.g., `your-project.vercel.app`)
- **Free Tier:** Vercel is free for personal projects with generous limits

