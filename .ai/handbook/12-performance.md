# Purpose

Define performance optimization standards for frontend and backend.

# Scope

Covers loading optimization, rendering performance, and Laravel performance.

# Principles

## Performance Goals

- **First Load**: Under 2 seconds
- **SPA Navigation**: Under 500ms
- **Bundle Size**: Minimal and tree-shaken
- **Database**: Efficient queries

# Standards

## Frontend Performance

### Code Splitting

- Route-based splitting via React.lazy
- Component-level splitting when >50KB
- Dynamic imports for heavy libraries

```tsx
const HeavyComponent = lazy(() => import('./HeavyComponent'));
```

### Images

- WebP format preferred
- Width/height attributes
- Lazy loading for below-fold

### React Performance

- useMemo for expensive calculations
- useCallback for handler refs
- React.memo for pure components
- Keys for list items

### Bundle Optimization

- Tree-shaking enabled
- Analyze bundle regularly
- Remove unused imports
- Dynamic imports for modals

## Backend Performance

### Queries

- Select only needed columns
- Eager load relationships
- Database indexes on searched columns
- Cache expensive queries

```php
Product::with('category')->select('id', 'name', 'price')->get();
```

### Caching

- Cache config and routes
- Query cache for reports
- Cache tags for invalidation
- Redis preferred for sessions

# Best Practices

- Profile before optimizing
- Measure real user performance
- Set performance budgets
- Monitor in production

# Anti-patterns

- Premature optimization
- Unnecessary re-renders
- N+1 queries
- Uncached expensive operations
- Heavy libraries on initial load

# Examples

```tsx
// Good: Memoized expensive calculation
const totalPrice = useMemo(() => 
  items.reduce((sum, item) => sum + item.price, 0),
  [items]
);
```

```php
// Good: Cached query
Cache::remember('products', 3600, fn() => Product::all());
```

# Checklist

- [ ] Frontend standards defined
- [ ] Backend standards defined
- [ ] Optimization patterns covered
- [ ] Anti-patterns documented
- [ ] Measurement approach included

# Dependencies

06-react.md, 08-laravel.md, HANDBOOK_BLUEPRINT.md

# References

None