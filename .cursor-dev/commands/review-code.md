# Code Review

## Overview
Perform a thorough review of implemented code to ensure correctness, maintainability, safety, and compliance with standards before merging.

## Steps
1. **Prepare for review**
   - Ensure branch/PR is small and focused
   - Include descriptive commit messages
   - Reference plan, acceptance criteria, and `engineer-playbook.md`

2. **Review for correctness**
   - Verify code meets acceptance criteria
   - Check all edge cases are handled
   - Confirm unit and integration tests exist and pass
   - Ensure no regressions are introduced

3. **Review for readability & maintainability**
   - Code is clear and easy to understand
   - Functions/methods are small and focused
   - Variable and function names are descriptive
   - Complex logic is commented if necessary
   - Follows patterns and conventions from `engineer-playbook.md`

4. **Review for safety & risk**
   - Errors and exceptions are properly handled
   - Security concerns addressed (input validation, sensitive data)
   - Avoids performance issues and side effects
   - Breaking changes clearly identified

5. **Review for testing**
   - Tests cover expected behaviors and edge cases
   - Test names are clear and descriptive
   - Critical paths have sufficient coverage

6. **Provide feedback**
   - Comment constructively and clearly
   - Highlight issues, suggest improvements, ask clarifying questions
   - Prioritize critical fixes over minor improvements

7. **Approve or request changes**
   - Approve if standards, tests, and acceptance criteria are met
   - Request changes for bugs, missing tests, unclear code, or standard violations

8. **Learn and document**
   - Note patterns or recurring issues for team improvement
   - Update documentation if needed
   - Feed insights into future iterations or planning

## Checklist
- [ ] Code meets acceptance criteria
- [ ] All edge cases handled
- [ ] Tests exist and pass
- [ ] Readable and maintainable
- [ ] Follows `engineer-playbook.md` standards
- [ ] Safe, secure, and low-risk
- [ ] Feedback provided or received
