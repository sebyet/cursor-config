# Code Review

Reviews your code for quality, maintainability, and best practices. Checks code style, finds potential bugs, suggests improvements, and makes sure your code is clean and easy to understand.


1. **Review code quality**
   - Check code style and formatting
   - Check for code smells (duplicated code, long functions)
   - Check for potential bugs
   - Check for best practices
   - Check error handling
   - Check performance issues
   - Check documentation
   - Tell the user what you found

2. **Suggest improvements**
   - Fix code style issues
   - Refactor duplicated code
   - Break down long functions
   - Fix potential bugs
   - Apply best practices
   - Improve error handling
   - Optimize performance
   - Add missing documentation

3. **Verify improvements**
   - Make sure code still works
   - **Run tests:** Use `run-tests.md` approach - run tests to confirm nothing broke
   - Confirm code is cleaner and better

4. **Document code review**
   - Create `doc/` folder if it doesn't exist
   - Create file: `doc/code-review-YYYY-MM-DD.md`
   - Document: issues found, improvements made, code quality status

## What to Tell the User

- Explain you're reviewing code quality
- List what you're checking (e.g., "Checking code style, potential bugs, and best practices...")
- If you find problems, explain them clearly and fix them
- Show progress of each check
- Tell them when code review passes
- Document all checks and improvements for the project history

## See Also

### Workflow
- **[Test](../test.md)**: Main test command
- **[Build](../build.md)**: Build features before review
- **[Deploy](../deploy.md)**: Deploy after review
- **[Maintain](maintain.md)**: Advanced maintenance (optional - maintenance happens automatically)

### Code Quality
- **[Run Tests](run-tests.md)**: Run tests to verify code still works
- **[Refactor Code](refactor-code.md)**: Refactor code for better quality
- **[Fix](../fix.md)**: Fix issues found during review