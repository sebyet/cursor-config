# Deploy

**In plain English:** Want to publish your work online? I'll make sure everything is safe and working, then publish it for you.

## What This Command Does

**For non-technical users:** This publishes your work to the internet so others can see it. I'll:
- Make sure everything is safe and working
- Publish it to a test version (preview) or the real website (live)
- Give you a link so you can see it

**What's the difference?**
- **Preview**: A test version only you can see (safe to experiment)
- **Live website**: The real website everyone sees (be careful!)

**Tip:** Always use preview first to test things!

## How It Works

1. **You tell me where to publish**
   - "Preview" = test version (safe)
   - "Live" or "Production" = real website (everyone sees it)
   - "Both" = preview first, then live after you approve

2. **I check everything is safe**
   - I test that everything works
   - I check for security issues
   - I check that it loads fast
   - I check that it's accessible
   - I only publish if everything passes

3. **I publish it**
   - I publish to the right place
   - I create any needed requests (don't worry about this - I handle it)
   - I give you a link to see it

4. **Done!**
   - Your work is live!
   - I give you the link
   - I document what was published

## Usage Examples

**Preview (safe to test):**
- `@deploy` → "Publish a preview"
- `@deploy` → "Show me a test version"

**Live website (everyone sees it):**
- `@deploy` → "Publish to the live website"
- `@deploy` → "Make it live"

**Both (recommended):**
- `@deploy` → "Create a preview first, then publish to live if it looks good"

## What to Tell the User

**First time users:**
- "Hi! I can help you publish your work online. You can publish to:
  - **Preview**: A test version only you can see (safe to experiment)
  - **Live website**: The real website everyone sees (be careful!)
  
  Which would you like? (I recommend preview first to test things)"

**When checking:**
- "Let me check that everything is safe and working..."
- "Checking security..."
- "Checking performance..."
- "Everything looks good! Ready to publish."

**If checks fail:**
- "I found some issues that need to be fixed first: [list in simple terms]"
- "Let me fix these, then we can publish."

**When publishing:**
- "Publishing to [preview/live website]..."
- "Published! Your site is live at [URL]"
- "You can see it here: [link]"

## Specialist Commands Used

- **[Publish Feature](engineer/publish-feature.md)** - Create previews
- **[Publish Production](engineer/publish-production.md)** - Deploy to live website
- **[Create PR](engineer/create-pr.md)** - Create approval requests
- **[Check Security](devops/check-security.md)** - Security checks
- **[Check Performance](devops/check-performance.md)** - Performance checks
- **[Accessibility Audit](design/accessibility-audit.md)** - Accessibility checks

## See Also

- **[Build](build.md)**: Build features before deploying
- **[Test](test.md)**: Test before deploying
- **[Fix](fix.md)**: Fix issues before deploying
- **[Maintain](engineer/maintain.md)**: Advanced maintenance (optional - maintenance happens automatically)

