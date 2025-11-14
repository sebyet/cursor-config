# Configure Trigger.dev

Configures Trigger.dev for background jobs and scheduled tasks in your project. Sets up API keys, task definitions, and job scheduling.

1. **Check prerequisites**
   - Verify Trigger.dev account exists (user needs to create account at trigger.dev)
   - Check if Trigger.dev API key is already configured
   - Verify project structure (Next.js project with package.json)
   - Verify Node.js version (Trigger.dev requires Node.js 18+)

2. **Install Trigger.dev SDK**
   - Install `@trigger.dev/sdk` package: `pnpm add @trigger.dev/sdk`
   - Install Trigger.dev CLI: `pnpm add -D @trigger.dev/cli` (or use npx)
   - Verify installation completed successfully

3. **Set up Trigger.dev account**
   - **If no account:** Guide user to create account at trigger.dev
   - **If account exists:** Ask for API key or guide to find it in dashboard
   - Verify API key is valid (test connection)

4. **Initialize Trigger.dev**
   - Run `npx @trigger.dev/cli@latest init` to initialize Trigger.dev in project
   - This creates `trigger.config.ts` configuration file
   - Creates `trigger` directory for task definitions
   - Sets up project structure

5. **Configure environment variables**
   - Check if `.env.local` exists, create if not
   - Add Trigger.dev environment variables:
     - `TRIGGER_SECRET_KEY` - Your Trigger.dev secret key
     - `TRIGGER_PUBLIC_API_KEY` - Your Trigger.dev public API key (if needed)
   - Add to `.env.example` (without actual values) for reference
   - Verify variables are set correctly

6. **Configure Trigger.dev project**
   - Link project to Trigger.dev account: `npx @trigger.dev/cli@latest login` and `npx @trigger.dev/cli@latest link`
   - Set project ID in `trigger.config.ts`
   - Configure project settings (dev server URL, etc.)

7. **Set up task definitions**
   - Create task files in `trigger` directory
   - Define task structure and handlers
   - Set up task scheduling (if needed)
   - Configure task retries and error handling

8. **Set up development server**
   - Configure Trigger.dev dev server URL (usually `http://localhost:3000/api/trigger`)
   - Set up API route for Trigger.dev webhooks: `app/api/trigger/route.ts`
   - Configure webhook authentication

9. **Set up production webhook**
   - Configure production webhook URL in Trigger.dev dashboard
   - Set up webhook endpoint in production
   - Verify webhook is working

10. **Test task execution**
    - Test running a task locally
    - Test task scheduling (if configured)
    - Test error handling and retries
    - Verify tasks appear in Trigger.dev dashboard

11. **Document configuration**
    - Create `doc/` folder if it doesn't exist
    - Create file: `doc/configure-trigger-dev-YYYY-MM-DD.md`
    - Document: API keys configured, tasks created, webhook URLs, configuration details

## What to Tell the User

- Start: "I'll help you configure Trigger.dev for background jobs. Do you have a Trigger.dev account? If not, you'll need to create one at trigger.dev."
- If no account: "Please create a Trigger.dev account at trigger.dev, then provide your API key."
- If account exists: "Please provide your Trigger.dev API key, or I can help you find it in your Trigger.dev dashboard."
- During setup: "Installing Trigger.dev SDK...", "Initializing Trigger.dev...", "Configuring environment variables...", "Setting up task definitions..."
- After configuration: "Trigger.dev is configured! I've set up the task structure. You can now create background jobs and scheduled tasks."
- If errors: Explain what went wrong and how to fix it

## See Also

### Related Services
- **[Configure Supabase](.cursor/commands/configure-supabase.md)**: Auth, Database, Storage, Realtime
- **[Configure Vercel](.cursor/commands/configure-vercel.md)**: Hosting and deployment
- **[Configure Resend](.cursor/commands/configure-resend.md)**: Email sending

### Technical Guidelines
- **[Writing Tasks](.cursor/rules/writing-tasks.mdc)**: Guidelines for writing Trigger.dev tasks
- **[Trigger.dev Documentation](https://trigger.dev/docs)**: Official Trigger.dev docs




