# Purpose

Define optional nWidart Laravel Modules usage for modular backend architecture.

# Scope

Covers module structure, organization, and integration patterns.

# Principles

## Modularity

- **Optional**: Use for bounded contexts
- **Independent**: Modules work standalone
- **Consistent**: Same patterns across modules
- **Frontend Independent**: Modules don't dictate frontend structure

# Standards

## Module Structure

```
Modules/
├── Inventory/
│   ├── Config/
│   ├── Database/
│   │   ├── migrations/
│   │   ├── seeders/
│   │   └── factories/
│   ├── Entities/
│   ├── Http/
│   │   ├── Controllers/
│   │   ├── Middleware/
│   │   └── Requests/
│   ├── Repositories/
│   ├── Services/
│   ├── Tests/
│   ├── composer.json
│   └── module.json
```

## Module Creation

```bash
php artisan module:make Inventory
php artisan module:make-controller ProductController Inventory
```

## Module Registration

- Modules auto-discovered
- Add to composer.json autoload
- Publish migrations if needed

## Frontend Integration

- Frontend features independent of modules
- Share types through common package or API resources
- Routes defined in module but pages in frontend features

## Module Naming

- Singular nouns (Inventory, User, Product)
- PascalCase directory names
- Clear domain boundaries

# Best Practices

- One module per bounded context
- Keep modules loosely coupled
- Use module events for cross-module communication
- Test modules in isolation
- Document module APIs

# Anti-patterns

- Too many small modules
- Modules depending on each other's internals
- Mixed concerns in single module
- Breaking frontend independence
- Circular module dependencies

# Examples

```php
// Module controller
namespace Modules\Inventory\Http\Controllers;

class ProductController extends Controller
{
    public function __construct(ProductService $service) 
    {
        $this->service = $service;
    }
}
```

# Checklist

- [ ] Module structure defined
- [ ] Creation commands documented
- [ ] Frontend integration covered
- [ ] Naming conventions set
- [ ] Coupling guidelines established

# Dependencies

02-architecture.md, 08-laravel.md, HANDBOOK_BLUEPRINT.md

# References

None