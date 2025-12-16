# Next Step

**In plain English:** Analyzes your plans folder to identify what's been completed and what the next step should be in your implementation plan.

## What This Command Does

This command helps you track progress through your implementation plans by:

1. **Analyzing plan files** - Reads all plan files in `.cursor/plans/` directory
2. **Checking implementation status** - Examines the codebase to see what's been implemented
3. **Identifying next step** - Determines which step should be worked on next
4. **Providing context** - Shows what's been done and what needs to be done

## How It Works

1. **Scan plans folder**
   - Find all plan files (`.md` files in `.cursor/plans/`)
   - Parse plan structure (Pre-Step, Step 1, Step 2, etc.)
   - Read frontmatter metadata (name, overview, todos)

2. **Analyze codebase**
   - Check for database tables/schema (via Supabase MCP or codebase search)
   - Look for authentication pages and flows
   - Check for feature implementations matching plan steps
   - Verify environment setup and configuration

3. **Determine completion status**
   - Compare plan requirements with actual implementation
   - Identify which steps are complete, in progress, or not started
   - Find the first incomplete step

4. **Report next step**
   - Display the next step to work on
   - Show acceptance criteria for that step
   - Provide context about what needs to be done
   - Suggest implementation approach if helpful

## Usage

Simply say:
- `@next-step` - "What's the next step in our plan?"
- `@next-step` - "Show me what we need to do next"
- `@next-step` - "Where are we in the plan?"

## Output Format

The command will provide:

1. **Plan Overview**
   - Plan name and description
   - Total steps in the plan

2. **Progress Summary**
   - Completed steps (with checkmarks)
   - Current/next step (highlighted)
   - Remaining steps (listed)

3. **Next Step Details**
   - Step number and title
   - Description
   - User story (if applicable)
   - Acceptance criteria
   - Implementation guidance

4. **Implementation Suggestions**
   - What needs to be created/configured
   - Relevant files or components
   - Database changes needed
   - Any dependencies on other steps

## Example Output

```
📋 Plan: Cycling Social App Flow

Progress: 0/14 steps completed

✅ Pre-Step: System Configuration & Environment Setup
   Status: Not started
   Next: Create database schema and RLS policies

📝 Step 1: User Registration
   Status: Not started
   Next: After Pre-Step is complete

...

🎯 NEXT STEP: Pre-Step - System Configuration & Environment Setup

Description:
Before any user interactions, the system must be configured with database 
schema, authentication service, and necessary infrastructure.

What needs to be done:
- Create database tables (profiles, rides, ride_rsvps, messages, conversations, 
  notifications, ride_feedback)
- Set up RLS policies for all tables
- Create database indexes
- Verify environment variables

Acceptance Criteria:
- Database schema is created and migrations are applied
- Authentication is enabled and configured
- RLS policies are active and tested
- Environment variables are properly set
- Database indexes are created for performance

Implementation:
1. Use Supabase MCP tools to create tables
2. Save migration SQL to supabase/migrations/
3. Set up RLS policies
4. Create indexes for performance
```

## Analysis Logic

### For Pre-Step (System Configuration):
- Check if database tables exist (via Supabase MCP `list_tables`)
- Check for migration files in `supabase/migrations/`
- Verify environment variables are set
- Check for RLS policies

### For Authentication Steps:
- Check for login/register pages (`app/login`, `app/register`, `app/auth/*`)
- Look for authentication components
- Verify Supabase auth configuration
- Check middleware for route protection

### For Feature Steps:
- Search for relevant pages/routes
- Check for components matching the feature
- Look for database queries/operations
- Verify API routes or server actions

### For UI/Flow Steps:
- Check for page components
- Look for form components
- Verify navigation/routing
- Check for related database operations

## Integration with Other Commands

- **After identifying next step:**
  - If it's a feature → Suggest using `@add-feature`
  - If it's database setup → Use Supabase MCP tools directly
  - If it's configuration → Use `@setup-project` or manual setup
  - If it's a bug/issue → Use `@fix-issues`

## What to Tell the User

**When starting:**
- "Let me analyze your plans and check what's been implemented to find the next step..."

**When analyzing:**
- "I found [X] plan(s) in your plans folder. Let me check the implementation status..."
- "Checking database schema..."
- "Checking for authentication pages..."
- "Verifying feature implementations..."

**When reporting:**
- "Here's your progress and the next step:"
- "**Next Step:** [Step name]"
- "**Status:** [Not started / In progress / Complete]"
- "**What to do:** [Clear action items]"

**If no plans found:**
- "I don't see any plan files in `.cursor/plans/`. Would you like to create a plan using `@plan-app-flow`?"

**If all steps complete:**
- "🎉 Congratulations! All steps in your plan are complete. Would you like to test the app with `@test-app` or deploy with `@go-live`?"

## Technical Implementation Notes

- Use `glob_file_search` to find plan files
- Use `read_file` to parse plan structure
- Use `codebase_search` to check for implementations
- Use Supabase MCP tools (`list_tables`, `list_migrations`) to check database state
- Use `grep` to find specific patterns (routes, components, etc.)
- Parse markdown to extract step information and acceptance criteria

## See Also

- **[Plan App Flow](plan-app-flow.md)**: Generate new plans
- **[Add Feature](add-feature.md)**: Implement features from plans
- **[Test App](test-app.md)**: Test completed features
- **[Go Live](go-live.md)**: Deploy completed app

