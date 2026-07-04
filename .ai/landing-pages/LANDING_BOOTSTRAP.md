# Purpose

Define the landing page domain bootstrap, including supported styles, specification structure, generation order, review workflow, and completion criteria.

# Scope

Covers all landing page specifications for the project's public-facing marketing pages. This document governs documentation generation only. Implementation is prohibited until specifications are approved.

# Principles

## Domain Philosophy

- **Inheritance First**: All landing page specs inherit Engineering Handbook standards
- **Style Isolation**: Each landing page style is independent and self-contained
- **Progressive Complexity**: Styles range from minimal SaaS setups to Three.js experiences
- **Reusability**: Landing pages share components from the shared UI layer where possible
- **Performance**: Every style must meet performance standards defined in the handbook

# Standards

## Supported Landing Page Styles

The project supports 7 distinct landing page styles. Each style defines a complete visual and interaction pattern. Specifications are generated one style at a time.

| ID | Style | Complexity | Use Case |
|----|-------|------------|----------|
| 01 | minimal-saas | Low | Utilities, products, SaaS launches |
| 02 | modern-gradient | Medium | Brand-forward sites, agencies |
| 03 | dashboard-preview | Medium | Back-office tools, analytics |
| 04 | floating-cards | Medium | Features, pricing, showcases |
| 05 | bento-grid | High | Product marketing, integrations |
| 06 | storytelling | High | Brand narrative, long-form |
| 07 | threejs | High | Immersive experiences, demos |

## Required Documentation Structure

Each landing page specification folder must contain:

```
01-minimal-saas/
├── SPECIFICATION.md
├── components.md
├── copy.md
├── assets.md
└── implementation-order.md
```

All files must follow the standard handbook template where applicable.

## Document Responsibilities

- LANDING_BOOTSTRAP.md: Governs the landing page domain, defines styles, and controls generation order
- SPECIFICATION.md: Defines the implementation-ready specification for a single style
- components.md: Lists required components with props, variants, and acceptance criteria
- copy.md: Defines copy requirements, content hierarchy, and placeholder copy
- assets.md: Lists required images, icons, fonts, media, and their specifications
- implementation-order.md: Defines component build and integration sequence

## Generation Order

Generate specifications in sequential ID order. Do not skip styles. Each specification requires review and approval before the next is generated.

1. 01-minimal-saas
2. 02-modern-gradient
3. 03-dashboard-preview
4. 04-floating-cards
5. 05-bento-grid
6. 06-storytelling
7. 07-threejs

## Review Workflow

After generating a specification:
1. Structural Review: Verify all required files exist
2. Consistency Review: Confirm inheritance from Engineering Handbook
3. Dependency Review: Check for conflicts with previously approved styles
4. Improvement Pass: Refine based on review findings
5. Final Review: Confirm completeness before presenting

Present the style options to the user and wait for selection before generating any specification.

## Engineering Handbook Inheritance

All landing page specifications inherit:

- 01-principles.md
- 02-architecture.md
- 03-folder-structure.md
- 04-design-system.md
- 05-component-architecture.md
- 06-react.md
- 07-inertia.md
- 08-laravel.md
- 09-tailwind.md
- 10-nwidart.md
- 11-ai-workflow.md
- 12-performance.md
- 13-accessibility.md
- 14-code-review.md
- 15-definition-of-done.md

Specifications must not contradict handbook standards. If a conflict exists, the handbook takes precedence.

## Complete Landing Page Design Catalog

### 01-minimal-saas

A clean, typographic-focused layout. Whitespace-driven. Single-column content flow. Minimal color application beyond the design system palette.

Required sections:
- Hero with headline, subheadline, CTA, and trust indicator
- Feature grid (3 items)
- Testimonial (1)
- Pricing preview (optional)
- Footer CTA

Component count: 5-8
Interaction complexity: Low

### 02-modern-gradient

Bold gradients, glassmorphism cards, and layered visual effects. High visual impact with maintained accessibility.

Required sections:
- Hero with gradient background and floating card
- Feature showcase (2-3 items with icons)
- Social proof strip
- Footer

Component count: 6-10
Interaction complexity: Medium

### 03-dashboard-preview

Product preview emphasis. Side-by-side layout, contextual UI mockups, and developer-focused detailing.

Required sections:
- Hero with product preview image/component
- Feature breakdown (3 points)
- Code example block
- Integration logos
- CTA

Component count: 7-12
Interaction complexity: Medium

### 04-floating-cards

Asymmetric layout with elevated cards that show depth through shadows and transforms. Scroll-triggered animations.

Required sections:
- Hero with floating card stack
- Feature bento cards (3-4 items)
- Pricing cards (2-3 tiers)
- CTA section

Component count: 8-12
Interaction complexity: Medium

### 05-bento-grid

Grid-based layout with varied card sizes. Information density with clear hierarchy. Apple-style presentation.

Required sections:
- Hero with headline grid
- Feature grid (Apple-style: 1x1, 2x1, 1x2, 2x2 combinations)
- Integrations grid
- CTA

Component count: 10-15
Interaction complexity: High

### 06-storytelling

Narrative-driven scroll experience. Section transitions, scroll-triggered reveals, and progressive disclosure.

Required sections:
- Opening statement
- Problem statement
- Solution walkthrough
- Social proof
- Final CTA

Component count: 12-20
Interaction complexity: High

### 07-threejs

Three.js immersive experience. 3D elements as background or interactive centerpieces. Performance sensitive.

Required sections:
- Immersive hero with 3D element
- Feature sections overlay
- Interactive demo placeholder
- CTA

Component count: 8-15
Interaction complexity: Very High

## Design Selection Matrix

Use the following criteria when assisting users with style selection:

| Criterion | Weight | Notes |
|-----------|--------|-------|
| Product type | High | Match style to brand position |
| Performance budget | High | threejs requires significant JS |
| Team skill | Medium | Complex styles need experienced devs |
| Timeline | Medium | Complex styles take longer |
| Accessibility | High | All styles must meet WCAG standards |

## Package Recommendation Matrix

| Style | Required Additions |
|-------|-------------------|
| 01-minimal-saas | None beyond core stack |
| 02-modern-gradient | None beyond core stack |
| 03-dashboard-preview | highlight.js or prism.js for code blocks |
| 04-floating-cards | Intersection Observer (native) |
| 05-bento-grid | None beyond core stack |
| 06-storytelling | gsap or framer-motion for scroll animations |
| 07-threejs | three.js, @react-three/fiber, @react-three/drei |

Dependencies must be tracked in the landing page assets.md specification.

## AI Workflow

1. Present style catalog to user
2. User selects a landing page style by ID and name
3. Generate only the selected style's specifications in the correct directory
4. Perform review workflow before presenting
5. Await explicit approval
6. Do not proceed until approved

## Completion Criteria

- LANDING_BOOTSTRAP.md reviewed and approved
- All 7 landing page specifications generated in sequential order
- Each specification reviewed and approved
- Specifications are internally consistent
- No conflicts with Engineering Handbook standards exist

# Best Practices

- Keep specifications implementation-ready but high-level enough for future flexibility
- Reuse shared UI components from `resources/js/Components/` wherever possible
- Document all animation and interaction requirements explicitly
- Include accessibility requirements for each section in specifications
- Track external dependencies in assets.md for each style
- Specify lazy loading strategies for complex assets in implementation-order.md

# Anti-patterns

- Generating more than one specification without user selection
- Proceeding to implementation before specifications are approved
- Contradicting handbook standards in landing page docs
- Creating landing-specific components that belong in shared UI
- Over-specifying pixel-perfect layouts - specify behavior and tokens, not exact dimensions
- Skipping accessibility requirements in any specification
- Generating empty placeholder directories - all structure must be populated with docs

# Examples

## Example Specification Header

```markdown
# Landing Page Specification

## Style: 01-minimal-saas

## Inherits From
- .ai/handbook/01-principles.md
- .ai/handbook/04-design-system.md
- .ai/handbook/06-react.md
- .ai/handbook/09-tailwind.md
- .ai/handbook/12-performance.md
```

# Checklist

- [ ] All 7 landing page styles defined
- [ ] Documentation structure documented
- [ ] Document responsibilities mapped
- [ ] Generation order established
- [ ] Review workflow defined
- [ ] Handbook inheritance list complete
- [ ] Design catalog covers all styles
- [ ] Design Selection Matrix provided
- [ ] Package Recommendation Matrix provided
- [ ] AI workflow documented
- [ ] Completion criteria defined

# Dependencies

04-design-system.md, 05-component-architecture.md, 06-react.md, 09-tailwind.md, 12-performance.md, 13-accessibility.md, 15-definition-of-done.md, HANDBOOK_BLUEPRINT.md

# References

02-architecture.md, 03-folder-structure.md, 07-inertia.md, 08-laravel.md
