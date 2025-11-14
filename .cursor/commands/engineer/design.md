# Design

**Advanced command** for explicit design work. For most users, design (accessibility, design system) happens automatically during `@build` and `@setup` workflows.

**In plain English:** Want to explicitly customize design or check accessibility? This is for advanced users who want explicit control over design work.

## When to Use This Command

**Most users don't need this command** - design happens automatically:
- ✅ `@build` → Automatically checks design and accessibility
- ✅ `@setup` → Automatically customizes design system for new projects

**Use this command when:**
- You're an advanced user who wants explicit control over design
- You want to customize design system outside of setup
- You want to run accessibility audits manually
- You're doing design work outside of normal workflows

## What This Command Does

**For advanced users:** This provides explicit control over design work. I'll:
- Check accessibility (if requested)
- Help customize colors, fonts, and styles
- Make sure everything looks consistent
- Check if the code matches your design

**Examples of what you can say:**
- "Check if it's easy to use"
- "Change the colors"
- "Make it easier to read"
- "Check if it matches the design"

## How It Works

1. **You tell me what you want**
   - "Customize design system" = change colors, fonts, styles
   - "Change the colors" = customize design system
   - "Make it easier to read" = customize design system

2. **I do the work automatically**
   - **I automatically check accessibility** (happens invisibly - you don't need to ask)
   - I customize what you asked for
   - I look for problems
   - I suggest improvements

3. **I tell you the results**
   - I show you what I found or changed
   - I tell you if anything needs fixing (including accessibility issues found automatically)
   - I suggest what to do next

## Usage Examples

**Simple:**
- `@design` → "Change the colors"
- `@design` → "Make it easier to read"
- `@design` → "Customize the design"

**Specific:**
- `@design` → "Change the colors to blue"
- `@design` → "Update fonts and spacing"
- `@design` → "Make it match my brand colors"

**Note:** Accessibility is checked automatically - you don't need to ask for it!

## What to Tell the User

**First time users:**
- "Hi! I can help you customize your design - colors, fonts, and styles. I'll also automatically check that everything is accessible (easy for everyone to use) while I work.
  
  What would you like to customize?"

**When working:**
- "Customizing your design..."
- "Checking accessibility automatically..." (only mention if issues found)
- "Everything looks good!" or "Found some issues: [list in simple terms, including accessibility if found]"

**Results:**
- "Design customized! Here's what changed: [list]"
- "I also checked accessibility automatically - everything looks good!" (only mention if checked)
- "Found [X] issues (including [X] accessibility issues). Would you like me to fix them?"

## Specialist Commands Used

- **[Accessibility Audit](design/accessibility-audit.md)** - Check accessibility (used automatically)
- **[Customize Design System](design/customize-design-system.md)** - Customize design system

## See Also

- **[Build](build.md)**: Build features before designing
- **[Deploy](deploy.md)**: Deploy after design changes
- **[Fix](fix.md)**: Fix design issues
- **[Test](test.md)**: Test design implementations

