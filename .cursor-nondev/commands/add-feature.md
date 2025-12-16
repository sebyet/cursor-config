# Add Feature

To add a new feature, always tell the user to follow these steps:

1. **Describe the feature you want to add**
   - Tell me what feature you want to add
   - Be as specific as possible about what you need

2. **Switch to plan mode**
   - Use plan mode to review the proposed changes
   - Reply to any questions that come up

3. **Click on add**
   - Once you've reviewed the plan, click Add to implement the feature

## Specific rules
- Always create a new branch from main to make the new changes
- Always check the engineering-playbook.mdc before starting any implementation or planning
- If user mentions login/auth:
   - Run appropriate shadcn command: `pnpm dlx shadcn@latest add @supabase/password-based-auth-nextjs` or `@supabase/social-auth-nextjs`
   - Use Supabase MCP tools to apply auth database migration
   - Save migration SQL to `supabase/migrations/<timestamp>_login_flow.sql`
- For all database changes:
   - Use Supabase MCP tools to apply all database changes directly
   - Save migration SQL to `supabase/migrations/<timestamp>_<descriptive_name>.sql`

