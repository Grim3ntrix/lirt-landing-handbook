# Purpose

Define React component architecture patterns, including structure, state management, and reusability.

# Scope

Covers component design patterns, hooks, props, and integration with Inertia.js.

# Principles

## Component Design

- **Presentational First**: Components receive props, render UI
- **Single Responsibility**: One reason to change
- **Composable**: Small components combine into larger ones
- **Type Safe**: TypeScript interfaces for all props

## State Management

- Server state through Laravel props
- Local state with useState/useReducer
- Shared state through context/hooks
- No global state management (Redux, etc.)

# Standards

## Component Structure

```tsx
function ComponentName({ prop1, prop2 }: ComponentProps) {
  // Hooks
  const [state, setState] = useState(initial);
  
  // Handlers
  const handleClick = () => {};
  
  // Render
  return (
    <div className="component-wrapper">
      {/* JSX */}
    </div>
  );
}
```

## Props Interface

```tsx
interface ComponentNameProps {
  title: string;
  items: Item[];
  onAction: (id: number) => void;
  variant?: 'primary' | 'secondary';
}

function ComponentName({ title, items, onAction, variant = 'primary' }: ComponentNameProps)
```

## File Organization

```
ComponentName/
├── ComponentName.tsx
├── index.ts
├── ComponentName.test.tsx
└── types.ts (if complex)
```

# Best Practices

- Export through index.ts for clean imports
- Keep components under 100 lines
- Extract hooks for reusable logic
- Use function declarations, not arrow functions for components
- Prefer composition over inheritance

# Anti-patterns

- Components over 200 lines
- Props drilling beyond 2 levels
- Anonymous functions in JSX
- Inline object/array creation in props
- Components with too many responsibilities

# Examples

```tsx
// Good: Focused component
function ProductCard({ product }: { product: Product }) {
  return (
    <div className="bg-white rounded-lg p-4 shadow">
      <h3 className="font-semibold">{product.name}</h3>
      <p className="text-gray-600">{product.price}</p>
    </div>
  );
}
```

# Checklist

- [ ] Component structure defined
- [ ] Props pattern established
- [ ] File organization specified
- [ ] TypeScript usage mandated
- [ ] Anti-patterns documented

# Dependencies

01-principles.md, 02-architecture.md, HANDBOOK_BLUEPRINT.md

# References

06-react.md, 07-inertia.md