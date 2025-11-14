# Contract Test

Perform API contract testing to ensure API compatibility and prevent breaking changes.

## What This Command Does

Performs contract testing by:
- Creating API contracts (OpenAPI, GraphQL schemas)
- Testing API compatibility
- Detecting breaking changes
- Validating request/response schemas
- Generating contract documentation

## How It Works

1. **Understand Contract Testing Needs**
   - Ask about API contracts
   - Identify APIs to test
   - Understand versioning strategy
   - Determine test scope

2. **Design Contract Tests**
   - Create or extract contracts
   - Set up contract validation
   - Define compatibility rules
   - Plan test execution

3. **Execute and Analyze**
   - Run contract tests
   - Validate schemas
   - Detect breaking changes
   - Generate reports

## What to Tell the User

- "What APIs should we test? (REST, GraphQL, etc.)"
- "What contract format are you using? (OpenAPI, GraphQL schema, etc.)"
- Execute contract tests and analyze results
- "Contract test complete! APIs tested: [count]. Breaking changes: [list]. Compatibility: [status]"

## See Also

- **[Write Test Cases](write-test-cases.md)**: Create test cases
- **[API Versioning](../engineer/api-versioning.md)**: API versioning strategy
- **[Write API Docs](../engineer/write-api-docs.md)**: API documentation

