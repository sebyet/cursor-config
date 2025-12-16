# Implement Feature

Write the code.

## Use Case

Implement a feature or task by writing code, creating configurations, and handling any necessary migrations.

## Process

### 1. Feature Implementation
- Write code following design specifications
- Follow project coding standards and patterns
- Implement error handling
- Add logging where appropriate
- Write clean, maintainable code

### 2. Configurations
- Update configuration files if needed
- Add environment variables if required
- Update build/deployment configs
- Document configuration changes
- Ensure configs are environment-aware

### 3. Migrations
- Create database migrations if needed
- Plan migration rollback strategy
- Test migrations on sample data
- Document migration steps
- Consider data migration scripts

### 4. Code Quality
- Follow linting rules
- Ensure proper formatting
- Add comments for complex logic
- Keep functions focused and small
- Maintain consistency with codebase

## Output Format

### Implementation Output
- **Code Changes**: Files modified/created
- **Config Changes**: Configuration updates
- **Migrations**: Database or data migrations
- **Dependencies**: New dependencies added

## Best Practices

### Code Implementation
- **Follow patterns**: Use established project patterns
- **Keep it simple**: Don't over-complicate
- **Error handling**: Handle errors gracefully
- **Logging**: Add appropriate logging
- **Documentation**: Comment complex logic

### Configurations
- **Environment-aware**: Don't hardcode values
- **Document defaults**: Clear default values
- **Validate configs**: Check config validity
- **Version control**: Track config changes

### Migrations
- **Test first**: Test on sample data
- **Rollback plan**: Always have rollback strategy
- **Idempotent**: Migrations should be safe to rerun
- **Document**: Clear migration documentation

## Related Commands

- Before implementation: Use `/plan-work` to understand task breakdown
- After implementation: Use `/run-and-check` to verify it works
- For testing: Use `/add-tests` to add test coverage

## Common Scenarios

### Database Changes
1. Create migration script
2. Test migration on sample data
3. Plan rollback strategy
4. Document migration steps

### New Dependencies
1. Add to package.json
2. Update lock file
3. Document why dependency is needed
4. Check for security vulnerabilities

## Safety Checks

- ✅ Code follows project standards
- ✅ Configurations are environment-aware
- ✅ Migrations are tested and reversible
- ✅ Error handling is in place

Clean implementation makes maintenance easier and reduces bugs.
