# Run Tests

Runs all your tests to make sure everything still works. Checks if your code is working correctly and finds any problems before you go live.

1. **Check if tests exist**
   - Check if test files exist in the project
   - Check if testing tools are set up (Jest, Vitest, etc.)
   - Tell the user what you found

2. **Run tests**
   - Run unit tests (fast tests for individual functions)
   - Run integration tests (tests for how parts work together)
   - Run E2E tests if they exist (tests that check the whole app)
   - Show test results and any failures
   - Tell the user what passed and what failed

3. **Fix test failures (if any)**
   - If tests fail, explain what went wrong
   - Fix the problems in the code
   - Run tests again to make sure everything passes
   - Don't proceed until all tests pass

4. **Show test summary**
   - Show how many tests passed
   - Show test coverage if available
   - Tell them if everything is working correctly

## What to Tell the User

- Explain you're running tests to check if everything works
- Show which tests you're running (unit, integration, E2E)
- Show test results as they run
- If tests pass: "All tests passed! Your code is working correctly."
- If tests fail: Explain what failed and fix it
- Show test summary when done

## See Also

### Workflow
- **[Build](../build.md)**: Build features before testing
- **[Deploy](../deploy.md)**: Deploy after tests pass
- **[Fix](../fix.md)**: Fix issues found during testing
- **[Test](../test.md)**: Main test command

### Testing
- **[Add Tests](add-tests.md)**: Add tests for new or existing code
- **[Create Test Plan](../qa/create-test-plan.md)**: Create test plan
- **[Write Test Cases](../qa/write-test-cases.md)**: Write test cases

### Guidelines
- **[Testing Guidelines](.cursor/rules/testing-guidelines.mdc)**: Testing best practices

