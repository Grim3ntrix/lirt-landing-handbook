# Purpose

Define AI-assisted development workflow and standards.

# Scope

Covers agent expectations, validation, and review processes.

# Principles

## AI Workflow

- **Sequential**: Follow phase order
- **Reviewed**: Each document reviewed before proceeding
- **Validated**: Code checked against handbook
- **Consistent**: Standards applied uniformly

# Standards

## Document Generation

- One document at a time
- Follow template structure
- Respect dependency order
- No skipping phases

## Code Generation

- Reference handbook before writing code
- Follow established patterns
- Type everything in TypeScript
- No inline comments unless requested

## Review Process

1. Structural Review - Does it match patterns?
2. Consistency Review - Any contradictions?
3. Dependency Review - All references checked?
4. Improvement Pass - Polish needed?
5. Final Review - Ready for next phase?

## Agent Protocol

- Load AGENTS.md before any task
- Check document status before implementation
- Flag conflicts with handbook
- Request clarification on ambiguities

# Best Practices

- Review every file against handbook
- Ask before deviating from standards
- Document deviations explicitly
- Validate folder structure matches docs

# Anti-patterns

- Skipping handbook before coding
- Ignoring established patterns
- Generating code without review
- Conflicting implementations

# Examples

```
Before coding:
1. Read .ai/handbook/
2. Check relevant standards
3. Generate code matching patterns
4. Review output
5. Proceed
```

# Checklist

- [ ] Workflow documented
- [ ] Review process defined
- [ ] Agent protocol established
- [ ] Validation steps clear
- [ ] Anti-patterns listed

# Dependencies

HANDBOOK_BLUEPRINT.md

# References

14-code-review.md