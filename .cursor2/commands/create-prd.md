# Create Product Requirement Document

Creates a comprehensive Product Requirement Document (PRD) from an initial idea. Refines the idea through strategic questions, then breaks it down into major steps and features to guide development.

1. **Capture the Initial Idea**
   - Ask the user to describe their product idea
   - Listen to their description
   - Take notes on key points
   - Ask for clarification if the idea is too vague

2. **Refine the Idea Through Strategic Questions**
   - **Problem & Target Audience:**
     - Who is this product for? (target users, personas)
     - What problem does it solve? (pain points)
     - Why does this problem need solving now?
   - **Value Proposition:**
     - What makes this product unique?
     - What value does it provide to users?
     - What's the core benefit users get?
   - **Scope & Constraints:**
     - What's the MVP (Minimum Viable Product) scope?
     - What's out of scope for v1?
     - Any technical constraints or limitations?
   - **Success Criteria:**
     - How will you know the product is successful?
     - What metrics matter most?
   - **User Journey:**
     - What's the main user flow?
     - What are the key user actions?
     - What happens before and after using the product?

3. **Define the Big Steps (Major Epics/Features)**
   - Break down the product into major functional areas
   - Identify core features that must exist
   - Group related features into logical epics
   - Prioritize: Must-have, Should-have, Nice-to-have
   - Define dependencies between features
   - Estimate complexity (Simple, Medium, Complex)

4. **Create the PRD Document**
   - Create `doc/` folder if it doesn't exist
   - Create file: `doc/prd-{product-name}-YYYY-MM-DD.md`
   - Structure the PRD with:
     - **Overview:** Product name, tagline, one-line description
     - **Problem Statement:** What problem this solves
     - **Target Users:** Who this is for
     - **Goals & Success Metrics:** What success looks like
     - **Core Features:** Major features/epics
     - **User Flows:** Key user journeys
     - **Technical Considerations:** High-level technical notes
     - **Out of Scope:** What's not included in v1
     - **Next Steps:** Recommended development approach

5. **Review and Refine**
   - Show the user the PRD
   - Ask for feedback
   - Make adjustments based on their input
   - Confirm the big steps make sense
   - Verify priorities are correct

## PRD Structure

The PRD should include:

### 1. Overview
- **Product Name:** Clear, memorable name
- **Tagline:** One-sentence description
- **Vision:** What the product aims to achieve
- **Date:** When PRD was created

### 2. Problem Statement
- What problem are we solving?
- Who experiences this problem?
- Why is this problem important?

### 3. Target Users
- Primary user personas
- User needs and pain points
- How they currently solve this problem

### 4. Goals & Success Metrics
- Primary goals
- Key performance indicators (KPIs)
- How success will be measured

### 5. Core Features (Big Steps)
- **Feature Name:** Clear feature title
  - **Description:** What it does
  - **User Value:** Why users care
  - **Priority:** Must-have / Should-have / Nice-to-have
  - **Complexity:** Simple / Medium / Complex
  - **Dependencies:** What needs to be built first

### 6. User Flows
- Key user journeys
- Step-by-step flow for main actions
- Entry points and exit points

### 7. Technical Considerations
- High-level architecture notes
- Integration requirements
- Technology choices (if relevant)
- Performance requirements

### 8. Out of Scope (v1)
- Features explicitly not in the first version
- Future considerations

### 9. Next Steps
- Recommended development approach
- Suggested order of implementation
- Key milestones

## What to Tell the User

- Start: "What's your product idea? Describe it in your own words."
- After initial description: "Let me refine this idea with some questions..."
- Ask strategic questions to clarify:
  - "Who is this product for?"
  - "What problem does it solve?"
  - "What makes it unique?"
  - "What's the MVP scope?"
- After questions: "Based on your answers, here are the big steps I see..."
- Show the major features/epics you've identified
- Create the PRD document
- Show them the PRD: "I've created a PRD document. Let me show you..."
- Ask for feedback: "Does this capture your vision? What would you like to adjust?"
- Make adjustments based on their feedback
- Finalize: "PRD is ready! This will guide your development process."

## Example Questions to Ask

### Problem & Audience
- "Who is this product for? Be specific - what type of person?"
- "What problem does this solve for them? What's their current pain?"
- "Why is this problem worth solving now?"

### Value & Differentiation
- "What makes your product different from existing solutions?"
- "What's the core value users get? The main benefit?"
- "Why would someone choose this over alternatives?"

### Scope
- "What's the absolute minimum needed to launch? The MVP?"
- "What can wait until later versions?"
- "Any constraints - budget, time, technical limitations?"

### Success
- "How will you know this product is successful?"
- "What metrics matter most - users, revenue, engagement?"

### User Experience
- "Walk me through the main user flow - what do they do step by step?"
- "What's the first thing a user sees or does?"
- "What happens when they finish their main task?"

## Tips for Creating Effective PRDs

- **Be Specific:** Vague ideas lead to vague PRDs. Ask clarifying questions.
- **User-Focused:** Always think from the user's perspective, not the technical implementation.
- **Prioritize:** Not everything needs to be in v1. Be clear about what's essential.
- **Realistic:** Consider complexity and dependencies when defining big steps.
- **Actionable:** Each feature should be something you can build and test.
- **Flexible:** PRDs are living documents - they can evolve as you learn more.

## See Also

### Development Commands
- **[Setup New Project](.cursor/commands/setup-new-project.md)**: Initialize a new project
- **[Brainstorm Feature](.cursor/commands/brainstorm-feature.md)**: Deep analysis for complex features
- **[Add Feature](.cursor/commands/add-feature.md)**: Build features from PRD
- **[Build Project](.cursor/commands/build-project.md)**: Build entire project from PRD

### Planning & Documentation
- **[Describe Project](.cursor/commands/describe-project.md)**: Document existing projects
- **[Add Documentation](.cursor/commands/add-documentation.md)**: Add project documentation

### UX/UI Guidelines
- **[UX Principles](.cursor/rules/dont-make-me-think.mdc)**: Understanding user behavior
- **[Design System](.cursor/rules/use-design-system.mdc)**: Using design system components
- **[Review Checklist](.cursor/rules/review-ui-ux.mdc)**: Quality assurance checklist



