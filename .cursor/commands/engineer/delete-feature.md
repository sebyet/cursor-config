# Delete Feature

Deletes an existing feature completely! Identifies the feature, checks dependencies, removes it safely, verifies nothing broke, and updates documentation. All automatically. Just describe which feature to delete!

1. **Identify which feature to delete**
   - Search codebase for features (components, pages, sections)
   - Check `doc/` folder for feature documentation
   - List available features if needed
   - Ask user to specify which feature to delete
   - Show examples: "course preview modal", "hero section", "footer"

2. **Understand deletion scope**
   - Find all files related to the feature
   - Check all imports and usages
   - Identify dependencies (what breaks if deleted?)
   - Check if feature is used elsewhere
   - Warn about impact if needed
   - Ask for confirmation if risky

3. **Check and setup automatically**
   - Check if project is ready (Git, dependencies)
   - Auto-setup anything that's missing
   - Create feature branch if needed
   - Don't ask - just do it!

4. **Quick validation** (30 seconds max)
   - Read feature documentation if exists (`doc/feature-*.md`)
   - Understand current implementation
   - Find all related files (components, pages, tests, docs)
   - Check dependencies: What uses this feature?
   - Identify impact: What breaks if deleted?
   - If risky: Ask 1 clarifying question about confirmation
   - Proceed immediately - don't overthink!

5. **Delete it safely**
   - Delete feature files (components, pages, etc.)
   - Remove imports from files that use it
   - Clean up references in other files
   - Update parent components/pages if needed
   - Remove or update routes if needed
   - Delete test files related to feature
   - Show what you're deleting
   - Ask for clarification if unclear

6. **Verify nothing broke**
   - Check for broken imports
   - Check for broken references
   - Check for broken routes
   - Fix any issues automatically
   - Run build check if needed

7. **Auto-preview**
   - Start the development server automatically (if not running)
   - Show them the preview URL
   - Tell them to check it out
   - Wait for their confirmation

8. **Auto-finish after confirmation**
   - Once they confirm it looks good
   - Automatically clean up code
   - Update or remove feature documentation
   - Tell them when it's done!

9. **Update documentation automatically**
   - Find existing feature doc: `doc/feature-{feature-name}-*.md`
   - If exists: Add deletion section with date, why deleted, impact
   - Or mark as deprecated/deleted
   - Include what was removed and why

## What to Tell the User

- Start: "Which feature do you want to delete? Examples: 'course preview modal', 'hero section', 'footer'"
- If multiple features found: List them and ask to choose
- After identifying feature: "Found it! This feature is used in: [list]. Deleting it will: [impact]. Continue?"
- If risky: "Warning: This feature is used in [X places]. Deleting it will remove [functionality]. Are you sure?"
- After validation: "Got it! Deleting [feature]... [quick notes]"
- Delete step by step, explaining what you're removing
- When done deleting: "I've deleted your feature and cleaned up references! Let me verify nothing broke..."
- After verification: "Verified! Nothing broke. Let me start a preview for you..."
- Show them the URL (usually http://localhost:3000)
- Tell them to open it in their browser and check it out
- After they confirm it looks good: "Great! Let me finish everything up - cleaning and updating documentation..."
- When done: "Done! Feature deleted successfully! Here's what I removed: [list]. Documentation has been updated."

## See Also

### For New Features
- **[Add Feature](.cursor/commands/add-feature.md)**: Add completely new features from scratch
- **[Modify Feature](.cursor/commands/modify-feature.md)**: Change existing features
- **[Brainstorm Feature](.cursor/commands/product/brainstorm-feature.md)**: Deep analysis and planning for complex features

### Configuration Services
- **[Configure Supabase](.cursor/commands/configure-supabase.md)**: Set up Auth, Database, Storage, and Realtime
- **[Configure Vercel](.cursor/commands/configure-vercel.md)**: Set up hosting and deployment
- **[Configure Resend](.cursor/commands/configure-resend.md)**: Set up email sending
- **[Configure Trigger.dev](.cursor/commands/configure-trigger-dev.md)**: Set up background jobs and scheduled tasks

### UX/UI Guidelines
- **[UX Principles](.cursor/rules/dont-make-me-think.mdc)**: Understanding user behavior
- **[Design System](.cursor/rules/use-design-system.mdc)**: Using design system components
- **[Review Checklist](.cursor/rules/review-ui-ux.mdc)**: Quality assurance checklist

### Technical Guidelines
- **[Next.js Documentation](https://nextjs.org/docs)**: Check Next.js docs via next-devtools MCP server (`nextjs_docs`) for technical recommendations
- **[Web Interface Guidelines](.cursor/rules/web-interface-guidelines.mdc)**: Implementation guidance
- **[Postgres SQL Style](.cursor/rules/postgres-sql-style-guide.mdc)**: Database code style
- **[Create Migrations](.cursor/rules/create-migration.mdc)**: Database migration guidelines
- **[RLS Policies](.cursor/rules/create-rls-policies.mdc)**: Security policies
- **[Supabase Edge Functions](.cursor/rules/writing-supabase-edge-functions.mdc)**: Server functions
- **[Supabase Realtime](.cursor/rules/use-realtime.mdc)**: Real-time features



