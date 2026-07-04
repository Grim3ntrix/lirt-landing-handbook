# Purpose

Prompt template for creating new components following handbook standards.

# Scope

Use this template when generating React components.

# Instructions

Before creating any component:
1. Read `.ai/handbook/05-component-architecture.md`
2. Read `.ai/handbook/04-design-system.md`
3. Read `.ai/handbook/06-react.md`

# Template

Create a component with these requirements:

## Structure
- Function component with function declaration
- Props interface defined
- Named export only
- File in correct feature folder

## Standards
- Types for all props (TypeScript)
- Design tokens for colors/styling
- Accessibility attributes
- No inline comments
- Follow utility ordering (09-tailwind.md)

## Review Self-Check
- [ ] Matches 05-component-architecture.md
- [ ] Uses design tokens from 04-design-system.md
- [ ] TypeScript strict mode compatible
- [ ] No magic values
- [ ] Under 100 lines