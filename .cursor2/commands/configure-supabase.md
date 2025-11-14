# Configure Supabase

Configures Supabase (Auth, Database, Storage, Realtime) for your project. Sets up authentication, database connection, storage buckets, and realtime subscriptions automatically.

1. **Check prerequisites**
   - Verify Supabase CLI is installed: `npx supabase --version` (if not, guide installation)
   - Check if Supabase project already exists locally
   - Check if Supabase account is logged in (if using local dev, check for Docker)
   - Verify project structure (Next.js project with package.json)

2. **Install Supabase components**
   - Install core Supabase client for Next.js: `pnpm dlx shadcn@latest add @supabase/supabase-client-nextjs`
   - Install Supabase CLI globally or locally: `pnpm add -D supabase` (or use npx)
   - **Ask user which features they need:**
     - **Password-based auth:** `pnpm dlx shadcn@latest add @supabase/password-based-auth-nextjs`
     - **Social auth (OAuth):** `pnpm dlx shadcn@latest add @supabase/social-auth-nextjs`
     - **File upload (Storage):** `pnpm dlx shadcn@latest add @supabase/dropzone-nextjs`
     - **Realtime cursor:** `pnpm dlx shadcn@latest add @supabase/realtime-cursor-nextjs`
     - **User avatar:** `pnpm dlx shadcn@latest add @supabase/current-user-avatar-nextjs`
     - **Realtime avatar stack:** `pnpm dlx shadcn@latest add @supabase/realtime-avatar-stack-nextjs`
     - **Infinite query hook:** `pnpm dlx shadcn@latest add @supabase/infinite-query-hook`
     - **AI editor rules:** `pnpm dlx shadcn@latest add @supabase/ai-editor-rules`
   - Verify installation completed successfully

3. **Set up Supabase project**
   - **If new project:** Ask user if they want to create a new Supabase project or link to existing
   - **If existing project:** Ask for project URL and anon key
   - Initialize Supabase locally: `npx supabase init` (creates supabase folder)
   - Link to remote project: `npx supabase link --project-ref <project-ref>`
   - Or start local development: `npx supabase start` (requires Docker)

4. **Configure environment variables**
   - Check if `.env.local` exists, create if not
   - Add Supabase environment variables:
     - `NEXT_PUBLIC_SUPABASE_URL` - Your Supabase project URL
     - `NEXT_PUBLIC_SUPABASE_ANON_KEY` - Your Supabase anon/public key
     - `SUPABASE_SERVICE_ROLE_KEY` - Service role key (for server-side operations, keep secret!)
   - Add to `.env.example` (without actual values) for reference
   - Verify variables are set correctly

5. **Set up Supabase client utilities**
   - The `@supabase/supabase-client-nextjs` component should have created client utilities automatically
   - Check if `lib/supabase/client.ts` and `lib/supabase/server.ts` were created
   - Create `lib/supabase/middleware.ts` for middleware authentication (if using middleware)
   - Set up proper TypeScript types for database schema
   - Verify all components installed correctly and utilities are in place

6. **Configure Auth**
   - If password-based auth was installed: Components and utilities should be available
   - If social auth was installed: Set up OAuth providers in Supabase dashboard
   - Create auth callback route: `app/auth/callback/route.ts` (Next.js App Router)
   - Set up middleware for protected routes (if needed)
   - Configure email templates in Supabase dashboard (if using email auth)

7. **Configure Database**
   - Check if database schema exists
   - Set up database migrations (if using migrations)
   - Create initial schema if needed
   - Set up Row Level Security (RLS) policies
   - Configure database functions (if needed)

8. **Configure Storage**
   - If dropzone was installed: File upload component should be available
   - Set up storage buckets in Supabase dashboard (if needed)
   - Configure bucket policies and RLS policies
   - Set up file upload utilities using the dropzone component (if installed)

9. **Configure Realtime**
   - If realtime components were installed: Cursor and avatar stack components should be available
   - Enable Realtime for specific tables/channels in Supabase dashboard (if needed)
   - Set up Realtime subscriptions using the installed components (if needed)
   - Configure Realtime policies
   - If infinite query hook was installed: Use it for paginated realtime data

10. **Test configuration**
    - Test Supabase connection (client and server)
    - Test authentication flow (if configured)
    - Test database connection
    - Test storage upload (if configured)
    - Test Realtime subscription (if configured)
    - Verify all services work correctly

11. **Document configuration**
    - Create `doc/` folder if it doesn't exist
    - Create file: `doc/configure-supabase-YYYY-MM-DD.md`
    - Document: what was configured, environment variables added, services enabled, project URL, configuration details

## What to Tell the User

- Start: "I'll help you configure Supabase for your project. Do you have an existing Supabase project or do you want to create a new one?"
- If new project: "I'll guide you through creating a new Supabase project and connecting it to your app."
- If existing project: "Please provide your Supabase project URL and anon key, or I can help you find them in your Supabase dashboard."
- During setup: "Installing Supabase client components...", "Which features do you need? (Password auth, Social auth, File upload, Realtime, etc.)", "Configuring environment variables...", "Setting up authentication...", etc.
- After configuration: "Supabase is configured! Here's what I set up: [list services]. Your project URL is: [url]. Test it by [suggestion]."
- If errors: Explain what went wrong and how to fix it

## See Also

### Related Services
- **[Configure Vercel](.cursor/commands/configure-vercel.md)**: Hosting and deployment
- **[Configure Resend](.cursor/commands/configure-resend.md)**: Email sending
- **[Configure Trigger.dev](.cursor/commands/configure-trigger-dev.md)**: Background jobs

### Technical Guidelines
- **[Supabase Edge Functions](.cursor/rules/writing-supabase-edge-functions.mdc)**: Server functions
- **[Supabase Realtime](.cursor/rules/use-realtime.mdc)**: Real-time features
- **[Create Migrations](.cursor/rules/create-migration.mdc)**: Database migration guidelines
- **[RLS Policies](.cursor/rules/create-rls-policies.mdc)**: Security policies
- **[Postgres SQL Style](.cursor/rules/postgres-sql-style-guide.mdc)**: Database code style
- **[Supabase Documentation](https://supabase.com/docs)**: Official Supabase docs

