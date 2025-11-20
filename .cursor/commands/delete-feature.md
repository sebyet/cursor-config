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

3. **MANDATORY: Refine and clarify the task** (REQUIRED - do not skip!)
   - **MUST** refine the user's request into a clear, complete picture
   - **MUST** ask clarifying questions until you have a clear understanding
   - **MUST** understand: What exactly needs to be deleted? Why?
   - **MUST** clarify: Is it the entire feature or just parts? Any exceptions?
   - **MUST** identify: What files/components are involved?
   - **MUST** understand: What's the impact? What breaks? What stays?
   - **MUST** check: Are there dependencies? What else uses this feature?
   - **MUST** clarify: Should related data/docs/tests also be deleted?
   - **MUST** confirm: Is this a permanent deletion or should it be archived?
   - **DO NOT** proceed to deleting until you have a clear, complete picture
   - Summarize your understanding back to the user for confirmation

4. **Check and setup automatically**
   - Check if project is ready (Git, dependencies)
   - Auto-setup anything that's missing
   - Create feature branch if needed
   - Don't ask - just do it!

5. **Quick validation** (30 seconds max)
   - Read feature documentation if exists (`doc/feature-*.md`)
   - Understand current implementation
   - Review the refined understanding from step 3
   - Find all related files (components, pages, tests, docs)
   - Check dependencies: What uses this feature?
   - Identify impact: What breaks if deleted?
   - If risky: Ask 1 clarifying question about confirmation
   - Proceed immediately - don't overthink!

6. **Delete it safely**
   - Delete feature files (components, pages, etc.)
   - Remove imports from files that use it
   - Clean up references in other files
   - Update parent components/pages if needed
   - Remove or update routes if needed
   - Delete test files related to feature
   - Show what you're deleting
   - Ask for clarification if unclear

7. **Verify nothing broke**
   - Check for broken imports
   - Check for broken references
   - Check for broken routes
   - Fix any issues automatically
   - Run build check if needed

8. **Auto-preview**
   - Start the development server automatically (if not running)
   - Show them the preview URL
   - Tell them to check it out
   - Wait for their confirmation

9. **Auto-finish after confirmation**
   - Once they confirm it looks good
   - Automatically clean up code
   - Update or remove feature documentation
   - Tell them when it's done!

10. **Update documentation automatically**
   - Find existing feature doc: `doc/feature-{feature-name}-*.md`
   - If exists: Add deletion section with date, why deleted, impact
   - Or mark as deprecated/deleted
   - Include what was removed and why

## What to Tell the User

- Start: "Which feature do you want to delete? Examples: 'course preview modal', 'hero section', 'footer'"
- If multiple features found: List them and ask to choose
- After identifying feature: "Found it! This feature is used in: [list]. Deleting it will: [impact]."
- **MUST refine and clarify**: Ask questions until you have a complete, clear picture
- **MUST understand**: What exactly gets deleted? Why? What's the impact? Any exceptions?
- **MUST confirm**: Summarize your understanding and get confirmation before proceeding
- If risky: "Warning: This feature is used in [X places]. Deleting it will remove [functionality]. Are you sure?"
- After refinement and confirmation: "Got it! I have a clear picture now. Deleting [feature]... [quick notes]"
- Delete step by step, explaining what you're removing
- When done deleting: "I've deleted your feature and cleaned up references! Let me verify nothing broke..."
- After verification: "Verified! Nothing broke. Let me start a preview for you..."
- Show them the URL (usually http://localhost:3000)
- Tell them to open it in their browser and check it out
- After they confirm it looks good: "Great! Let me finish everything up - cleaning and updating documentation..."
- When done: "Done! Feature deleted successfully! Here's what I removed: [list]. Documentation has been updated."



