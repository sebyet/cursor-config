# Add Feature

Does everything to add a new feature in one go! Plans it, builds it, shows you a preview, and finishes it - all automatically. Just describe what you want and confirm it looks good!

1. **Ask what they want**
   - Ask them what feature they want to add
   - Show examples of good descriptions
   - **If they mention login/auth:** Offer to scaffold login flow: "I can set up a complete login system for you! Would you like password-based auth, social auth (Google/GitHub), or both?"
   - Help them describe it clearly
   - Ask clarifying questions if needed

2. **MANDATORY: Refine and clarify the task** (REQUIRED - do not skip!)
   - **MUST** refine the user's description into a clear, complete picture
   - **MUST** ask clarifying questions until you have a clear understanding
   - **MUST** understand: What exactly needs to be built? Why? For whom?
   - **MUST** clarify: What's the problem being solved? What's the user value?
   - **MUST** define: What's the MVP scope? What's included/excluded?
   - **MUST** identify: Where does it fit in the app? What pages/components?
   - **MUST** understand: What are the key behaviors/interactions?
   - **MUST** clarify: Any specific design requirements? Any constraints?
   - **DO NOT** proceed to building until you have a clear, complete picture
   - Summarize your understanding back to the user for confirmation

3. **Check and setup automatically**
   - Check if project is ready (Git, dependencies)
   - Auto-setup anything that's missing
   - Create feature branch if needed
   - Don't ask - just do it!

4. **Quick validation** (30 seconds max)
   - Review the refined understanding from step 2
   - Define MVP scope: What's the simplest usable version?
   - Quick feasibility check: Can we build it? Any blockers?
   - Note UX considerations: States needed (empty, loading, error, success), mobile-first, accessibility basics
   - Proceed immediately - don't overthink!

5. **Build it**
   - **If login/auth feature:** 
     - Ask which flow: password-based, social auth, or both
       - Explain simply: "Do you want users to sign in with a password, or with Google/GitHub (like 'Sign in with Google'), or both?"
     - Run appropriate shadcn command: `pnpm dlx shadcn@latest add @supabase/password-based-auth-nextjs` or `@supabase/social-auth-nextjs`
     - Use Supabase MCP tools to apply auth database migration (explain: "I'm setting up the database to store user accounts")
     - Save migration SQL to `supabase/migrations/<timestamp>_login_flow.sql`
   - Translate their description into code
   - Build the feature step by step
   - Show them what you're building (explain: "I'm building your feature now - like assembling furniture from instructions")
   - Ask for clarification if unclear
   
6. **Auto-preview**
   - Start the development server automatically (explain: "I'm starting a preview server - this lets you see your feature before it's finished, like a preview of a blog post")
   - Show them the preview URL in the @browser
   - Tell them to check it out (explain: "You can see your feature here: [URL]. Open it in your browser - it's like opening a draft document to review it")
   - Wait for their confirmation

7. **Auto-finish after confirmation**
   - Once they confirm it looks good
   - Automatically clean up code (remove AI slop, fix formatting) - Explain: "I'm cleaning up the code - like proofreading and formatting a document"
   - **Run tests automatically** - Check for test files, run test suites, verify everything works (explain: "I'm testing everything to make sure it works - like testing all the buttons on a remote control")
   - **Add tests automatically** - If no tests exist for the feature, create test files with test cases for key functionality
   - Fix any test failures automatically (explain: "Found a small issue in testing - I'll fix it quickly!")
   - Tell them when it's done! (explain: "All done! Your feature is ready and tested!")

8. **Document automatically**
   - Create `doc/` folder if it doesn't exist
   - Create file: `doc/feature-{feature-name}-YYYY-MM-DD.md`
   - Document: what feature was added, why, when, how, impact, notes
   - Include implementation details and changes made
   - Extract feature name from context (lowercase with hyphens)

## What to Tell the User

**First time users:**
- "Hi! I can help you build features. You don't need to know how to code - just tell me what you want in plain English! For example: 'Add a blue button that says Sign Up' or 'Create a contact form with name, email, and message fields'. I'll handle all the technical stuff automatically."

**Regular users:**
- Ask them what feature they want to add
- Show examples: "Like 'Add a blue button that says Sign Up' or 'Create a contact form with name, email, and message fields'"
- **MUST refine and clarify**: Ask questions until you have a complete, clear picture
- **MUST understand**: What exactly? Why? For whom? Where? How should it work?
- **MUST confirm**: Summarize your understanding and get confirmation before proceeding

**During building:**
- After refinement and confirmation: "Got it! I have a clear picture now. I'm building your feature..."
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

