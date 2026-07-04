# Purpose

Prompt template for optimizing components.

# Scope

Use this template when improving component performance.

# Instructions

Reference these documents:
1. `.ai/handbook/12-performance.md`
2. `.ai/handbook/06-react.md`

# Template

Optimize the component checking:

## React Performance
- useMemo for expensive calculations
- useCallback for handler refs
- React.memo for pure components
- Keys for list items

## Bundle Size
- Unused imports removed
- Code splitting where applicable
- Heavy libraries lazy loaded

## Rendering
- Avoid anonymous functions in JSX
- Stable references in useEffect deps
- Conditional rendering optimized

## Backend
- Query optimization (if applicable)
- Eager loading relationships
- Caching opportunities