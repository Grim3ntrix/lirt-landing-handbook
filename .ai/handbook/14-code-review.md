# Purpose

Define code review standards and checklist for all contributions.

# Scope

Covers review process, standards verification, and quality gates.

# Principles

## Review Focus

- **Correctness**: Does it solve the problem?
- **Standards**: Follows handbook?
- **Quality**: Maintainable and readable?
- **Security**: No vulnerabilities?

# Standards

## Review Checklist

### Frontend
- [ ] TypeScript types present and correct
- [ ] Component follows 05-component-architecture.md
- [ ] Tailwind classes follow 09-tailwind.md
- [ ] Accessibility standards from 13-accessibility.md
- [ ] No hardcoded values (use design tokens)

### Backend
- [ ] Controller thin (under 50 lines) per 08-laravel.md
- [ ] Service handles business logic
- [ ] Validation in FormRequest
- [ ] Routes use named routes
- [ ] No raw queries in controllers

### General
- [ ] No inline comments (unless requested)
- [ ] Props/explicit parameters
- [ ] No magic values
- [ ] Error handling present
- [ ] Tests written or updated

## Review Process

1. **Structural Review**: Matches patterns?
2. **Consistency Review**: No conflicts?
3. **Dependency Review**: References correct?
4. **Quality Review**: Readable and simple?
5. **Approval**: Ready to proceed?

## AI Review Protocol

- Check against relevant handbook sections
- Flag deviations immediately
- Suggest improvements not just issues
- Verify folder structure matches docs

## Blocking Issues

- Security vulnerabilities
- Missing type safety
- Breaking established patterns
- Performance regressions
- Accessibility failures

# Best Practices

- Review before merge
- Document architectural decisions
- Link to handbook sections
- Keep reviews constructive
- Automate checks where possible

# Anti-patterns

- Skipping review
- Approving without checking standards
- Personal preference over standards
- Ignoring repeated violations
- Reviewing own large PRs

# Examples

Good review comment:
```
Component uses hardcoded color. Per 04-design-system.md, use semantic tokens.
Change bg-red-500 to bg-error.
```

# Checklist

- [ ] Review checklist complete
- [ ] Blocking issues defined
- [ ] Process documented
- [ ] AI protocol specified
- [ ] Feedback guidelines included

# Dependencies

HANDBOOK_BLUEPRINT.md, all handbook documents

# References

11-ai-workflow.md, 14-code-review.md