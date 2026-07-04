# Purpose

Prompt template for reviewing existing components.

# Scope

Use this template when reviewing React components for handbook compliance.

# Instructions

Reference these documents during review:
1. `.ai/handbook/05-component-architecture.md`
2. `.ai/handbook/04-design-system.md`
3. `.ai/handbook/06-react.md`
4. `.ai/handbook/13-accessibility.md`

# Template

Review the component against these criteria:

## Architecture
- Function declaration used
- Props interface defined
- Named export
- Single responsibility

## Styling
- Design tokens used (no arbitrary values)
- Utility ordering correct
- Responsive classes used
- No inline styles

## Accessibility
- Semantic HTML
- ARIA attributes where needed
- Form labels present
- Focus indicators

## TypeScript
- No any types
- Props fully typed
- Handler types correct

Report deviations with handbook section reference.