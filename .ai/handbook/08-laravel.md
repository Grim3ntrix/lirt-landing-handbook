# Purpose

Define Laravel backend standards including controllers, services, models, and routing.

# Scope

Covers Laravel coding patterns, architecture, and integration with Inertia.js.

# Principles

## Laravel Patterns

- **Thin Controllers**: Handle requests only
- **Fat Services**: Business logic lives here
- **Explicit**: Clear method and class names
- **Testable**: Separated concerns enable testing

## Request Lifecycle

Request → Route → Controller → Service → Model → Response → Inertia → React

# Standards

## Controllers

- One controller per resource/feature
- Dependency injection via constructor
- Return only Inertia responses
- No business logic in controllers

```php
class InventoryController extends Controller
{
    public function __construct(
        private InventoryService $service
    ) {}
    
    public function index(): Response
    {
        $products = $this->service->getAll();
        return Inertia::render('Inventory/Index', compact('products'));
    }
}
```

## Services

- Handle business logic
- One service per domain
- Inject repositories if needed
- Return data, not responses

```php
class InventoryService
{
    public function getAll(): Collection
    {
        return Product::all();
    }
}
```

## Models

- One model per table
- Relationships explicitly defined
- Casts for data types
- No query logic in models

## Requests (Validation)

- FormRequest for validation
- Authorization rules in FormRequest
- Typed properties

```php
class StoreProductRequest extends FormRequest
{
    public function rules(): array
    {
        return [
            'name' => ['required', 'string', 'max:255'],
            'price' => ['required', 'numeric', 'min:0'],
        ];
    }
}
```

## Routes

- Resource routes where possible
- Named routes
- Grouped by feature

```php
Route::get('/inventory', [InventoryController::class, 'index'])->name('inventory.index');
```

# Best Practices

- Type hint all parameters and returns
- Use dependency injection
- Keep models thin
- Validate at the edge (FormRequest)
- Use Laravel's built-in features

# Anti-patterns

- Fat controllers with logic
- Raw queries in controllers
- Validation in controllers
- Logic in views/blade files
- Global scope or accessors for queries

# Examples

```php
// Controller
class ProductController extends Controller
{
    public function store(StoreProductRequest $request): Response
    {
        $product = $this->service->create($request->validated());
        return redirect()->route('products.index')
            ->with('success', 'Product created');
    }
}
```

# Checklist

- [ ] Controller standards defined
- [ ] Service pattern documented
- [ ] Model standards covered
- [ ] Validation pattern established
- [ ] Route conventions set

# Dependencies

01-principles.md, 02-architecture.md, HANDBOOK_BLUEPRINT.md

# References

07-inertia.md, 10-nwidart.md