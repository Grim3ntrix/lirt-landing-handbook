# Purpose

Define React-specific standards and patterns for the project.

# Scope

Covers React best practices, hooks usage, component patterns, and TypeScript standards.

# Principles

## React Philosophy

- Functional components only
- Hooks for all state and side effects
- TypeScript for type safety
- Server-side rendering through Inertia

## Component Patterns

- Presentational components for UI
- Container components for data fetching
- Custom hooks for reusable logic
- Compound components for complex UI

# Standards

## Component Definition

- Use `function` declaration for components
- Arrow functions for handlers and inline exports
- Named exports only (no default exports)
- Props interface defined separately

## Hooks Standards

```tsx
// State hooks
const [value, setValue] = useState<T>(initial);

// Effect hooks
useEffect(() => {
  // cleanup return optional
}, [deps]);

// Context
const context = useContext(SomeContext);
```

## Event Handlers

- Handlers defined before return
- Use useCallback for expensive operations
- Handler names: handle[Event] (handleClick, handleChange)

## Conditional Rendering

```tsx
{condition && <Component />}
{status === 'loading' ? <Loading /> : <Component />}
```

## Lists

- Always use keys from data (id)
- Never use index as key
- Memoize when performant needed

## TypeScript Standards

- Strict mode enabled
- Interfaces for component props
- Type for API responses
- Avoid any - use unknown + type narrowing

# Best Practices

- Extract complex logic into custom hooks
- Keep useEffect dependencies explicit
- Use React.FC sparingly (no for components with children)
- Prefer controlled components
- Error boundaries for feature modules

# Anti-patterns

- Inline object creation in render
- Anonymous functions in JSX props
- Components over 200 lines
- Deep prop drilling (use context at 3+ levels)
- Side effects in render

# Examples

```tsx
interface UserCardProps {
  user: User;
  onEdit: (id: number) => void;
}

export function UserCard({ user, onEdit }: UserCardProps) {
  const handleClick = () => onEdit(user.id);
  
  return (
    <div className="p-4 border rounded">
      <h2>{user.name}</h2>
      <button onClick={handleClick}>Edit</button>
    </div>
  );
}
```

# Checklist

- [ ] Component patterns defined
- [ ] Hooks usage documented
- [ ] TypeScript standards set
- [ ] Common patterns covered
- [ ] Anti-patterns listed

# Dependencies

01-principles.md, 05-component-architecture.md, HANDBOOK_BLUEPRINT.md

# References

07-inertia.md