# Command Gap Analysis

This document analyzes the completeness of commands across **engineer**, **growth**, **product**, and **qa** categories.

**Analysis Date:** 2025-01-27

---

## 📊 Summary

| Category | Existing | Missing (Critical) | Missing (Nice-to-Have) | Coverage |
|----------|----------|-------------------|------------------------|----------|
| **Engineer** | 37 | 8 | 5 | ~85% |
| **Growth** | 9 | 6 | 4 | ~60% |
| **Product** | 17 | 5 | 3 | ~77% |
| **QA** | 10 | 4 | 2 | ~71% |

---

## 🔧 Engineer Commands

### ✅ Existing (37 commands)
- Feature management: `add-feature`, `modify-feature`, `delete-feature`, `publish-feature`
- Code quality: `code-review`, `refactor-code`, `lint-fix`, `deslop`
- Bug fixing: `fix-everything`, `fix-compile-errors`, `fix-git-issues`
- Testing: `add-tests`, `run-tests`
- Deployment: `publish-production`, `create-pr`, `rollback-deployment`, `canary-deployment`, `blue-green-deployment`
- Database: `database-migration`, `data-migration`, `database-optimization`, `backup-database`, `restore-database`, `setup-database-replication`
- Documentation: `create-adr`, `write-api-docs`, `create-troubleshooting-guide`, `onboarding-documentation`, `create-release-notes`
- Project setup: `setup-new-project`, `build-project`, `describe-project`
- Configuration: `manage-feature-flags`, `setup-rate-limiting`, `api-versioning`, `version-management`
- Error handling: `add-error-handling`
- Design: `design`
- Maintenance: `maintain`

### ❌ Missing - Critical (8 commands)

1. **`debug-performance.md`** - Performance debugging and profiling
   - Profile slow code paths
   - Identify bottlenecks
   - Optimize rendering performance
   - Memory leak detection

2. **`security-audit.md`** - Code security audit (different from devops/security-audit)
   - Code-level security vulnerabilities
   - Dependency security scanning
   - OWASP Top 10 checks
   - Secure coding practices

3. **`integration-test.md`** - Integration testing setup
   - API integration tests
   - Database integration tests
   - Third-party service integration tests

4. **`e2e-test.md`** - End-to-end testing setup
   - Playwright/Cypress setup
   - E2E test scenarios
   - Test data management

5. **`debug-issue.md`** - Debugging production issues
   - Reproduce bugs
   - Analyze error logs
   - Debug memory issues
   - Performance debugging

6. **`optimize-bundle.md`** - Bundle size optimization
   - Analyze bundle size
   - Code splitting
   - Tree shaking
   - Lazy loading

7. **`setup-ci.md`** - CI/CD pipeline setup (basic)
   - GitHub Actions setup
   - Test automation
   - Build automation
   - Deployment automation

8. **`monitor-errors.md`** - Error monitoring setup
   - Sentry integration
   - Error tracking
   - Error alerting

### 🟡 Missing - Nice-to-Have (5 commands)

1. **`code-metrics.md`** - Code quality metrics
   - Cyclomatic complexity
   - Code coverage reports
   - Technical debt analysis

2. **`dependency-update.md`** - Dependency management
   - Update dependencies
   - Security patches
   - Breaking changes analysis

3. **`api-mocking.md`** - API mocking for development
   - Mock API responses
   - Mock service setup

4. **`local-dev-setup.md`** - Local development environment
   - Docker setup
   - Environment variables
   - Database seeding

5. **`code-generation.md`** - Code generation from templates
   - Component generation
   - API route generation

---

## 📈 Growth Commands

### ✅ Existing (9 commands)
- Conversion: `analyze-conversion`, `optimize-landing-page`
- SEO: `analyze-seo`, `optimize-seo`, `generate-meta-tags`, `check-structured-data`, `optimize-performance-seo`
- Testing: `setup-ab-test`, `setup-feature-flag`
- Analytics: `track-user-journey`

### ❌ Missing - Critical (6 commands)

1. **`email-campaign.md`** - Email marketing campaigns
   - Email template creation
   - Campaign setup
   - A/B testing emails
   - Email analytics

2. **`content-marketing.md`** - Content marketing strategy
   - Blog post optimization
   - Content calendar
   - SEO content optimization
   - Content performance tracking

3. **`social-media.md`** - Social media optimization
   - Social sharing optimization
   - Open Graph optimization
   - Social media analytics
   - Social proof integration

4. **`funnel-optimization.md`** - Conversion funnel optimization
   - Funnel analysis
   - Drop-off identification
   - Conversion path optimization

5. **`cohort-analysis.md`** - User cohort analysis
   - Cohort segmentation
   - Retention analysis
   - Cohort-based metrics

6. **`referral-program.md`** - Referral program setup
   - Referral tracking
   - Incentive management
   - Referral analytics

### 🟡 Missing - Nice-to-Have (4 commands)

1. **`event-tracking.md`** - Event tracking setup
   - Custom event tracking
   - Analytics integration
   - Event schema design

2. **`user-segmentation.md`** - User segmentation
   - Segment creation
   - Behavioral segmentation
   - Segmentation analytics

3. **`retention-analysis.md`** - User retention analysis
   - Retention metrics
   - Churn analysis
   - Retention strategies

4. **`growth-experiments.md`** - Growth experiment framework
   - Experiment design
   - Hypothesis testing
   - Experiment analysis

---

## 📦 Product Commands

### ✅ Existing (17 commands)
- Planning: `brainstorm-feature`, `create-prd`, `define-user-story`, `prioritize-features`, `create-roadmap`
- Analysis: `analyze-feature-impact`, `analyze-analytics`, `analyze-metrics`, `analyze-ab-test`, `analyze-feature-adoption`
- Tracking: `track-conversion`, `create-dashboard`, `identify-insights`
- Feedback: `create-feedback-loop`, `measure-feature-success`
- Management: `prioritize-bugs`, `retrospective`

### ❌ Missing - Critical (5 commands)

1. **`competitive-analysis.md`** - Competitive analysis
   - Competitor feature analysis
   - Market positioning
   - Competitive benchmarking
   - SWOT analysis

2. **`pricing-strategy.md`** - Pricing strategy
   - Pricing model design
   - Price optimization
   - Pricing experiments
   - Revenue analysis

3. **`user-research.md`** - User research synthesis
   - Research synthesis
   - User interview analysis
   - Survey analysis
   - Research insights

4. **`go-to-market.md`** - Go-to-market planning
   - GTM strategy
   - Launch planning
   - Market entry strategy
   - Launch checklist

5. **`product-metrics.md`** - Product metrics framework
   - North Star metric definition
   - KPI framework
   - Metrics dashboard design
   - Metrics tracking setup

### 🟡 Missing - Nice-to-Have (3 commands)

1. **`feature-flag-strategy.md`** - Feature flag strategy
   - Flag rollout strategy
   - Gradual rollout planning
   - Flag management

2. **`product-positioning.md`** - Product positioning
   - Positioning statement
   - Value proposition
   - Messaging framework

3. **`stakeholder-communication.md`** - Stakeholder communication
   - Status updates
   - Communication templates
   - Stakeholder reports

---

## 🧪 QA Commands

### ✅ Existing (10 commands)
- Test planning: `create-test-plan`, `write-test-cases`
- Testing: `test-accessibility`, `test-cross-browser`, `visual-regression-test`
- Performance: `load-test`, `stress-test`
- Advanced: `chaos-engineering`, `contract-test`
- Bug reporting: `report-bug`

### ❌ Missing - Critical (4 commands)

1. **`integration-test.md`** - Integration testing
   - API integration tests
   - Service integration tests
   - Database integration tests
   - Integration test scenarios

2. **`e2e-test.md`** - End-to-end testing
   - E2E test framework setup
   - E2E test scenarios
   - E2E test automation
   - Test data management

3. **`api-test.md`** - API testing
   - API endpoint testing
   - API contract testing
   - API performance testing
   - API security testing

4. **`test-automation.md`** - Test automation strategy
   - Test automation framework
   - CI/CD test integration
   - Test maintenance strategy
   - Test reporting

### 🟡 Missing - Nice-to-Have (2 commands)

1. **`performance-test.md`** - Performance testing (comprehensive)
   - Performance test scenarios
   - Performance benchmarks
   - Performance regression testing
   - Performance monitoring

2. **`security-test.md`** - Security testing
   - Security test scenarios
   - Vulnerability testing
   - Penetration testing support
   - Security test automation

---

## 🎯 Priority Recommendations

### High Priority (Add First)

**Engineer:**
1. `debug-performance.md` - Critical for production issues
2. `security-audit.md` - Security is always critical
3. `integration-test.md` - Essential for quality
4. `e2e-test.md` - Critical for user-facing features

**Growth:**
1. `email-campaign.md` - Core growth channel
2. `content-marketing.md` - SEO and content strategy
3. `funnel-optimization.md` - Conversion optimization

**Product:**
1. `competitive-analysis.md` - Market understanding
2. `user-research.md` - User insights
3. `go-to-market.md` - Launch planning

**QA:**
1. `integration-test.md` - Essential testing type
2. `e2e-test.md` - Critical for user flows
3. `api-test.md` - API quality assurance

### Medium Priority

**Engineer:**
- `debug-issue.md`
- `optimize-bundle.md`
- `setup-ci.md`

**Growth:**
- `cohort-analysis.md`
- `social-media.md`

**Product:**
- `pricing-strategy.md`
- `product-metrics.md`

**QA:**
- `test-automation.md`

### Low Priority (Nice-to-Have)

All commands marked as "Nice-to-Have" can be added as needed based on specific project requirements.

---

## 📝 Notes

1. **Overlap with DevOps:** Some commands (like `security-audit`, `setup-ci`) might overlap with devops commands. Consider if they should be consolidated or kept separate for role-specific workflows.

2. **Command Organization:** Consider if some commands should be moved between categories (e.g., `setup-ab-test` in growth vs product).

3. **Command Templates:** When creating new commands, follow the existing pattern and structure from similar commands.

4. **Testing Coverage:** QA commands are well-covered for basic testing, but integration and E2E testing are critical gaps.

5. **Growth Commands:** Growth category has the lowest coverage and would benefit significantly from the missing commands.

---

## ✅ Next Steps

1. **Review this analysis** with the team
2. **Prioritize missing commands** based on current project needs
3. **Create missing commands** starting with High Priority items
4. **Update COMMANDS-REFERENCE.md** as new commands are added
5. **Test new commands** to ensure they follow existing patterns

---

**Last Updated:** 2025-01-27

