# Fix Everything

Intelligently checks what's wrong and fixes only the problems that exist. Think of it as a smart "fix everything" button that only fixes what needs fixing!

1. **Check what's wrong first**
   - Look for code errors (compilation errors)
   - Check for bugs (things not working)
   - Check Git status (saving/upload issues)
   - Check code quality (formatting/style issues)
   - Check test status (failing tests)
   - Tell the user what you found

2. **Fix only what needs fixing**
   - **If code errors exist:** Use `fix-compile-errors.md` approach - fix all compilation errors
   - **If bugs exist:** Use `debug-issue.md` approach - find and fix bugs
   - **If Git issues exist:** Use `fix-git-issues.md` approach - resolve Git problems
   - **If code quality issues:** Use `lint-fix.md` approach - clean up formatting

3. **Verify everything works**
   - Run tests to confirm fixes worked
   - Make sure nothing broke
   - Confirm everything is working

## What to Tell the User

- Explain you're checking what's wrong first
- List what problems you found (don't fix things that aren't broken!)
- Fix only the problems that exist
- Skip steps that aren't needed (e.g., "No Git issues found, skipping Git fixes")
- Show what you're fixing
- Test that everything works
- Tell them when it's all fixed!