# Purpose

Define Tailwind CSS configuration, utility usage, and styling standards.

# Scope

Covers Tailwind setup, custom configuration, component styling, and responsive patterns.

# Principles

## Tailwind Philosophy

- **Utility First**: Compose styles from utilities
- **Extract When Repeated**: Create components for repeated patterns
- **Responsive**: Mobile-first approach
- **Consistent**: Use design tokens

# Standards

## Configuration

```js
// tailwind.config.js
module.exports = {
  content: ['./resources/**/*.tsx', './resources/**/*.blade.php'],
  theme: {
    extend: {
      colors: {
        primary: { /* 50-900 scale */ }
      }
    }
  },
  plugins: []
}
```

## Utility Ordering

Order within className:
1. Layout (flex, grid, block)
2. Spacing (margin, padding)
3. Sizing (width, height)
4. Typography (text, font)
5. Colors (bg, text)
6. Borders (rounded, border)
7. Effects (shadow, opacity)

## Responsive Classes

- Mobile first: No prefix = mobile
- sm: 640px+
- md: 768px+
- lg: 1024px+
- xl: 1280px+

## Component Styling

```tsx
// Extract repeated patterns
const cardClasses = "bg-white rounded-lg p-4 shadow";

// Conditionally apply
className={`btn ${variant === 'primary' ? 'bg-blue-600' : 'bg-gray-200'}`}
```

## Arbitrary Values

- Avoid when design system covers it
- Acceptable for one-off values
- Document arbitrary values used

# Best Practices

- Use @apply sparingly (for repeated patterns only)
- Enable JIT mode for development
- Purge unused styles in production
- Theme through CSS variables
- Use semantic color names

# Anti-patterns

- Inline styles over utilities
- Arbitrary colors instead of design tokens
- @apply in every component
- Media queries over responsive classes
- Hardcoded values over theme scale

# Examples

```tsx
<div className="flex items-center justify-between p-4 bg-white rounded-lg shadow-md">
  <h2 className="text-lg font-semibold text-gray-900">Title</h2>
  <button className="px-4 py-2 bg-blue-600 text-white rounded hover:bg-blue-700">
    Action
  </button>
</div>
```

# Checklist

- [ ] Configuration documented
- [ ] Utility ordering standard
- [ ] Responsive patterns defined
- [ ] Component patterns covered
- [ ] Best practices listed

# Dependencies

04-design-system.md, HANDBOOK_BLUEPRINT.md

# References

09-tailwind.md