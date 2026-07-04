# Purpose

Define the exact folder structure for both Laravel backend and React frontend.

# Scope

Covers all directories, naming conventions, and file organization patterns.

# Principles

## Organization Strategy

- **Feature-first**: Group by domain functionality, not by file type
- **Separation**: Clear boundaries between features and shared code
- **Consistency**: Same patterns frontend and backend
- **Discoverability**: Easy to find related code

# Standards

## Frontend Structure (`resources/js/`)

```
resources/js/
├── app.tsx                    # App entry point
├── bootstrap.ts               # Inertia setup
├── hooks/                     # Shared React hooks
│   ├── useForm.ts
│   └── useAuth.ts
├── Components/                # Shared UI components
│   ├── Button/
│   ├── Card/
│   └── Form/
├── Features/                  # Feature modules
│   ├── Landing/
│   │   ├── Components/
│   │   ├── hooks/
│   │   └── LandingPage.tsx
│   ├── Inventory/
│   │   ├── Components/
│   │   ├── hooks/
│   │   └── InventoryPage.tsx
│   └── Authentication/
├── Layouts/                   # Layout components
│   ├── AppLayout.tsx
│   └── AuthLayout.tsx
└── Pages/                     # Inertia pages
    └── (mirrors feature structure)
```

## Backend Structure (`app/`)

```
app/
├── Http/
│   ├── Controllers/
│   │   ├── LandingController.php
│   │   ├── InventoryController.php
│   │   └── Auth/
│   └── Middleware/
├── Services/
│   ├── LandingService.php
│   └── InventoryService.php
├── Models/
├── Repositories/
└── (Modules/ if using nWidart)
```

## Module Structure (nWidart)

```
Modules/
├── Inventory/
│   ├── Http/Controllers/
│   ├── Services/
│   └── Views/
└── Auth/
```

# Best Practices

- Use kebab-case for folder names
- One component per file
- Index files for clean exports
- Feature folders contain all related code

# Anti-patterns

- Mixed feature code in shared folders
- Generic names like "utils" or "helpers"
- Deep nesting over 3 levels
- Inconsistent naming across features

# Examples

Feature folder structure:
```
Features/Inventory/
├── Components/
│   ├── ProductCard/
│   │   ├── ProductCard.tsx
│   │   └── index.ts
├── hooks/
│   └── useInventory.ts
└── InventoryList.tsx
```

# Checklist

- [ ] Folder paths clearly defined
- [ ] Naming conventions specified
- [ ] Feature-first structure shown
- [ ] Module structure optional
- [ ] Paths align with architecture

# Dependencies

02-architecture.md, HANDBOOK_BLUEPRINT.md

# References

05-component-architecture.md, 08-laravel.md