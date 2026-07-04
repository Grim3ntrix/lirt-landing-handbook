# Purpose

Define the design system including colors, typography, spacing, and component tokens.

# Scope

Covers Tailwind CSS configuration, design tokens, and UI component standards.

# Principles

## Design Philosophy

- **System First**: Consistent design through tokens and constraints
- **Utility Driven**: Leverage Tailwind's utility classes
- **Theme Ready**: Support light/dark mode variants
- **Accessible**: Meet WCAG standards by default

# Standards

## Color Palette

```
Primary: Blue (500-600 range)
Secondary: Gray (400-500 range)
Success: Green (500)
Warning: Amber (500)
Error: Red (500)
```

## Typography

- Font family: System stack (Inter, system-ui, sans-serif)
- Sizes: text-xs, text-sm, text-base, text-lg, text-xl, text-2xl
- Font weights: font-normal, font-medium, font-semibold, font-bold

## Spacing Scale

Use Tailwind's default spacing scale (1-96):
- xs: 1-2 (gap-1, p-1)
- sm: 3-4 (gap-3, p-3)
- md: 5-6 (gap-5, p-5)
- lg: 8-10 (gap-8, p-8)

## Border Radius

- Sharp: rounded-none
- Default: rounded-md
- Pill: rounded-full

## Shadows

- Subtle: shadow-sm
- Default: shadow
- Elevated: shadow-md
- Floating: shadow-lg

# Best Practices

- Use semantic color names in components
- Define component variants (primary, secondary, ghost)
- Maintain contrast ratios > 4.5:1 for text
- Use CSS variables for themeable values

# Anti-patterns

- Arbitrary values (avoid inline styles)
- Hardcoded colors outside design system
- Inconsistent button styles
- Missing focus states

# Examples

```tsx
// Button variants using design tokens
const buttonClasses = {
  primary: "bg-blue-600 text-white hover:bg-blue-700",
  secondary: "bg-gray-200 text-gray-900 hover:bg-gray-300",
  ghost: "bg-transparent text-gray-700 hover:bg-gray-100"
};
```

# Checklist

- [ ] Color palette defined
- [ ] Typography scale established
- [ ] Spacing system documented
- [ ] Component tokens specified
- [ ] Accessibility considerations included

# Dependencies

01-principles.md, HANDBOOK_BLUEPRINT.md

# References

04-design-system.md, 09-tailwind.md