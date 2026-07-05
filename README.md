# LIRT Engineering Handbook

An opinionated engineering handbook for building modern applications with **L**aravel, **I**nertia.js, **R**eact, and **T**ailwind CSS. Includes architecture, coding standards, reusable patterns, AI workflows, and project blueprints.

## What Is This

The LIRT Engineering Handbook is a **single source of truth** for engineering decisions in your application. Every component, service, and pattern in your project should reference this handbook.

It also ships with **AI prompt standards** so that you — and every teammate — get consistent, high-quality results when collaborating with AI coding assistants.

## How to Use This Handbook

### 1. Read Before You Code

Before writing any code, read the relevant handbook documents. The full reading order is defined in `.ai/AGENTS.md`. At minimum:

- [`.ai/handbook/01-principles.md`](.ai/handbook/01-principles.md) — Core engineering values
- [`.ai/handbook/02-architecture.md`](.ai/handbook/02-architecture.md) — System architecture and data flow
- [`.ai/handbook/03-folder-structure.md`](.ai/handbook/03-folder-structure.md) — Where files live
- [`.ai/handbook/04-design-system.md`](.ai/handbook/04-design-system.md) — Design tokens and styling rules
- [`.ai/handbook/05-component-architecture.md`](.ai/handbook/05-component-architecture.md) — Component patterns
- [`.ai/handbook/11-ai-workflow.md`](.ai/handbook/11-ai-workflow.md) — How to work with AI using this handbook

### 2. Reference It When Prompting AI

When asking an AI assistant to generate code, **always include the relevant handbook references in your prompt**. This gives the AI the context it needs to produce output that matches your standards.

## Prompt Standards

This repository defines strict prompt standards to ensure consistent, high-quality AI-generated code. Every prompt should follow these rules.

### Prompt Anatomy

A good prompt has three parts:

1. **Task** — What you want done (create, refactor, review, optimize).
2. **Context** — Which handbook documents apply.
3. **Criteria** — Explicit checklist the AI must satisfy before responding.

### Prompt Template

Use this structure for every AI interaction:

```markdown
[TASK] — e.g., "Create a new React component for billing"

## Context
Read and follow:
- [x] `.ai/handbook/05-component-architecture.md`
- [x] `.ai/handbook/04-design-system.md`
- [x] `.ai/handbook/06-react.md`

## Requirements
[Describe what the component/feature should do]

## Standards
- Function declaration for components
- Named export only
- Design tokens for all styling
- TypeScript strict mode compatible
- No inline comments

## Review Self-Check
- [ ] Matches component-architecture.md
- [ ] Uses design tokens from design-system.md
- [ ] No any types
- [ ] Under 100 lines
```

### Prompt Best Practices

**Do:**

- Name the exact handbook documents that apply to your task.
- Provide a concrete example of the expected output shape.
- Include a self-check checklist so the AI validates its own work.
- Be specific about file paths, naming conventions, and constraints.
- Combine with existing prompt templates in `.ai/prompts/` when they fit.

**Don't:**

- Give vague instructions like "make it look nice."
- Assume the AI knows your project conventions.
- Skip the self-check checklist.
- Add inline comments to generated code (the handbook bans them).
- Accept output that hasn't been checked against the handbook.

### Built-in Prompt Templates

Use these as starting points for common tasks:

| Task | Template |
|------|----------|
| Create a component | `.ai/prompts/create-component.md` |
| Refactor a component | `.ai/prompts/refactor-component.md` |
| Optimize a component | `.ai/prompts/optimize-component.md` |
| Review a component | `.ai/prompts/review-component.md` |

## Good Prompt Examples

### Good: Component Creation

```text
Task: Create a UserCard component for the admin dashboard.

Read:
- .ai/handbook/05-component-architecture.md
- .ai/handbook/04-design-system.md
- .ai/handbook/06-react.md

Requirements:
- Display user avatar, name, email, and role badge
- Props: user object with name, email, avatarUrl, role
- Click navigates to /admin/users/:id

Standards:
- Function declaration
- Named export
- Design tokens for colors and spacing
- aria-label on interactive elements
- TypeScript props interface

Self-check:
- [ ] 05-component-architecture.md compliant
- [ ] 04-design-system.md tokens only
- [ ] No any types
- [ ] Under 80 lines
```

### Good: Component Refactor

```text
Task: Refactor the DashboardStats component.

Read:
- .ai/handbook/05-component-architecture.md
- .ai/handbook/01-principles.md

Requirements:
- Extract data fetching into a custom hook
- Separate chart logic from layout

Standards:
- Single responsibility per function
- Reusable custom hook named useDashboardStats
- No framework-specific hacks

Self-check:
- [ ] Extracted custom hook
- [ ] No business logic in component body
- [ ] Naming matches conventions
- [ ] Tests still pass
```

### Bad: Vague Prompt (Avoid)

```text
Task: Make a nice dashboard card thing.

It should look good and be responsive.

Don't worry about conventions.
```

## Handbook Structure

```
.ai/
├── AGENTS.md                      # Kilo agent bootstrap file
├── HANDBOOK_BLUEPRINT.md          # Master blueprint for all handbook docs
├── handbook/                      # Canonical engineering documents
│   ├── 01-principles.md
│   ├── 02-architecture.md
│   ├── 03-folder-structure.md
│   ├── 04-design-system.md
│   ├── 05-component-architecture.md
│   ├── 06-react.md
│   ├── 07-inertia.md
│   ├── 08-laravel.md
│   ├── 09-tailwind.md
│   ├── 10-nwidart.md
│   ├── 11-ai-workflow.md
│   ├── 12-performance.md
│   ├── 13-accessibility.md
│   ├── 14-code-review.md
│   └── 15-definition-of-done.md
├── landing-pages/                 # Landing page templates
│   ├── LANDING_BOOTSTRAP.md
│   ├── 01-minimal-saas/
│   ├── 02-modern-gradient/
│   └── ...
└── prompts/                       # AI prompt templates
    ├── create-component.md
    ├── refactor-component.md
    ├── optimize-component.md
    └── review-component.md
```

## Getting Started

1. **Clone this repo** into your project root.
2. **Review the handbook** — at minimum, read `01-principles.md` through `05-component-architecture.md`.
3. **Copy the prompt template** above into your AI assistant for every new request.
4. **Follow the checklist** — never skip the self-check at the end of a prompt.

## Contributing

To propose changes to the handbook:

1. Open a PR with the proposed document change.
2. Reference the affected handbook section in your PR description.
3. Ensure your change doesn't contradict an already-approved standard.

## License

See [LICENSE.md](LICENSE.md).
