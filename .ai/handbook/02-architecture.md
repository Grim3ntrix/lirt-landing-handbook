# Purpose

Define the high-level architecture patterns and decisions for the application.

# Scope

Covers frontend-backend integration, data flow, module organization, and architectural boundaries.

# Principles

## System Architecture

- **Frontend**: Feature-first React with Inertia.js for SPA experience
- **Backend**: Laravel service-based architecture
- **State**: Server state via Laravel, client state via React hooks
- **Routing**: Laravel handles all routing, React components render via Inertia

## Integration Patterns

- Inertia.js manages client-server communication
- Components receive props from Laravel controllers
- No direct API calls - all data through server-side rendering
- Form submissions via Inertia middleware

# Standards

## Frontend Architecture

- Features organized in `resources/js/Features/`
- Shared UI components in `resources/js/Components/`
- Layout components in `resources/js/Layouts/`
- Pages in `resources/js/Pages/` reflect feature structure

## Backend Architecture

- Controllers handle HTTP requests only
- Business logic in Services
- Data access in Repositories
- Optional: nWidart modules for bounded contexts

## Data Flow

- Unidirectional: Controller → Service → Model → Component
- Validation at controller entry point
- Authorization at service layer
- Props passed explicitly to components

# Best Practices

- Keep controllers thin (under 50 lines)
- Services handle one domain concern
- Components remain presentational
- Use Laravel's built-in features over custom code

# Anti-patterns

- Fat controllers with business logic
- Direct database queries in controllers
- Components fetching their own data
- Cross-feature dependencies in components
- Circular dependencies between layers

# Examples

```
Laravel Request → Route → Controller 
    → Service → Model 
    → Inertia::render('Feature/Page', props)
    → React Component renders props
```

# Checklist

- [ ] Architecture clearly defined
- [ ] Frontend pattern specified
- [ ] Backend pattern specified
- [ ] Data flow documented
- [ ] No gaps in boundaries

# Dependencies

01-principles.md, HANDBOOK_BLUEPRINT.md

# References

03-folder-structure.md, 05-component-architecture.md, 02-laravel.md