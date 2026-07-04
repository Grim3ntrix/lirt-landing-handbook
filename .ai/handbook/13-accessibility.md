# Purpose

Define accessibility standards for all UI components and pages.

# Scope

Covers WCAG compliance, ARIA usage, keyboard navigation, and screen reader support.

# Principles

## Accessibility First

- **WCAG 2.1 AA**: Minimum compliance
- **Keyboard**: Full keyboard navigation
- **Screen Reader**: Semantic HTML and ARIA
- **Inclusive**: Consider all users

# Standards

## Semantic HTML

- Use proper heading hierarchy (h1-h6)
- Buttons for actions, links for navigation
- Form labels associated with inputs
- Landmark roles for layout

## ARIA Patterns

- aria-label for icon buttons
- aria-live for dynamic content
- aria-expanded for collapsible
- Role="alert" for notifications

## Focus Management

- Visible focus indicators
- Focus trap in modals
- Skip links for navigation
- Logical tab order

## Color Contrast

- Text: 4.5:1 minimum ratio
- UI components: 3:1 minimum
- Tested with tools
- Theme aware

## Keyboard Navigation

- All interactive elements reachable
- Escape closes modals
- Arrow keys for radio/select
- Enter triggers actions

## Forms

- Labels for all inputs
- Error messages announced
- Required fields indicated
- Auto-focus management

# Best Practices

- Test with keyboard only
- Screen reader testing monthly
- Color contrast validation
- Accessibility audits in CI
- Use semantic HTML over ARIA

# Anti-patterns

- Divs for buttons
- Missing form labels
- Insufficient color contrast
- Keyboard traps
- Ignoring focus states

# Examples

```tsx
// Good: Accessible button
<button 
  aria-label="Close"
  className="focus:outline-none focus:ring-2"
>
  <XIcon />
</button>

// Good: Form with labels
<label htmlFor="email">Email</label>
<input id="email" type="email" required />
```

# Checklist

- [ ] ARIA standards defined
- [ ] Semantic HTML covered
- [ ] Focus management documented
- [ ] WCAG requirements stated
- [ ] Testing approach included

# Dependencies

01-principles.md, 06-react.md, 09-tailwind.md, HANDBOOK_BLUEPRINT.md

# References

None