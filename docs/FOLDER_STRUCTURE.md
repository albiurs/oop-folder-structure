# OOP Folder Structure Best Practices

## Folder Structure

```
project/
│
├── config/             # Configuration files
│   ├── env/            # Environment configuration
│
├── docs/                   # Documentation
│
├── locales/                # Internationalization/localization
│
├── public/                 # Publicly accessible files (for web apps)
│   ├── css/
│   ├── js/
│   └── images/
│
├── src/                    # Source code
│   │
│   ├── api/                # API-specific components
│   │   ├── controllers/    # API controllers
│   │   ├── resources/      # Resources for API responses
│   │   └── serializers/    # Serialization logic for API data
│   │
│   ├── application/        # Application-specific logic
│   │   ├── commands/       # Command objects for task-based actions
│   │   ├── factories/      # Factory classes for object creation
│   │   ├── listeners/        # Event listeners (focused actions for events)
│   │   ├── queries/        # Query objects for fetching data
│   │   ├── services/       # Business logic and reusable services
│   │   ├── subscribers/      # Event subscribers (manage multiple events)
│   │   └── use_cases/      # Use case logic
│   │
│   ├── domain/             # Core domain models and business logic
│   │   ├── events/         # Domain events
│   │   ├── models/         # Business/domain models
│   │   └── value_objects/  # Value objects (e.g., immutable types)
│   │
│   ├── infrastructure/     # Technical details and external system interaction
│   │   ├── adapters/       # Adapter pattern for external systems
│   │   ├── cache/          # Caching logic
│   │   ├── events/           # Event dispatching infrastructure
│   │   ├── exceptions/     # Custom exception classes
│   │   ├── guards/         # Runtime checks for access or rules
│   │   ├── localization/   # Handles locales and related logic
│   │   ├── middleware/     # Middleware logic (e.g., for HTTP requests)
│   │   └── repositories/   # Database access and data persistence
│   │
│   ├── jobs/               # Asynchronous or background tasks
│   │
│   ├── policies/           # Authorization policies
│   │
│   ├── shared/                      # Contains reusable utilities, adapters, and shared components
│   │   ├── adapters/                # Interfaces or wrappers for external libraries or APIs
│   │   ├── dto/                     # Data Transfer Objects for inter-layer communication
│   │   ├── exceptions/              # Custom exception classes for consistent error handling
│   │   ├── helpers/                 # General-purpose utility functions
│   │
│   ├── tests/              # Test cases
│   │   ├── e2e/            # End-to-end tests
│   │   ├── fixtures/       # Test data
│   │   ├── integration/    # Integration tests
│   │   ├── mocks/          # Mock objects
│   │   └── unit/           # Unit tests
│   │
│   └── utilities/          # General-purpose utilities
│       ├── validator.py
│       ├── date_formatter.py
│       └── logger.py
│
└── vendor/                 # Third-party libraries (e.g., pip, npm)
```
