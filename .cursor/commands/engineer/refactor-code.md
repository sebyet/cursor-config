# Refactor Code

Improves your code without changing what it does. Makes code cleaner, easier to understand, and easier to maintain. Fixes code smells and removes duplication.

1. **Identify what to refactor**
   - Ask what code needs refactoring (or detect from context)
   - Check for code smells (long functions, duplicated code, magic numbers)
   - Check for technical debt
   - Tell the user what you found

2. **Run tests first (safety check)**
   - Run existing tests to make sure everything works
   - If tests fail, fix them first
   - Only refactor if tests pass (safety first!)

3. **Refactor code**
   - Extract repeated code into reusable functions
   - Break down long functions into smaller ones
   - Remove magic numbers and strings (replace with constants)
   - Simplify complex conditionals
   - Remove dead code (unused functions, variables)
   - Improve code organization
   - Make code more readable

4. **Verify refactoring worked**
   - Run tests again to make sure nothing broke
   - Check that code still works the same way
   - Fix any problems if tests fail
   - Don't proceed until all tests pass

5. **Document refactoring**
   - Create `doc/` folder if it doesn't exist
   - Create file: `doc/refactor-YYYY-MM-DD.md`
   - Document: what was refactored, why, improvements made

## What to Tell the User

- Explain you're improving the code without changing what it does
- Show what code smells or problems you found
- Run tests first to make sure it's safe to refactor
- Refactor step by step, explaining what you're doing
- Run tests after refactoring to make sure nothing broke
- Tell them when refactoring is complete
- Document what was improved

## See Also

### Workflow
- **[Maintain](maintain.md)**: Advanced maintenance command
- **[Test](../test.md)**: Test after refactoring
- **[Build](../build.md)**: Build improvements from refactoring
- **[Deploy](../deploy.md)**: Deploy refactored code

### Code Quality
- **[Run Tests](run-tests.md)**: Run tests before and after refactoring
- **[Code Review](code-review.md)**: Review code before refactoring
- **[Fix](../fix.md)**: Fix issues found during refactoring

### Guidelines
- **[Refactoring Guidelines](.cursor/rules/refactoring-guidelines.mdc)**: Refactoring best practices and patterns

