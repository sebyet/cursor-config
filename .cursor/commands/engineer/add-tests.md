# Add Tests

Adds tests for your code so you can make sure it works correctly. Creates tests for functions, components, and features to catch problems before they happen.

1. **Understand what to test**
   - Ask what code needs tests (or detect from context)
   - Identify functions, components, or features that need testing
   - Check if tests already exist
   - Tell the user what you'll test

2. **Write tests**
   - Write unit tests for functions and utilities
   - Write component tests for React components
   - Write integration tests for API routes and Server Actions
   - Write E2E tests for critical user journeys (if needed)
   - Follow testing best practices (AAA pattern, descriptive names)

3. **Run tests to verify**
   - Run the new tests to make sure they work
   - Fix any problems with the tests
   - Make sure all tests pass
   - Show test results

4. **Document tests**
   - Create `doc/` folder if it doesn't exist
   - Create file: `doc/tests-added-YYYY-MM-DD.md`
   - Document: what was tested, test types added, coverage improvements

## What to Tell the User

- Explain you're adding tests for their code
- Show what you're testing (functions, components, features)
- Write tests step by step
- Run tests to verify they work
- Tell them when tests are added and passing
- Document what was tested

## See Also

### Workflow
- **[Build](../build.md)**: Build features that need tests
- **[Test](../test.md)**: Main test command
- **[Run Tests](run-tests.md)**: Run all tests to check if everything works

### Testing
- **[Create Test Plan](../qa/create-test-plan.md)**: Create test plan before adding tests
- **[Write Test Cases](../qa/write-test-cases.md)**: Write test cases

### Guidelines
- **[Testing Guidelines](.cursor/rules/testing-guidelines.mdc)**: Testing best practices and patterns

