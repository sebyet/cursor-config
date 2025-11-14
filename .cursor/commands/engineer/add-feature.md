# Add Feature

Does everything to add a new feature in one go! Plans it, builds it, shows you a preview, and finishes it - all automatically. Just describe what you want and confirm it looks good!

1. **Ask what they want**
   - Ask them what feature they want to add
   - Show examples of good descriptions
   - Help them describe it clearly
   - Ask clarifying questions if needed

2. **Check and setup automatically**
   - Check if project is ready (Git, dependencies)
   - Auto-setup anything that's missing
   - Create feature branch if needed
   - Don't ask - just do it!

2.5. **Quick validation** (30 seconds max)
   - If unclear: Ask 1 clarifying question about problem/user value
   - Define MVP scope: What's the simplest usable version?
   - Quick feasibility check: Can we build it? Any blockers?
   - Note UX considerations: States needed (empty, loading, error, success), mobile-first, accessibility basics
   - Proceed immediately - don't overthink!

3. **Build it**
   - Translate their description into code
   - Build the feature step by step
   - Show them what you're building
   - Ask for clarification if unclear
   
4. **Auto-preview**
   - Start the development server automatically
   - Show them the preview URL in the @browser
   - Tell them to check it out
   - Wait for their confirmation

5. **Auto-finish after confirmation**
   - Once they confirm it looks good
   - Automatically clean up code
   - **Run tests** - Use `run-tests.md` approach to verify everything works
   - **Add tests** - Use `add-tests.md` approach to add tests for the new feature
   - Tell them when it's done!

6. **Document automatically**
   - Create `doc/` folder if it doesn't exist
   - Create file: `doc/feature-{feature-name}-YYYY-MM-DD.md`
   - Document: what feature was added, why, when, how, impact, notes
   - Include implementation details and changes made
   - Extract feature name from context (lowercase with hyphens)

## What to Tell the User

**First time users:**
- "Hi! I can help you build features. Just tell me what you want to add or change in plain English. For example: 'Add a blue button that says Sign Up' or 'Create a contact form with name, email, and message fields'."

**Regular users:**
- Ask them what feature they want to add
- Show examples: "Like 'Add a blue button that says Sign Up' or 'Create a contact form with name, email, and message fields'"
- If description is unclear, ask 1 quick clarifying question about problem/user value (in plain English)

**During building:**
- After validation: "Got it! I'm building your feature now..."
- Build it step by step, explaining what you're doing in simple terms
- While building: Mention key quality checks being applied in plain English (e.g., "Adding loading states...", "Making it work on phones...", "Making sure it's accessible...")
- **Automatically check design and accessibility** (happens invisibly - only mention if issues found)
- When done building: "I've built your feature! Let me show you a preview..."

**Preview:**
- "Starting a preview server..." (don't explain what this means - just do it)
- Show them the URL (usually http://localhost:3000)
- "You can see your feature here: [URL]. Open it in your browser and check it out!"
- "Does this look good? If yes, I'll finish everything up automatically."

**After confirmation:**
- "Great! Let me finish everything up - cleaning up, testing, checking design, and documenting..."
- When done: "Done! Your feature is ready! Here's what I built: [list in plain English]. Everything has been tested, checked for accessibility, and documented."

## See Also

### Workflow
- **[Test](../test.md)**: Test the feature after building
- **[Deploy](../deploy.md)**: Deploy the feature after testing
- **[Fix](../fix.md)**: Fix issues found during building

### Planning
- **[Brainstorm Feature](../product/brainstorm-feature.md)**: Deep analysis and planning for complex features
- **[Create PRD](../product/create-prd.md)**: Create PRD before building
- **[Define User Story](../product/define-user-story.md)**: Create user stories

### Design
- **[Design](design.md)**: Advanced design work (optional - design happens automatically)
- **[Create Design Spec](../design/create-design-spec.md)**: Create design specifications
- **[Review Design Implementation](../design/review-design-implementation.md)**: Review implementation

### Testing & Quality
- **[Run Tests](run-tests.md)**: Run tests to verify everything works
- **[Add Tests](add-tests.md)**: Add tests for new features
- **[Create Test Plan](../qa/create-test-plan.md)**: Create test plan for feature

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

