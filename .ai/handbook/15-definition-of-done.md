# Purpose

Define the Definition of Done for all features and tasks.

# Scope

Covers when work is considered complete for code, documentation, and testing.

# Principles

## Done Means

- **Working**: Meets requirements
- **Tested**: Coverage for critical paths
- **Reviewed**: Passes handbook standards
- **Merged**: Integrated safely

# Standards

## Code Complete

- [ ] Implements requirements fully
- [ ] Follows handbook standards (all sections)
- [ ] TypeScript compiles without errors
- [ ] PHP static analysis passes
- [ ] No lint errors

## Testing Complete

- [ ] Unit tests for business logic
- [ ] Component tests for UI
- [ ] Integration tests for features
- [ ] All tests passing
- [ ] Test coverage >= 80% for changed code

## Documentation Complete

- [ ] Inline types documented
- [ ] Complex logic explained
- [ ] README updated for feature
- [ ] API changes documented
- [ ] Breaking changes noted

## Review Complete

- [ ] Code reviewed
- [ ] Accessibility checked
- [ ] Performance verified
- [ ] Security reviewed
- [ ] Handbook standards verified

## Deployment Complete

- [ ] Migrations run successfully
- [ ] Assets built and minified
- [ ] Environment variables documented
- [ ] Monitoring configured
- [ ] Rollback plan exists

# Best Practices

- Use definition as PR template
- Automate verifiable checks
- Document incomplete work
- Require all checkboxes for merge
- Track definition violations

# Anti-patterns

- Merging without tests
- Skipping handbook review
- Undocumented breaking changes
- Deploying on Friday
- Ignoring failing checks

# Examples

Feature checklist:
```
✓ Component follows 05-component-architecture.md
✓ Uses design tokens from 04-design-system.md
✓ Accessibility per 13-accessibility.md
✓ Tests added
✓ Documentation updated
```

# Checklist

- [ ] All done criteria listed
- [ ] Checklists provided
- [ ] Gate requirements defined
- [ ] Automation opportunities noted
- [ ] Handbook ready for implementation

# Dependencies

All handbook documents (01-14), HANDBOOK_BLUEPRINT.md

# References

None