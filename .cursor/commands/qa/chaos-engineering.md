# Chaos Engineering

Perform chaos engineering tests to verify system resilience and fault tolerance.

## What This Command Does

Performs chaos engineering by:
- Injecting failures (network, CPU, memory, etc.)
- Testing system resilience
- Verifying fault tolerance
- Measuring recovery time
- Generating resilience improvements

## How It Works

1. **Understand Chaos Testing Needs**
   - Ask about resilience requirements
   - Identify critical services
   - Understand failure scenarios
   - Determine test scope

2. **Design Chaos Tests**
   - Create failure scenarios
   - Set up chaos injection
   - Define success criteria
   - Plan recovery verification

3. **Execute and Analyze**
   - Run chaos tests
   - Measure system behavior
   - Analyze recovery
   - Generate recommendations

## What to Tell the User

- "What failure scenarios should we test? (network, CPU, memory, service failures)"
- "What are your resilience requirements?"
- Execute chaos tests and analyze results
- "Chaos engineering complete! Tests: [count]. Resilience: [assessment]. Recommendations: [list]"

## See Also

- **[Stress Test](stress-test.md)**: Stress testing
- **[Load Test](load-test.md)**: Load testing
- **[Analyze Incident](../devops/analyze-incident.md)**: Analyze incidents

