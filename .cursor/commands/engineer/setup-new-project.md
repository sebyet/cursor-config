# Setup New Project

Set up a brand new project from scratch so you can start building your website or app.

1. **Verify prerequisites before starting**
   - **Check if project name provided:** Ask the user what they want to name their project if not provided
   - **Verify Node.js is installed:** Check with `node --version` (if not, guide them to install Node.js first)
   - **Verify pnpm is installed:** Check with `pnpm --version` (if not, guide them to install pnpm with `npm install -g pnpm`)
   - **Verify Git is installed:** Check with `git --version` (if not, guide them to install Git first)
   - **Verify Git is authenticated:** Check with `git config --global user.name` and `git config --global user.email` (if not configured, help them set it up)
   - **Verify Vercel CLI is installed:** Check with `vercel --version` (if not, guide them to install Vercel CLI with `npm i -g vercel` or `pnpm add -g vercel`)
   - **Verify Vercel is logged in:** Check with `vercel whoami` (if not logged in, use `expect` to automate login with Google - arrow down once from default GitHub option, then Enter)
   - **Verify GitHub CLI is installed:** Check with `gh --version` (if not, guide them to install GitHub CLI with `brew install gh` on macOS or see github.com/cli/cli for other platforms)
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
   - Install Supabase JavaScript client: `pnpm add @supabase/supabase-js`
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
   - After project is set up, automatically route to `design/customize-design-system.md`
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

- Start by asking for the project name if not provided
- **Verify prerequisites FIRST:** Before starting any installation, check that Node.js, pnpm, Git, Vercel CLI, and GitHub CLI are installed, and that Git, Vercel, and GitHub are logged in/authenticated
- Do not proceed with project initialization until all prerequisites are met
- Navigate to `Projects/sebastien/` folder
- Create the project directory first, then navigate into it
- Use shadcn CLI flags (`--template next-16 --base-color neutral --yes`) to initialize the project without prompts
- The CLI will automatically create the Next.js project, set up shadcn/ui configuration, and install dependencies
- Copy the `.cursor` folder from the parent directory to the new project to include all Cursor commands and rules
- Install all available shadcn/ui components using `--all --yes` flags
- Set up Supabase by installing the JavaScript client
- List what you found (e.g., "Node.js installed ✓, pnpm installed ✓, Git installed and configured ✓, Vercel CLI installed and logged in ✓")
- Only set up what's needed - skip steps that are already done
- Explain each step in simple words before doing it
- Show them what's happening as you go
- If there are errors, explain what they mean in simple terms
- Celebrate when everything works!

## Smart Setup Strategy

**Check in this order:**
1. Ask for project name if not provided
2. **Verify prerequisites (REQUIRED before proceeding):**
   - Check Node.js is installed (`node --version`)
   - Check pnpm is installed (`pnpm --version`)
   - Check Git is installed (`git --version`)
   - Check Git is authenticated (`git config --global user.name` and `git config --global user.email`)
   - Check Vercel CLI is installed (`vercel --version`)
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
- If Git not authenticated → Help configure (`git config --global user.name` and `git config --global user.email`), then stop
- If Vercel CLI not installed → Guide installation (`npm i -g vercel` or `pnpm add -g vercel`), then stop
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
  - [ ] Git is authenticated (`git config --global user.name` and `git config --global user.email`)
  - [ ] Vercel CLI is installed (`vercel --version`)
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

- **Prerequisites Required:** Before starting any installation, verify that Node.js, pnpm, Git, Vercel CLI, and GitHub CLI are installed, and that Git, Vercel, and GitHub are authenticated/logged in. Do not proceed with project initialization until all prerequisites are met.
- **Git Authentication:** Check with `git config --global user.name` and `git config --global user.email`. If not set, help configure with `git config --global user.name "Your Name"` and `git config --global user.email "your.email@example.com"`.
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

