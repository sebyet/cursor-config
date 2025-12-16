# Test Locally

## Overview
Verify the implemented solution on your local or development environment to ensure correctness, stability, and compliance with requirements before wider deployment. Follow the steps carefully and document results.

## Steps
1. **Prepare environment**
   - Ensure local/dev environment mirrors staging/production
   - Pull latest code and dependencies
   - Verify database schemas, configs, and environment variables
   - Clear caches or temporary data if needed

2. **Identify test scope**
   - Unit tests: individual functions/components
   - Integration tests: interactions between modules/services
   - End-to-end / functional tests: full user scenarios
   - Edge case tests: boundary inputs, error handling, unusual states

3. **Run automated tests**
   - Execute existing and newly added unit tests
   - Run linting and static analysis tools
   - Run integration and functional tests if available
   - Confirm all tests pass

4. **Manual verification**
   - Simulate realistic user or system workflows affected by the change
   - Validate:
     - Output matches expected results
     - UI/UX behaves correctly (if relevant)
     - Error handling works
     - No unexpected side effects in other modules

5. **Performance & edge case checks**
   - Test scenarios that may stress the system
   - Check for slow responses, memory leaks, resource contention, unexpected exceptions

6. **Logging & monitoring**
   - Check logs and debug outputs for hidden errors
   - Confirm metrics are within expected thresholds

7. **Document results**
   - Note test outcomes and minor issues discovered
   - Reference plan and acceptance criteria to confirm verification
   - Prepare notes for next iteration, peer review, or QA handoff

## Checklist
- [ ] Local/dev environment prepared and matches expected configuration
- [ ] All relevant automated tests executed and passed
- [ ] Manual verification of workflows completed
- [ ] Edge cases and performance scenarios tested
- [ ] Logs and metrics checked for anomalies
- [ ] Results documented with references to plan and acceptance criteria
