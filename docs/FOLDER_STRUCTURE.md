# OOP Folder Structure Best Practices

## Folder Structure

```
project/
│
├── src/                    # Source code
│   ├── domain/             # Core domain models and business logic
│   │   ├── models/         # Business/domain models
│   │   ├── value_objects/  # Value objects (e.g., immutable types)
│   │   └── events/         # Domain events
│   │
│   ├── application/        # Application-specific logic
│   │   ├── use_cases/      # Use case logic
│   │   ├── commands/       # Command objects for task-based actions
│   │   ├── queries/        # Query objects for fetching data
│   │   ├── services/       # Business logic and reusable services
│   │   └── factories/      # Factory classes for object creation
│   │
│   ├── infrastructure/     # Technical details and external system interaction
│   │   ├── repositories/   # Database access and data persistence
│   │   ├── adapters/       # Adapter pattern for external systems
│   │   ├── middleware/     # Middleware logic (e.g., for HTTP requests)
│   │   ├── cache/          # Caching logic
│   │   ├── guards/         # Runtime checks for access or rules
│   │   └── exceptions/     # Custom exception classes
│   │
│   ├── api/                # API-specific components
│   │   ├── controllers/    # API controllers
│   │   ├── resources/      # Resources for API responses
│   │   └── serializers/    # Serialization logic for API data
│   │
│   ├── shared/             # Shared resources and reusable components
│   │   ├── dto/            # Data Transfer Objects
│   │
│   ├── utilities/          # General-purpose utilities
│   │
│   ├── config/             # Configuration files
│   │
│   └── tests/              # Test cases
│       ├── unit/           # Unit tests
│       ├── integration/    # Integration tests
│       ├── e2e/            # End-to-end tests
│       ├── fixtures/       # Test data
│       └── mocks/          # Mock objects
│
├── locales/                # Internationalization/localization
│
├── docs/                   # Documentation
│
├── public/                 # Publicly accessible files (for web apps)
│   ├── css/
│   ├── js/
│   └── images/
│
└── vendor/                 # Third-party libraries (e.g., pip, npm)
```
