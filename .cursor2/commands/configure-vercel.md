# Configure Vercel

Configures Vercel for hosting and deployment of your Next.js project. Sets up automatic deployments, environment variables, and project settings.

1. **Check prerequisites**
   - Verify Vercel CLI is installed: `vercel --version` (if not, install with `pnpm add -g vercel` or `npm i -g vercel`)
   - Verify Vercel is logged in: `vercel whoami` (if not, use `expect` to automate login with Google - arrow down once from default GitHub option, then Enter)
   - Check if project is already linked to Vercel (look for `.vercel` folder)
   - Verify project structure (Next.js project with package.json)
   - Verify Git is initialized and repository exists

2. **Link project to Vercel**
   - **If not linked:** Initialize Vercel project: `vercel link`
     - Select or create Vercel project
     - Choose scope (team or personal account)
     - Configure project settings
   - **If already linked:** Check current link status
   - Verify `.vercel` folder exists with project configuration

3. **Configure project settings**
   - Set framework preset (should auto-detect Next.js)
   - Configure build settings (build command, output directory, install command)
   - Set up environment variables (if needed)
   - Configure domain settings (if needed)
   - Set up preview deployments (if needed)

4. **Set up environment variables**
   - Check `.env.local` for environment variables
   - Add environment variables to Vercel project:
     - Use `vercel env add <key>` for each variable
     - Or use Vercel dashboard to add variables
   - Configure for different environments (production, preview, development)
   - Verify all required variables are set

5. **Connect GitHub repository (if not already connected)**
   - Check if GitHub repo is connected to Vercel
   - **If not connected:** Guide through connecting GitHub repo
     - Use Vercel dashboard: Project Settings → Git
     - Or use `vercel git connect`
   - Configure automatic deployments:
     - Production: Deploy from main/master branch
     - Preview: Deploy from all other branches and pull requests
   - Verify automatic deployments are enabled

6. **Configure deployment settings**
   - Set up build command (if custom)
   - Set up install command (if custom)
   - Configure output directory (if custom)
   - Set up ignore files (if needed)
   - Configure node version (if needed)

7. **Test deployment**
   - Deploy to preview: `vercel` (or `vercel --prod` for production)
   - Verify deployment succeeds
   - Check deployment URL
   - Test the deployed application
   - Verify all features work in production environment

8. **Set up custom domain (optional)**
   - If user wants custom domain: Guide through domain setup
   - Add domain in Vercel dashboard
   - Configure DNS settings
   - Verify domain is working

9. **Document configuration**
    - Create `doc/` folder if it doesn't exist
    - Create file: `doc/configure-vercel-YYYY-MM-DD.md`
    - Document: project URL, deployment URLs, environment variables configured, Git integration, deployment settings

## What to Tell the User

- Start: "I'll help you configure Vercel for hosting and deployment. Checking if you're logged in..."
- If not logged in: "I'll log you in to Vercel automatically..." (use expect to automate Google login)
- During setup: "Linking project to Vercel...", "Configuring environment variables...", "Setting up automatic deployments..."
- After configuration: "Vercel is configured! Your project is live at: [deployment-url]. Automatic deployments from GitHub are enabled."
- If errors: Explain what went wrong and how to fix it

## See Also

### Related Services
- **[Configure Supabase](.cursor/commands/configure-supabase.md)**: Auth, Database, Storage, Realtime
- **[Configure Resend](.cursor/commands/configure-resend.md)**: Email sending
- **[Configure Trigger.dev](.cursor/commands/configure-trigger-dev.md)**: Background jobs

### Technical Guidelines
- **[Next.js Documentation](https://nextjs.org/docs)**: Next.js deployment guide
- **[Vercel Documentation](https://vercel.com/docs)**: Official Vercel docs




