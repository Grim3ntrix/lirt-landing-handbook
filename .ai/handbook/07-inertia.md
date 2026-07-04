# Purpose

Define Inertia.js integration standards and patterns.

# Scope

Covers Inertia setup, page navigation, form handling, and shared data patterns.

# Principles

## Inertia Patterns

- **Seamless SPA**: No full page reloads
- **Server Driven**: All data from Laravel
- **Progressive Enhancement**: Works without JS
- **Shared State**: Persistent layouts

# Standards

## Inertia Setup

```tsx
// app.tsx
import { createInertiaApp } from '@inertiajs/react';

createInertiaApp({
  resolve: name => {
    const pages = import.meta.glob('./Pages/**/*.tsx');
    return pages[`./Pages/${name}.tsx`]();
  },
  setup({ el, App, props }) {
    // hydrate root element
  },
});
```

## Page Props

```tsx
// Always receive props from controller
interface PageProps {
  user: User;
  flash: FlashMessage;
}
```

## Navigation

```tsx
import { Link, router } from '@inertiajs/react';

// Links
<Link href="/dashboard" className="nav-link">Dashboard</Link>

// Programmatic navigation
router.visit('/path', { method: 'get' });
router.post('/resource', data);
```

## Form Handling

```tsx
import { useForm } from '@inertiajs/react';

function MyForm() {
  const { data, setData, post, processing, errors } = useForm({
    name: '',
    email: ''
  });
  
  const submit = (e: FormEvent) => {
    e.preventDefault();
    post('/users');
  };
}
```

## Shared Data

```tsx
// app.tsx
import { usePage } from '@inertiajs/react';

const { props: { user } } = usePage();
```

# Best Practices

- Use Inertia's useForm for all forms
- Handle validation errors from backend
- Preserve scroll on navigation
- Use partial reloads when possible
- Flash messages for user feedback

# Anti-patterns

- Direct fetch/XHR calls
- Ignoring Inertia loading states
- Not handling validation errors
- Breaking SPA experience with window.location

# Examples

```tsx
// Good: Form with Inertia
function LoginForm() {
  const { data, setData, post, errors } = useForm({
    email: '',
    password: ''
  });
  
  return (
    <form onSubmit={e => { e.preventDefault(); post('/login'); }}>
      <input 
        value={data.email}
        onChange={e => setData('email', e.target.value)}
      />
      {errors.email && <span>{errors.email}</span>}
    </form>
  );
}
```

# Checklist

- [ ] Setup pattern defined
- [ ] Navigation covered
- [ ] Form handling documented
- [ ] Shared data pattern
- [ ] Error handling included

# Dependencies

01-principles.md, 06-react.md, HANDBOOK_BLUEPRINT.md

# References

08-laravel.md