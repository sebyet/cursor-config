# Plan Work

## Overview
Break a designed solution into **atomic, delegable steps** that can be executed safely, with clear inputs, outputs, and verification, to produce working code.  
Reference: `engineer-playbook.md` as the source of truth for standards, conventions, and best practices.

## Steps
1. **Decompose the solution**
   - Break the solution into self-contained, testable steps
   - Example: create endpoint → implement logic → add tests → update docs

2. **Define inputs and outputs**
   - **Input**: what is needed to complete the step (code snippets, data models, function signatures)
   - **Output**: what the step should produce (code, tests, documentation)
   - Ensure steps are unambiguous and focused
   - Follow conventions in `engineer-playbook.md`

3. **Establish dependencies**
   - Determine which steps must precede others
   - Create a sequence or DAG of steps
   - Ensure no step is executed before its prerequisites

4. **Set constraints**
   - Code style and patterns
   - Performance, security, or operational requirements
   - Avoid breaking existing interfaces
   - Adhere to guidelines in `engineer-playbook.md`

5. **Verification & feedback**
   - Include test or validation after each step:
     - Unit tests pass
     - Lint/style check passes
     - Behavior matches acceptance criteria
   - If verification fails, loop back to fix the step

6. **Integration & iteration**
   - Integrate all steps into the main branch/module
   - Run full integration/end-to-end tests
   - Document final changes and any assumptions

7. **Documentation**
   - Include what was done, why, and any notes or assumptions
   - Keeps the team aligned and ensures reproducibility
   - Reference `engineer-playbook.md` for documentation standards

## Checklist
- [ ] Solution broken into atomic, testable steps
- [ ] Inputs and outputs defined for each step
- [ ] Dependencies and execution order clear
- [ ] Constraints and rules documented according to `engineer-playbook.md`
- [ ] Verification included after each step
- [ ] Integration and final testing planned
- [ ] Documentation and notes follow `engineer-playbook.md` standards
