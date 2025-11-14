# Modify Feature

Modifies an existing feature in one go! Identifies the feature, understands what to change, modifies it, shows preview, and finishes it - all automatically. Just describe what feature to modify and what changes you want!

1. **Identify which feature to modify**
   - Search codebase for features (components, pages, sections)
   - Check `doc/` folder for feature documentation
   - List available features if needed
   - Ask user to specify which feature to modify
   - Show examples: "course preview modal", "hero section", "footer"

2. **Understand what to modify**
   - Ask what changes they want
   - Show examples: "Change button color to blue", "Add loading state", "Update text"
   - Help them describe it clearly
   - Ask clarifying questions if needed

3. **Check and setup automatically**
   - Check if project is ready (Git, dependencies)
   - Auto-setup anything that's missing
   - Create feature branch if needed
   - Don't ask - just do it!

4. **Quick validation** (30 seconds max)
   - Read feature documentation if exists (`doc/feature-*.md`)
   - Understand current implementation
   - If unclear: Ask 1 clarifying question about change/impact
   - Define modification scope: What exactly changes?
   - Quick feasibility check: Can we modify it? Any blockers?
   - Note UX considerations: States needed (empty, loading, error, success), mobile-first, accessibility basics
   - Proceed immediately - don't overthink!

5. **Modify it**
   - Find all files related to the feature
   - Make changes step by step
   - Show them what you're modifying
   - Ask for clarification if unclear
   
6. **Auto-preview**
   - Start the development server automatically (if not running)
   - Show them the preview URL
   - Tell them to check it out
   - Wait for their confirmation

7. **Auto-finish after confirmation**
   - Once they confirm it looks good
   - Automatically clean up code
   - Update feature documentation
   - Tell them when it's done!

8. **Update documentation automatically**
   - Find existing feature doc: `doc/feature-{feature-name}-*.md`
   - If exists: Add modification section with date, what changed, why, impact
   - If doesn't exist: Create new doc with modification details
   - Include implementation details and changes made
   - Extract feature name from context (lowercase with hyphens)

## What to Tell the User

- Start: "Which feature do you want to modify? Examples: 'course preview modal', 'hero section', 'footer'"
- If multiple features found: List them and ask to choose
- Ask what changes they want: "What do you want to change? Examples: 'Change button color to blue', 'Add loading state', 'Update text'"
- After identifying feature: "Found it! Current implementation: [brief summary]. What changes do you want?"
- After validation: "Got it! Modifying [feature]... [quick notes]"
- Modify step by step, explaining what you're doing
- While modifying: Mention key quality checks being applied (e.g., "Updating loading states...", "Making it mobile-responsive...")
- When done modifying: "I've modified your feature with quality checks applied! Let me start a preview for you..."
- Show them the URL (usually http://localhost:3000)
- Tell them to open it in their browser and check it out
- After they confirm it looks good: "Great! Let me finish everything up - cleaning and updating documentation..."
- When done: "Done! Your feature modification is ready! Here's what I changed: [list]. Documentation has been updated."

## See Also

### For New Features
- **[Add Feature](.cursor/commands/add-feature.md)**: Add completely new features from scratch
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



