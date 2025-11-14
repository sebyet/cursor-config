# Recommend Command

**In plain English:** Not sure which command to use? Just describe what you want to do, and I'll recommend the best command(s) for your task.

## What This Command Does

This command analyzes your request and recommends the most appropriate command(s) from your command set. It helps you:
- Find the right command when you're not sure
- Discover commands you might not know about
- Understand which commands work together
- Get started quickly without memorizing all commands

**Examples of what you can say:**
- "I want to add a new feature"
- "How do I test my code?"
- "I need to fix a bug"
- "I want to understand my users better"
- "How do I deploy to production?"
- "I need to optimize performance"

## How It Works

1. **You describe what you want to do**
   - Just tell me in plain English what you're trying to accomplish
   - Examples: "Add a feature", "Fix a bug", "Test my app", "Deploy to production"

2. **I analyze your request**
   - I understand your intent and goals
   - I match it to relevant commands from your command set
   - I consider the context and complexity

3. **I recommend the best command(s)**
   - I suggest the most appropriate command(s) for your task
   - I explain why each command is recommended
   - I provide examples of how to use them
   - I suggest related commands that might help

4. **You use the recommended command**
   - Follow my recommendation
   - Or ask for alternatives if needed

## Usage Examples

**Simple requests:**
- `@recommend-command` → "I want to add a new feature"
  - **Recommended:** `@build` → "Add a contact form"
  - **Why:** The @build command automatically handles feature development end-to-end

- `@recommend-command` → "Something is broken"
  - **Recommended:** `@fix` → "The button doesn't work"
  - **Why:** The @fix command intelligently diagnoses and fixes issues

**Complex requests:**
- `@recommend-command` → "I want to understand my users and then build a feature for them"
  - **Recommended:** 
    1. `@ux/create-persona` - First understand your users
    2. `@ux/create-user-journey` - Map their experience
    3. `@build` → "Build the feature based on the research"
  - **Why:** User research should come before building to ensure you're solving the right problem

- `@recommend-command` → "I want to optimize my app's performance and security"
  - **Recommended:**
    1. `@devops/check-performance` - Check and optimize performance
    2. `@devops/check-security` - Security audit and fixes
  - **Why:** These are specialized commands for performance and security optimization

**Discovery requests:**
- `@recommend-command` → "What commands are available for testing?"
  - **Recommended:**
    - `@test` - Main testing command (for non-technical users)
    - `@engineer/add-tests` - Add tests for features
    - `@engineer/run-tests` - Run test suites
    - `@qa/create-test-plan` - Generate test plans
    - `@qa/write-test-cases` - Create test cases
    - `@qa/test-accessibility` - Accessibility testing
    - `@qa/test-cross-browser` - Cross-browser testing

## Command Recommendation Logic

### For Non-Technical Users (Start Here!)

I prioritize the **5 key commands** that work in plain English:

1. **`@setup`** - When you need to:
   - Set up a new project
   - Configure an existing project
   - Set up design systems

2. **`@build`** - When you need to:
   - Add new features
   - Modify existing features
   - Remove features
   - Plan features (routes to product commands)

3. **`@test`** - When you need to:
   - Test your code
   - Check if everything works
   - Run test suites
   - Add tests

4. **`@deploy`** - When you need to:
   - Publish to preview
   - Deploy to production
   - Create pull requests

5. **`@fix`** - When you need to:
   - Fix bugs
   - Fix broken features
   - Fix compilation errors
   - Fix Git issues

### For Power Users (Direct Access)

When you know what you need, I recommend specific role-based commands:

**Engineering:**
- `@engineer/add-feature` - Build new features end-to-end
- `@engineer/modify-feature` - Update existing features
- `@engineer/refactor-code` - Refactor code safely
- `@engineer/code-review` - Review code for quality
- `@engineer/database-migration` - Create database migrations
- And many more...

**Product:**
- `@product/brainstorm-feature` - Brainstorm and evaluate features
- `@product/create-prd` - Create product requirement documents
- `@product/prioritize-features` - Prioritize features
- `@product/analyze-analytics` - Interpret analytics data

**UX:**
- `@ux/create-persona` - Generate user personas
- `@ux/create-user-journey` - Map user journeys
- `@ux/conduct-usability-test` - Conduct usability testing
- `@ux/analyze-user-feedback` - Synthesize user feedback

**Design:**
- `@design/create-wireframes` - Create wireframes
- `@design/customize-design-system` - Customize design systems
- `@design/accessibility-audit` - Audit accessibility

**DevOps:**
- `@devops/check-performance` - Check and optimize performance
- `@devops/check-security` - Security audit
- `@devops/setup-monitoring` - Configure monitoring
- `@devops/setup-ci-cd` - Configure CI/CD

**QA:**
- `@qa/create-test-plan` - Generate test plans
- `@qa/write-test-cases` - Create test cases
- `@qa/report-bug` - Generate bug reports

**Growth:**
- `@growth/optimize-seo` - SEO optimization
- `@growth/analyze-conversion` - Analyze conversion funnels
- `@growth/setup-ab-test` - Set up A/B tests

## What to Tell the User

**First time users:**
- "Hi! I can help you find the right command. Just describe what you want to do in plain English. For example: 'I want to add a feature' or 'How do I test my code?'"

**When analyzing:**
- "Let me analyze your request and find the best command(s) for you..."
- "Based on what you described, here are my recommendations..."

**When recommending:**
- "**Recommended:** `@command-name` → 'Your specific request'"
- "**Why:** [Clear explanation of why this command fits]"
- "**Alternative:** If you prefer direct access, you can use `@role/specific-command`"
- "**Related commands:** You might also want to use [related commands]"

**For complex tasks:**
- "For this task, I recommend a sequence:"
  1. "First, use `@command1` to [purpose]"
  2. "Then, use `@command2` to [purpose]"
  3. "Finally, use `@command3` to [purpose]"

**When multiple options exist:**
- "I found several options. Here's the best one for your situation:"
- "**Best for beginners:** `@simple-command`"
- "**Best for power users:** `@advanced-command`"
- "**Best for this specific case:** `@specific-command`"

## Command Matching Patterns

I match requests to commands based on:

**Intent keywords:**
- "add", "create", "build", "implement" → `@build` or `@engineer/add-feature`
- "fix", "broken", "error", "bug" → `@fix` or `@engineer/fix-everything`
- "test", "check", "verify" → `@test` or `@engineer/run-tests`
- "deploy", "publish", "release" → `@deploy` or `@engineer/publish-production`
- "setup", "configure", "initialize" → `@setup` or `@engineer/setup-new-project`

**Domain keywords:**
- "user", "persona", "journey" → UX commands
- "design", "wireframe", "component" → Design commands
- "performance", "speed", "optimize" → DevOps performance commands
- "security", "vulnerability", "audit" → DevOps security commands
- "analytics", "metrics", "conversion" → Product/Growth commands
- "database", "migration", "query" → Engineering database commands

**Complexity indicators:**
- Simple requests → Key commands (`@build`, `@fix`, etc.)
- Specific technical needs → Role-based commands
- Multi-step tasks → Sequence of commands

## See Also

- **[Commands Reference](COMMANDS-REFERENCE.md)**: Complete list of all commands organized by purpose
- **[Build](build.md)**: Build features
- **[Fix](fix.md)**: Fix problems
- **[Test](test.md)**: Test and quality
- **[Deploy](deploy.md)**: Deploy and publish
- **[Setup](setup.md)**: Set up projects

