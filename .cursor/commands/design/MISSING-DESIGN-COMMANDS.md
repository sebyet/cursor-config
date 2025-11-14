# Missing Design Commands Analysis

This document identifies design tasks that are NOT covered by existing commands across all categories.

## ✅ Already Covered (Don't Need New Commands)

### Covered by Existing Design Commands
- ✅ **Accessibility audit** - `design/accessibility-audit.md`
- ✅ **Design consistency check** - `design/check-design-consistency.md`
- ✅ **Create design specs** - `design/create-design-spec.md`
- ✅ **Customize design system** - `design/customize-design-system.md` (includes color palette & typography)
- ✅ **Extract design tokens** - `design/extract-design-tokens.md`
- ✅ **Generate component docs** - `design/generate-component-docs.md`
- ✅ **Review design implementation** - `design/review-design-implementation.md`

### Covered by Other Commands
- ✅ **Visual regression testing** - `qa/visual-regression-test.md`
- ✅ **A/B test variants** - `growth/setup-ab-test.md` (creates variants)
- ✅ **Landing page design optimization** - `growth/optimize-landing-page.md` (optimizes design)
- ✅ **Dashboard visualizations** - `product/create-dashboard.md` (visualization recommendations)
- ✅ **Color palette generation** - Partially in `design/customize-design-system.md` (chart colors)
- ✅ **Typography selection** - Covered in `design/customize-design-system.md`

---

## 🎯 Missing Design Commands (Should Create)

### High Priority - Core Design Workflows

#### 1. **`design/create-wireframes.md`**
**Purpose:** Create low-fidelity wireframes and layout structures
**Why needed:** Foundation of design process, not covered anywhere
**Use cases:**
- Create wireframe layouts for new features
- Design page structure and information architecture
- Plan component placement and hierarchy
- Create responsive wireframe variations

#### 2. **`design/competitive-design-analysis.md`**
**Purpose:** Analyze competitor designs and extract insights
**Why needed:** Strategic design research, not covered
**Use cases:**
- Analyze competitor UI/UX patterns
- Extract design inspiration and best practices
- Identify design trends in the industry
- Compare design approaches across competitors

#### 3. **`design/create-style-guide.md`**
**Purpose:** Create comprehensive brand/style guide documentation
**Why needed:** Brand guidelines separate from design system tokens
**Use cases:**
- Document brand identity and visual language
- Create usage guidelines for logos, colors, typography
- Define brand voice and tone
- Create brand asset library documentation

#### 4. **`design/export-assets.md`**
**Purpose:** Export and optimize design assets for development
**Why needed:** Critical handoff step, not automated
**Use cases:**
- Export images, icons, graphics from designs
- Optimize assets (compression, formats, sizes)
- Generate asset specifications (dimensions, formats)
- Create asset naming conventions
- Export assets for different screen densities

### Medium Priority - Design Quality & Handoff

#### 5. **`design/create-prototype.md`**
**Purpose:** Create interactive, clickable prototypes for testing
**Why needed:** Prototyping is distinct from implementation
**Use cases:**
- Create clickable prototypes from designs
- Design interaction flows and user paths
- Test navigation and user journeys
- Share prototypes for stakeholder feedback

#### 6. **`design/visual-audit.md`**
**Purpose:** Comprehensive visual design quality review (beyond consistency)
**Why needed:** Different from consistency check - focuses on aesthetic quality
**Use cases:**
- Review visual hierarchy and information architecture
- Assess visual balance and composition
- Evaluate color harmony and contrast (aesthetic, not just accessibility)
- Review typography choices and readability
- Assess spacing, alignment, and whitespace

#### 7. **`design/design-handoff.md`**
**Purpose:** Create detailed design-to-development handoff documentation
**Why needed:** Critical for developer implementation, more than just specs
**Use cases:**
- Create comprehensive handoff documentation
- Document all design decisions and rationale
- Provide asset specifications and export instructions
- Include interaction specifications and animations
- Document responsive behavior and breakpoints

#### 8. **`design/create-state-designs.md`**
**Purpose:** Design empty states, error states, and loading states
**Why needed:** Specific design patterns not covered in general design
**Use cases:**
- Design empty state illustrations and messaging
- Create error state designs and messaging
- Design loading indicators and skeleton screens
- Create onboarding flow designs
- Design micro-interactions and transitions

### Lower Priority - Specialized Design Tasks

#### 9. **`design/create-illustrations.md`**
**Purpose:** Create custom illustrations and graphics
**Why needed:** Custom visual assets, not covered
**Use cases:**
- Design custom illustrations for marketing
- Create icon sets and iconography
- Design data visualization graphics
- Create custom graphics and imagery

#### 10. **`design/animation-specs.md`**
**Purpose:** Create detailed animation and transition specifications
**Why needed:** Motion design is specialized, needs detailed specs
**Use cases:**
- Document animation timing and easing
- Specify transition behaviors
- Design micro-interactions
- Create motion design guidelines

#### 11. **`design/design-presentation.md`**
**Purpose:** Create design presentations for stakeholders
**Why needed:** Communication and collaboration tool
**Use cases:**
- Create design presentations
- Document design rationale and decisions
- Present design concepts to stakeholders
- Create design review materials

#### 12. **`design/create-design-brief.md`**
**Purpose:** Create design project briefs and requirements
**Why needed:** Planning and scoping design work
**Use cases:**
- Create design project briefs
- Document design requirements
- Define design scope and deliverables
- Plan design sprints and timelines

---

## 📊 Priority Summary

### Must Have (High Priority)
1. **`design/create-wireframes.md`** - Foundation of design process
2. **`design/competitive-design-analysis.md`** - Strategic design research
3. **`design/create-style-guide.md`** - Brand guidelines separate from tokens
4. **`design/export-assets.md`** - Critical for design handoff

### Should Have (Medium Priority)
5. **`design/create-prototype.md`** - Important for testing and validation
6. **`design/visual-audit.md`** - Quality assurance beyond consistency
7. **`design/design-handoff.md`** - Critical for developer collaboration
8. **`design/create-state-designs.md`** - Common design patterns

### Nice to Have (Lower Priority)
9. **`design/create-illustrations.md`** - Specialized asset creation
10. **`design/animation-specs.md`** - Motion design specifications
11. **`design/design-presentation.md`** - Communication tool
12. **`design/create-design-brief.md`** - Planning tool

---

## 🎯 Recommended Next Steps

1. **Start with High Priority commands** - These cover core design workflows
2. **Focus on handoff and collaboration** - Commands that bridge design and development
3. **Add specialized commands as needed** - Based on actual usage patterns

---

## 📝 Notes

- Some tasks might be partially covered by `@build` or `@engineer/add-feature`, but designers need explicit design-focused commands
- Design commands should focus on design work BEFORE implementation
- Consider the designer's workflow: Research → Wireframe → Design → Prototype → Handoff → Assets
- Commands should support both visual designers and UX designers

