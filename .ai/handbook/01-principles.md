# Purpose

Establish the core engineering principles that guide all technical decisions in this project.

# Scope

This document defines foundational principles for the Laravel + React + Inertia.js + Tailwind CSS technology stack.

# Principles

## Core Engineering Values

1. **Simplicity First** - Prefer simple, readable solutions over complex abstractions
2. **Explicit over Implicit** - Make intentions clear through code and naming
3. **Consistency** - Maintain uniform patterns across frontend and backend
4. **Separation of Concerns** - Clear boundaries between features, layers, and responsibilities
5. **Progressive Enhancement** - Build core functionality first, enhance progressively
6. **Accessibility by Default** - Consider a11y from the start
7. **Performance Mindful** - Optimize for user experience, not benchmarks

# Standards

## Code Standards

- Write code for the next developer who will read it
- Use descriptive names for variables, functions, and classes
- Keep functions under 50 lines when possible
- One level of abstraction per function
- Avoid premature abstraction

## Architecture Standards

- Feature-first organization for React components
- Service-oriented architecture for Laravel
- Stateless components where possible
- Explicit data flow

## Documentation Standards

- Every public function must have a docstring
- Complex logic requires inline comments
- README for each feature module
- Architecture decisions documented

# Best Practices

- Start with the simplest solution that satisfies requirements
- Refactor when duplication is found, not before
- Document decisions in code comments or ADRs
- Prefer composition over inheritance
- Use TypeScript for type safety on frontend

# Anti-patterns

- Over-engineering solutions
- Magic strings and numbers
- Deeply nested conditionals
- Premature optimization
- Framework-specific hacks
- Tight coupling between features

# Examples

```php
// Good: Explicit, simple
class UserService 
{
    public function create(array $data): User
    {
        return User::create($data);
    }
}

// Avoid: Over-abstracted
class AbstractFactoryManagerFactoryProxy {}
```

```tsx
// Good: Simple component
function Button({ children, onClick }: ButtonProps) {
    return (
        <button onClick={onClick} className="btn-primary">
            {children}
        </button>
    );
}
```

# Checklist

- [ ] Principles clearly defined
- [ ] Standards are actionable
- [ ] Examples are relevant to stack
- [ ] No contradictions with blueprint

# Dependencies

HANDBOOK_BLUEPRINT.md

# References

02-architecture.md