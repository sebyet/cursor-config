# Commands Reference by Purpose and Lifecycle Stage

This document organizes all commands by their purpose and which stage of the software development lifecycle they support.

## 🎯 Two Ways to Use Commands

### For Non-Technical Users: 5 Key Commands (Recommended)

**Start here!** These 5 commands are task-oriented and work in plain English:

| Command | When to Use | Example |
|---------|-------------|---------|
| `@setup` | Setting up projects | `@setup` → "Set up a new project" |
| `@build` | Building features | `@build` → "Add a contact form" |
| `@test` | Testing & quality | `@test` → "Run all tests" |
| `@deploy` | Publishing & deploying | `@deploy` → "Publish to production" |
| `@fix` | Fixing problems | `@fix` → "The button doesn't work" |

**Why this is easier:**
- ✅ Think in tasks, not roles ("I want to build" not "I need an engineer")
- ✅ Only 5 commands to remember
- ✅ Natural language - just describe what you want
- ✅ AI automatically routes to the right specialist command

### For Power Users: Role-Based Commands (Advanced)

If you know exactly what you need, you can use role-based commands directly:

- `@engineer/add-feature` - Direct access to feature building
- `@product/brainstorm-feature` - Direct product planning
- `@ux/create-persona` - Direct UX research
- `@devops/check-performance` - Direct performance check
- etc.

**When to use this:**
- You know which role handles the task
- You want to skip the routing step
- You're working on a specific domain

---

## Software Development Lifecycle Stages

1. **Planning & Discovery** - Understanding users, defining requirements, prioritizing features
2. **Design & Architecture** - Creating designs, design systems, technical architecture
3. **Development** - Building, coding, implementing features
4. **Testing** - Quality assurance, testing, bug reporting
5. **Deployment** - Publishing, deploying, releasing to production
6. **Monitoring & Maintenance** - Operations, security, performance, incident management
7. **Growth & Optimization** - Analytics, conversion, SEO, A/B testing

---

## Commands by Lifecycle Stage

| Stage | Command | Purpose | Role |
|-------|---------|---------|------|
| **Planning & Discovery** |
| Planning | `@product/brainstorm-feature` | Brainstorm and evaluate new features | Product Manager |
| Planning | `@product/create-prd` | Create product requirement documents | Product Manager |
| Planning | `@product/define-user-story` | Create user stories with acceptance criteria | Product Manager |
| Planning | `@product/prioritize-features` | Prioritize features using RICE/ICE frameworks | Product Manager |
| Planning | `@product/create-roadmap` | Generate product roadmap documents | Product Manager |
| Planning | `@product/analyze-feature-impact` | Estimate business impact and metrics | Product Manager |
| Planning | `@product/competitive-analysis` | Analyze competitors and market positioning | Product Manager |
| Planning | `@product/pricing-strategy` | Design pricing models and optimize pricing | Product Manager |
| Planning | `@product/user-research` | Synthesize user research and generate insights | Product Manager |
| Planning | `@product/go-to-market` | Plan go-to-market strategy and launch | Product Manager |
| Planning | `@product/product-metrics` | Define product metrics framework | Product Manager |
| Planning | `@product/feature-flag-strategy` | Plan feature flag rollout strategy | Product Manager |
| Planning | `@product/product-positioning` | Define product positioning and messaging | Product Manager |
| Planning | `@product/stakeholder-communication` | Create stakeholder communication templates | Product Manager |
| Discovery | `@ux/create-persona` | Generate user personas from research | UX Designer |
| Discovery | `@ux/create-user-journey` | Map user journeys and experiences | UX Designer |
| Discovery | `@ux/create-research-plan` | Plan user research studies | UX Designer |
| Discovery | `@ux/analyze-user-feedback` | Synthesize user feedback and insights | UX Designer |
| Discovery | `@ux/conduct-usability-test` | Conduct usability testing sessions | UX Designer |
| Discovery | `@ux/heuristic-evaluation` | Evaluate interfaces against usability heuristics | UX Designer |
| Discovery | `@ux/information-architecture` | Design and organize information architecture | UX Designer |
| Discovery | `@ux/task-analysis` | Analyze and break down user tasks | UX Designer |
| Discovery | `@ux/create-user-flow` | Create detailed user flow diagrams | UX Designer |
| Discovery | `@ux/empathy-mapping` | Create empathy maps for user understanding | UX Designer |
| Discovery | `@ux/user-story-mapping` | Organize features by user stories | UX Designer |
| Discovery | `@ux/conduct-user-interviews` | Conduct and analyze user interviews | UX Designer |
| Discovery | `@ux/create-survey` | Create and analyze user surveys | UX Designer |
| Discovery | `@ux/interaction-design` | Design interactions and behaviors | UX Designer |
| Discovery | `@ux/card-sorting` | Conduct card sorting studies for IA | UX Designer |
| Discovery | `@ux/content-strategy` | Plan content strategy and messaging | UX Designer |
| Discovery | `@ux/ux-metrics` | Define and track UX metrics and KPIs | UX Designer |
| Discovery | `@ux/analyze-analytics-ux` | Analyze analytics from UX perspective | UX Designer |
| Discovery | `@ux/service-blueprint` | Create service blueprints for experiences | UX Designer |
| **Design & Architecture** |
| Design | `@design/create-wireframes` | Create low-fidelity wireframes and layouts | UI Designer |
| Design | `@design/competitive-design-analysis` | Analyze competitor designs for insights | UI Designer |
| Design | `@design/create-design-spec` | Generate design specifications | UI Designer |
| Design | `@design/customize-design-system` | Customize design system components | UI Designer |
| Design | `@design/extract-design-tokens` | Extract colors/spacing from designs | UI Designer |
| Design | `@design/check-design-consistency` | Verify design system compliance | UI Designer |
| Design | `@design/generate-component-docs` | Create component documentation | UI Designer |
| Design | `@design/review-design-implementation` | Check if code matches design | UI Designer |
| Design | `@design/visual-audit` | Comprehensive visual design quality review | UI Designer |
| Design | `@design/create-state-designs` | Design empty/error/loading states | UI Designer |
| Design | `@design/accessibility-audit` | Audit accessibility issues | UI Designer |
| Design | `@engineer/design` | Advanced design work (explicit control) | Engineer |
| Architecture | `@engineer/setup-new-project` | Set up new projects from scratch | Engineer |
| Architecture | `@engineer/describe-project` | Describe project structure and features | Engineer |
| **Development** |
| Development | `@engineer/add-feature` | Build new features end-to-end | Engineer |
| Development | `@engineer/modify-feature` | Update existing features | Engineer |
| Development | `@engineer/delete-feature` | Safely remove features | Engineer |
| Development | `@engineer/refactor-code` | Refactor code safely | Engineer |
| Development | `@engineer/code-review` | Review code for quality | Engineer |
| Development | `@engineer/database-migration` | Create database migrations | Engineer |
| Development | `@engineer/add-error-handling` | Add error handling | Engineer |
| Development | `@engineer/deslop` | Remove AI-generated code artifacts | Engineer |
| Development | `@engineer/fix-compile-errors` | Fix compilation errors | Engineer |
| Development | `@engineer/fix-git-issues` | Resolve Git problems | Engineer |
| Development | `@engineer/lint-fix` | Fix linting issues | Engineer |
| Development | `@engineer/fix-everything` | Intelligently fix all issues | Engineer |
| Development | `@engineer/build-project` | Build the project | Engineer |
| Development | `@engineer/debug-performance` | Debug and optimize performance | Engineer |
| Development | `@engineer/security-audit` | Code-level security audit | Engineer |
| Development | `@engineer/integration-test` | Set up integration testing | Engineer |
| Development | `@engineer/e2e-test` | Set up end-to-end testing | Engineer |
| Development | `@engineer/debug-issue` | Debug production issues | Engineer |
| Development | `@engineer/optimize-bundle` | Optimize bundle size | Engineer |
| Development | `@engineer/setup-ci` | Set up CI/CD pipeline | Engineer |
| Development | `@engineer/monitor-errors` | Set up error monitoring | Engineer |
| Development | `@engineer/code-metrics` | Analyze code quality metrics | Engineer |
| Development | `@engineer/dependency-update` | Update dependencies and security patches | Engineer |
| Development | `@engineer/api-mocking` | Set up API mocking | Engineer |
| Development | `@engineer/local-dev-setup` | Set up local development environment | Engineer |
| Development | `@engineer/code-generation` | Generate code from templates | Engineer |
| **Testing** |
| Testing | `@engineer/add-tests` | Add tests for features | Engineer |
| Testing | `@engineer/run-tests` | Run test suites | Engineer |
| Testing | `@qa/create-test-plan` | Generate test plans | QA Engineer |
| Testing | `@qa/write-test-cases` | Create test cases | QA Engineer |
| Testing | `@qa/test-accessibility` | Accessibility testing | QA Engineer |
| Testing | `@qa/test-cross-browser` | Cross-browser testing checklist | QA Engineer |
| Testing | `@qa/integration-test` | Create integration tests | QA Engineer |
| Testing | `@qa/e2e-test` | Create end-to-end tests | QA Engineer |
| Testing | `@qa/api-test` | Create API tests | QA Engineer |
| Testing | `@qa/test-automation` | Set up test automation strategy | QA Engineer |
| Testing | `@qa/performance-test` | Create performance tests | QA Engineer |
| Testing | `@qa/security-test` | Create security tests | QA Engineer |
| Testing | `@qa/report-bug` | Generate bug reports | QA Engineer |
| **Deployment** |
| Deployment | `@engineer/create-pr` | Create pull requests | Engineer |
| Deployment | `@engineer/publish-feature` | Publish feature previews | Engineer |
| Deployment | `@engineer/publish-production` | Deploy to production | Engineer |
| Deployment | `@devops/setup-ci-cd` | Configure CI/CD pipelines | DevOps |
| **Monitoring & Maintenance** |
| Monitoring | `@devops/setup-monitoring` | Configure monitoring and alerts | DevOps |
| Monitoring | `@devops/check-system-health` | Check system health and performance | DevOps |
| Monitoring | `@devops/analyze-incident` | Analyze and document incidents | DevOps |
| Monitoring | `@devops/create-runbook` | Generate runbooks for common issues | DevOps |
| Monitoring | `@devops/setup-logging` | Configure structured logging and aggregation | DevOps |
| Monitoring | `@devops/setup-error-tracking` | Set up error tracking (Sentry, Rollbar) | DevOps |
| Monitoring | `@devops/setup-apm` | Configure Application Performance Monitoring | DevOps |
| Monitoring | `@devops/configure-alerts` | Set up alerting rules and notifications | DevOps |
| Monitoring | `@devops/setup-synthetic-monitoring` | Configure synthetic/uptime monitoring | DevOps |
| Performance | `@devops/check-performance` | Check and optimize performance | DevOps |
| Performance | `@devops/optimize-infrastructure` | Optimize infrastructure costs | DevOps |
| Performance | `@devops/capacity-planning` | Capacity planning and scaling strategies | DevOps |
| Performance | `@devops/setup-cdn` | CDN configuration | DevOps |
| Performance | `@devops/configure-caching` | Caching strategies (Redis, CDN) | DevOps |
| Performance | `@devops/optimize-database-queries` | Database query optimization | DevOps |
| Performance | `@devops/performance-budget` | Set and monitor performance budgets | DevOps |
| Performance | `@devops/auto-scaling` | Configure auto-scaling policies | DevOps |
| Security | `@devops/check-security` | Security audit and fixes | DevOps |
| Security | `@devops/security-audit` | Comprehensive security audit | DevOps |
| Security | `@devops/check-vulnerabilities` | Check for security vulnerabilities | DevOps |
| Security | `@devops/review-permissions` | Review access controls and permissions | DevOps |
| Security | `@devops/compliance-check` | Check compliance (GDPR, SOC2, etc.) | DevOps |
| Security | `@devops/penetration-test` | Security testing procedures | DevOps |
| Security | `@devops/api-security-audit` | API security and rate limiting | DevOps |
| Security | `@devops/container-security` | Container image scanning | DevOps |
| Security | `@devops/setup-waf` | Web Application Firewall setup | DevOps |
| Security | `@devops/audit-logging` | Audit logging for compliance | DevOps |
| Security | `@devops/manage-secrets` | Secrets management (Vault, AWS Secrets Manager) | DevOps |
| Security | `@devops/manage-ssl-certificates` | Manage SSL/TLS certificates | DevOps |
| Infrastructure | `@devops/setup-terraform` | Infrastructure as Code with Terraform | DevOps |
| Infrastructure | `@devops/manage-infrastructure` | Infrastructure lifecycle management | DevOps |
| Infrastructure | `@devops/setup-cloudformation` | AWS CloudFormation setup | DevOps |
| Infrastructure | `@devops/setup-kubernetes` | Set up Kubernetes cluster and orchestration | DevOps |
| Infrastructure | `@devops/manage-containers` | Manage Docker containers and lifecycle | DevOps |
| Infrastructure | `@devops/setup-load-balancer` | Set up and configure load balancers | DevOps |
| Infrastructure | `@devops/manage-dns` | Manage DNS records and configurations | DevOps |
| Infrastructure | `@devops/infrastructure-backup` | Backup infrastructure configurations | DevOps |
| Infrastructure | `@devops/infrastructure-drift-detection` | Detect and manage infrastructure drift | DevOps |
| Infrastructure | `@devops/setup-gitops` | Set up GitOps workflows | DevOps |
| Infrastructure | `@devops/setup-service-mesh` | Set up service mesh for microservices | DevOps |
| Infrastructure | `@devops/cloud-migration` | Plan and execute cloud migration | DevOps |
| Infrastructure | `@devops/multi-cloud-management` | Manage infrastructure across clouds | DevOps |
| Infrastructure | `@devops/resource-tagging` | Set up and manage resource tagging | DevOps |
| Infrastructure | `@devops/infrastructure-testing` | Test infrastructure configurations | DevOps |
| Infrastructure | `@devops/container-registry` | Set up and manage container registries | DevOps |
| Infrastructure | `@devops/infrastructure-documentation` | Generate infrastructure documentation | DevOps |
| Infrastructure | `@devops/configuration-management` | Manage configuration across environments | DevOps |
| Cost | `@devops/cost-optimization` | Analyze and optimize cloud costs | DevOps |
| Cost | `@devops/cloud-cost-analysis` | Analyze cloud costs and generate reports | DevOps |
| Compliance | `@devops/data-retention-policy` | Data retention and deletion policies | DevOps |
| Compliance | `@devops/change-management` | Change management process | DevOps |
| Compliance | `@devops/risk-assessment` | Risk assessment and mitigation | DevOps |
| Compliance | `@devops/disaster-recovery-plan` | Disaster recovery planning | DevOps |
| Maintenance | `@devops/audit-dependencies` | Audit dependencies for vulnerabilities | DevOps |
| Maintenance | `@engineer/maintain` | Explicit maintenance control | Engineer |
| Maintenance | `@engineer/dependency-update` | Update dependencies and security patches | Engineer |
| **Growth & Optimization** |
| Analytics | `@product/analyze-analytics` | Interpret analytics data | Product Manager |
| Analytics | `@product/analyze-metrics` | Analyze key metrics and trends | Product Manager |
| Analytics | `@product/create-dashboard` | Generate analytics dashboard queries | Product Manager |
| Analytics | `@product/identify-insights` | Find insights from data | Product Manager |
| Analytics | `@product/track-conversion` | Set up conversion tracking | Product Manager |
| Conversion | `@growth/analyze-conversion` | Analyze conversion funnels | Growth Engineer |
| Conversion | `@growth/optimize-landing-page` | Optimize landing pages | Growth Engineer |
| Conversion | `@growth/funnel-optimization` | Optimize conversion funnels | Growth Engineer |
| Marketing | `@growth/email-campaign` | Create and optimize email campaigns | Growth Engineer |
| Marketing | `@growth/content-marketing` | Optimize content marketing strategy | Growth Engineer |
| Marketing | `@growth/social-media` | Optimize social media presence | Growth Engineer |
| Marketing | `@growth/referral-program` | Set up referral program | Growth Engineer |
| A/B Testing | `@product/analyze-ab-test` | Analyze A/B test results | Product Manager |
| A/B Testing | `@growth/setup-ab-test` | Set up A/B tests | Growth Engineer |
| A/B Testing | `@growth/growth-experiments` | Design and analyze growth experiments | Growth Engineer |
| Feature Flags | `@growth/setup-feature-flag` | Configure feature flags | Growth Engineer |
| SEO | `@growth/analyze-seo` | Analyze SEO performance | Growth Engineer |
| SEO | `@growth/optimize-seo` | SEO optimization checklist | Growth Engineer |
| SEO | `@growth/generate-meta-tags` | Generate meta tags | Growth Engineer |
| SEO | `@growth/check-structured-data` | Validate structured data | Growth Engineer |
| SEO | `@growth/optimize-performance-seo` | Performance optimization for SEO | Growth Engineer |
| Tracking | `@growth/track-user-journey` | Track user journey analytics | Growth Engineer |
| Tracking | `@growth/event-tracking` | Set up custom event tracking | Growth Engineer |
| Analytics | `@growth/cohort-analysis` | Perform user cohort analysis | Growth Engineer |
| Analytics | `@growth/user-segmentation` | Create user segments | Growth Engineer |
| Analytics | `@growth/retention-analysis` | Analyze user retention metrics | Growth Engineer |

---

## 🚀 Key Commands (Primary Entry Points - Use These First!)

**For non-technical users:** These 5 commands are all you need. Just describe what you want in plain English!

| Command | Purpose | What It Does | Routes To |
|---------|---------|--------------|-----------|
| `@setup` | Set up projects | "Set up a new project" or "Set up this existing project" | `engineer/setup-new-project.md`, `design/customize-design-system.md` |
| `@build` | Build features | "Add a contact form" or "Update the login page" | `engineer/add-feature.md`, `engineer/modify-feature.md`, `engineer/delete-feature.md`, `product/brainstorm-feature.md` |
| `@test` | Test & quality | "Run all tests" or "Check if everything works" | `engineer/run-tests.md`, `engineer/add-tests.md`, `engineer/code-review.md` |
| `@deploy` | Publish & deploy | "Publish to preview" or "Deploy to production" | `engineer/publish-feature.md`, `engineer/publish-production.md`, `engineer/create-pr.md` |
| `@fix` | Fix problems | "The button doesn't work" or "Something's broken" | `engineer/fix-everything.md`, `engineer/fix-compile-errors.md`, `engineer/fix-git-issues.md`, `engineer/lint-fix.md` |

**How it works:**
1. You use one of the 5 key commands
2. Describe what you want in plain English
3. The AI automatically routes to the right specialist command
4. Everything happens automatically!

**Example:**
```
You: @build
AI: "What would you like to build?"
You: "Add a contact form"
AI: [Routes to engineer/add-feature.md automatically]
AI: [Builds the feature, shows preview, tests, documents]
```

---

## 🔧 Commands by Role (Advanced - Direct Access)

**Note:** These are available for power users who know what they need. Most users should use the 5 key commands above instead.

### Software Engineers (`engineer/`)
- Feature development (add-feature, modify-feature, delete-feature, publish-feature)
- Code quality (refactor-code, code-review, lint-fix, code-metrics)
- Bug fixing (fix-everything, fix-compile-errors, fix-git-issues, debug-issue)
- Performance (debug-performance, optimize-bundle)
- Security (security-audit)
- Testing (add-tests, run-tests, integration-test, e2e-test)
- Deployment (create-pr, publish-production, rollback-deployment, canary-deployment, blue-green-deployment)
- CI/CD (setup-ci)
- Monitoring (monitor-errors)
- Maintenance (maintain, deslop, dependency-update)
- Project setup (setup-new-project, build-project, describe-project, local-dev-setup)
- Database (database-migration, data-migration, database-optimization, backup-database, restore-database, setup-database-replication)
- Documentation (create-adr, write-api-docs, create-troubleshooting-guide, onboarding-documentation, create-release-notes)
- Configuration (manage-feature-flags, setup-rate-limiting, api-versioning, version-management)
- Development tools (api-mocking, code-generation)
- Error handling (add-error-handling)
- Design (design)

### Product Managers (`product/`)
- Planning (brainstorm-feature, create-prd, define-user-story, prioritize-features, create-roadmap, go-to-market)
- Analysis (analyze-feature-impact, analyze-analytics, analyze-metrics, analyze-ab-test, analyze-feature-adoption, competitive-analysis, user-research)
- Strategy (pricing-strategy, product-positioning, product-metrics, feature-flag-strategy)
- Tracking (track-conversion, create-dashboard, identify-insights)
- Feedback (create-feedback-loop, measure-feature-success)
- Management (prioritize-bugs, retrospective, stakeholder-communication)

### UX Designers (`ux/`)
- User research (create-research-plan, analyze-user-feedback, conduct-usability-test, heuristic-evaluation, conduct-user-interviews, create-survey)
- User understanding (create-persona, create-user-journey, empathy-mapping, task-analysis)
- Information architecture (information-architecture, card-sorting)
- User flows (create-user-flow, user-story-mapping)
- Interaction design (interaction-design, content-strategy)
- UX measurement (ux-metrics, analyze-analytics-ux)
- Service design (service-blueprint)

### UI Designers (`design/`)
- Wireframes and planning (create-wireframes, competitive-design-analysis)
- Design system (customize-design-system, extract-design-tokens, check-design-consistency)
- Design specs (create-design-spec, review-design-implementation, generate-component-docs)
- Design quality (visual-audit, create-state-designs)
- Accessibility (accessibility-audit)

### DevOps/SRE (`devops/`)
- Monitoring (setup-monitoring, check-system-health, setup-logging, setup-error-tracking, setup-apm, configure-alerts, setup-synthetic-monitoring)
- Performance (check-performance, optimize-infrastructure, capacity-planning, setup-cdn, configure-caching, optimize-database-queries, performance-budget, auto-scaling)
- Security (check-security, security-audit, check-vulnerabilities, review-permissions, compliance-check, penetration-test, api-security-audit, container-security, setup-waf, audit-logging, manage-secrets, manage-ssl-certificates)
- Infrastructure (setup-terraform, manage-infrastructure, setup-cloudformation, setup-kubernetes, manage-containers, setup-load-balancer, manage-dns, infrastructure-backup, infrastructure-drift-detection, setup-gitops, setup-service-mesh, cloud-migration, multi-cloud-management, resource-tagging, infrastructure-testing, container-registry, infrastructure-documentation, configuration-management)
- Cost (cost-optimization, cloud-cost-analysis)
- Compliance (data-retention-policy, change-management, risk-assessment, disaster-recovery-plan)
- Operations (setup-ci-cd, analyze-incident, create-runbook, audit-dependencies)

### QA Engineers (`qa/`)
- Test planning (create-test-plan, write-test-cases, test-automation)
- Testing (test-accessibility, test-cross-browser, visual-regression-test, integration-test, e2e-test, api-test)
- Performance testing (load-test, stress-test, performance-test)
- Advanced testing (chaos-engineering, contract-test, security-test)
- Bug reporting (report-bug)

### Growth Engineers (`growth/`)
- Conversion (analyze-conversion, optimize-landing-page, funnel-optimization)
- Marketing (email-campaign, content-marketing, social-media, referral-program)
- A/B Testing (setup-ab-test, growth-experiments)
- Feature flags (setup-feature-flag)
- SEO (analyze-seo, optimize-seo, generate-meta-tags, check-structured-data, optimize-performance-seo)
- Analytics (track-user-journey, event-tracking, cohort-analysis, user-segmentation, retention-analysis)

---

## 📋 Quick Reference by Need

### For Non-Technical Users (Use Key Commands)

**"I want to start a new project"**
→ `@setup` → "Set up a new project called 'my-app'"

**"I want to add a feature"**
→ `@build` → "Add a contact form"

**"I want to test my code"**
→ `@test` → "Run all tests"

**"I want to deploy"**
→ `@deploy` → "Publish to production"

**"Something is broken"**
→ `@fix` → "The button doesn't work"

**"I want to understand users"**
→ `@build` → "Help me create user personas" (AI routes to UX commands)

**"I want to plan features"**
→ `@build` → "Help me brainstorm a new feature" (AI routes to product commands)

### For Power Users (Direct Access)

**"I want to understand users"**
→ `@ux/create-persona` or `@ux/create-user-journey`

**"I want to plan features"**
→ `@product/brainstorm-feature` or `@product/create-prd`

**"I want to optimize performance"**
→ `@devops/check-performance`

**"I want to analyze metrics"**
→ `@product/analyze-metrics` or `@product/analyze-analytics`

**"I want to improve SEO"**
→ `@growth/optimize-seo` or `@growth/analyze-seo`

