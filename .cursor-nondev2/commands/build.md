# Build → "Create something"

Help the user create new features, components, or functionality in their application. This is the main command for building new things!

## What This Does

1. **Understand what to create**
   - Ask the user what they want to build
   - Clarify requirements and specifications
   - Understand the context and purpose

2. **Plan the implementation**
   - Review the engineering-playbook.mdc before starting
   - Create a plan for what needs to be built
   - Identify dependencies and requirements
   - Use plan mode to review proposed changes

3. **Build it**
   - Always create a new branch from main for new changes
   - Implement the feature following best practices
   - Follow the engineering playbook guidelines
   - Create clean, maintainable code

4. **Handle special cases**
   - **If login/auth mentioned:** Run appropriate shadcn command: `pnpm dlx shadcn@latest add @supabase/password-based-auth-nextjs` or `@supabase/social-auth-nextjs`
   - **For database changes:** Use Supabase MCP tools to apply all database changes directly
   - **Save migrations:** Save migration SQL to `supabase/migrations/<timestamp>_<descriptive_name>.sql`

## What to Tell the User

**When starting:**
- "What would you like to create?"
- "Tell me what you want to build, and I'll help you create it!"

**When planning:**
- "Let me plan this out first..."
- "I'll review the engineering guidelines and create a plan"
- "Use plan mode to review the proposed changes, then click Add to implement"

**When building:**
- "Creating a new branch for this work..."
- "Building [feature name] now..."
- "Following best practices and guidelines..."

**When done:**
- "✅ Created [feature name]!"
- "Your new feature is ready. Want to test it?"

## Specific Rules

- Always create a new branch from main to make the new changes
- Always check the engineering-playbook.mdc before starting any implementation or planning
- If user mentions login/auth:
  - Run appropriate shadcn command: `pnpm dlx shadcn@latest add @supabase/password-based-auth-nextjs` or `@supabase/social-auth-nextjs`
  - Use Supabase MCP tools to apply auth database migration
  - Save migration SQL to `supabase/migrations/<timestamp>_login_flow.sql`
- For all database changes:
  - Use Supabase MCP tools to apply all database changes directly
  - Save migration SQL to `supabase/migrations/<timestamp>_<descriptive_name>.sql`

