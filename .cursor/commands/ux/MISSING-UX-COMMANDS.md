# Missing UX Commands Analysis

This document identifies UX tasks that are NOT covered by existing commands, after checking all command categories.

## ✅ Currently Covered UX Commands

1. **`ux/create-persona.md`** - Generate user personas from research
2. **`ux/create-user-journey.md`** - Map user journeys end-to-end
3. **`ux/create-research-plan.md`** - Plan user research studies (mentions usability testing, interviews, surveys)
4. **`ux/analyze-user-feedback.md`** - Synthesize user feedback and insights (mentions surveys, interviews)

## ✅ Partially Covered (Mentioned But Not Dedicated Commands)

### Covered Elsewhere (Don't Need UX Commands)
- ✅ **User Stories** - `product/define-user-story.md` (defines individual user stories)
- ✅ **Analytics Analysis** - `product/analyze-analytics.md` (general analytics, not UX-focused)
- ✅ **Feedback Collection** - `product/create-feedback-loop.md` (sets up feedback systems)

### Mentioned But Need Dedicated Commands
- ⚠️ **Usability Testing** - Mentioned in `ux/create-research-plan.md` but no dedicated command
- ⚠️ **User Interviews** - Mentioned in `ux/create-research-plan.md` and `ux/analyze-user-feedback.md` but no dedicated command
- ⚠️ **Surveys** - Mentioned in `ux/create-research-plan.md` and `ux/analyze-user-feedback.md` but no dedicated command
- ⚠️ **Information Architecture** - Mentioned in `design/create-wireframes.md` and `design/visual-audit.md` but no dedicated command
- ⚠️ **User Flows** - Mentioned in `design/create-wireframes.md` and `design/competitive-design-analysis.md` but no dedicated command

---

## 🎯 Missing UX Commands (Should Create)

### High Priority - Core UX Research & Evaluation

#### 1. **`ux/conduct-usability-test.md`** ⭐
**Purpose:** Conduct usability testing sessions and analyze results
**Why needed:** Core UX validation method, only mentioned in research plan
**Use cases:**
- Plan usability test sessions
- Create test scenarios and tasks
- Conduct usability tests (moderated/unmoderated)
- Analyze usability test results
- Identify usability issues and prioritize fixes
- Generate usability test reports

#### 2. **`ux/heuristic-evaluation.md`** ⭐
**Purpose:** Evaluate interfaces against usability heuristics (Nielsen's 10 heuristics)
**Why needed:** Quick, expert-based evaluation method, not covered anywhere
**Use cases:**
- Evaluate interface against usability principles
- Identify heuristic violations
- Prioritize usability issues
- Generate heuristic evaluation reports
- Compare multiple design options

#### 3. **`ux/information-architecture.md`** ⭐
**Purpose:** Design and organize information architecture
**Why needed:** Critical for content organization, only mentioned in design commands
**Use cases:**
- Design site structure and navigation
- Organize content hierarchies
- Create sitemaps and content models
- Plan information architecture improvements
- Document IA decisions

#### 4. **`ux/task-analysis.md`** ⭐
**Purpose:** Analyze and break down user tasks
**Why needed:** Foundation for understanding user workflows, not covered
**Use cases:**
- Break down user tasks into steps
- Identify task goals and sub-goals
- Document task flows and dependencies
- Identify pain points in task completion
- Optimize task flows

### Medium Priority - User Understanding & Flows

#### 5. **`ux/create-user-flow.md`**
**Purpose:** Create detailed user flow diagrams (different from journey maps)
**Why needed:** More granular than journey maps, only mentioned in design commands
**Use cases:**
- Map detailed user flows for specific tasks
- Document decision points and branches
- Identify flow optimization opportunities
- Create flow diagrams for development handoff
- Compare alternative flow options

#### 6. **`ux/empathy-mapping.md`**
**Purpose:** Create empathy maps to understand user context and emotions
**Why needed:** Deep user understanding tool, complements personas, not covered
**Use cases:**
- Map user thoughts, feelings, actions, and pain points
- Understand user context and environment
- Identify emotional triggers and motivations
- Create empathy maps for different user segments
- Use empathy maps to inform design decisions

#### 7. **`ux/user-story-mapping.md`**
**Purpose:** Create user story maps to organize features by user stories
**Why needed:** Different from `product/define-user-story.md` - this organizes multiple stories into a map
**Use cases:**
- Organize features by user stories
- Map user activities and tasks
- Prioritize features and releases
- Plan MVP and feature roadmaps
- Align team on user value

#### 8. **`ux/conduct-user-interviews.md`**
**Purpose:** Conduct and analyze user interviews
**Why needed:** Core qualitative research method, only mentioned but not dedicated
**Use cases:**
- Plan user interview sessions
- Create interview guides and questions
- Conduct user interviews
- Analyze interview transcripts
- Extract insights and themes from interviews
- Generate interview reports

### Lower Priority - Specialized UX Tasks

#### 9. **`ux/create-survey.md`**
**Purpose:** Create and analyze user surveys
**Why needed:** Quantitative research method, only mentioned but not dedicated
**Use cases:**
- Design survey questions
- Create survey structure and flow
- Analyze survey results
- Extract insights from survey data
- Generate survey reports

#### 10. **`ux/interaction-design.md`**
**Purpose:** Design interactions and behaviors
**Why needed:** Interaction design is core UX work, not covered
**Use cases:**
- Design interaction patterns
- Specify interaction behaviors
- Design micro-interactions
- Create interaction specifications
- Document interaction design decisions

#### 11. **`ux/card-sorting.md`**
**Purpose:** Conduct card sorting studies for information architecture
**Why needed:** User-driven IA research method, not covered
**Use cases:**
- Plan card sorting studies
- Create card sorting tasks
- Analyze card sorting results
- Use results to inform IA decisions
- Compare open vs. closed card sorting

#### 12. **`ux/content-strategy.md`**
**Purpose:** Plan content strategy and messaging
**Why needed:** UX includes content and messaging decisions, not covered
**Use cases:**
- Plan content structure and hierarchy
- Define content tone and voice
- Create content guidelines
- Plan content for different user journeys
- Optimize content for user goals

#### 13. **`ux/ux-metrics.md`**
**Purpose:** Define and track UX metrics and KPIs
**Why needed:** Measure UX success and improvement, different from product metrics
**Use cases:**
- Define UX metrics and KPIs (task success rate, time on task, error rate, etc.)
- Set up UX measurement framework
- Track UX metrics over time
- Analyze UX metric trends
- Report on UX performance

#### 14. **`ux/analyze-analytics-ux.md`**
**Purpose:** Analyze analytics data from UX perspective
**Why needed:** UX interpretation of analytics data, different from product analytics
**Use cases:**
- Interpret analytics data for UX insights
- Identify UX issues from analytics
- Analyze user behavior patterns
- Find conversion barriers
- Generate UX-focused analytics reports

#### 15. **`ux/service-blueprint.md`**
**Purpose:** Create service blueprints for service experiences
**Why needed:** Maps service experiences beyond digital touchpoints, not covered
**Use cases:**
- Map service experiences end-to-end
- Identify service touchpoints
- Document frontstage and backstage processes
- Find service improvement opportunities
- Align teams on service delivery

---

## 📊 Priority Summary

### Must Have (High Priority) - 4 Commands
1. **`ux/conduct-usability-test.md`** - Core UX validation method
2. **`ux/heuristic-evaluation.md`** - Quick expert evaluation
3. **`ux/information-architecture.md`** - Critical for content organization
4. **`ux/task-analysis.md`** - Foundation for understanding workflows

### Should Have (Medium Priority) - 4 Commands
5. **`ux/create-user-flow.md`** - Detailed flow mapping
6. **`ux/empathy-mapping.md`** - Deep user understanding
7. **`ux/user-story-mapping.md`** - Feature prioritization tool
8. **`ux/conduct-user-interviews.md`** - Core qualitative research

### Nice to Have (Lower Priority) - 7 Commands
9. **`ux/create-survey.md`** - Quantitative research
10. **`ux/interaction-design.md`** - Interaction specifications
11. **`ux/card-sorting.md`** - IA research method
12. **`ux/content-strategy.md`** - Content planning
13. **`ux/ux-metrics.md`** - UX measurement
14. **`ux/analyze-analytics-ux.md`** - Analytics interpretation
15. **`ux/service-blueprint.md`** - Service experience mapping

---

## 🎯 Recommended Next Steps

1. **Start with High Priority commands** - These cover core UX research and evaluation methods
2. **Focus on user understanding** - Commands that help understand users deeply
3. **Add specialized commands as needed** - Based on actual UX workflow needs

---

## 📝 Notes

- UX commands should focus on research, understanding, and evaluation
- Design commands handle visual design; UX commands handle user research and flows
- Product commands handle business/product perspective; UX commands focus on user perspective
- Some overlap is expected, but each command should have a clear focus
- Commands should support both qualitative and quantitative research methods
- Consider the UX workflow: Research → Understand → Design → Test → Iterate
