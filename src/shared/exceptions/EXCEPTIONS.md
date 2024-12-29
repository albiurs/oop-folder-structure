# Contains reusable utilities, adapters, and shared components

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── shared/                      # Contains reusable utilities, adapters, and shared components
│   │   ├── exceptions/              # Custom exception classes for consistent error handling
│   │   │   ├── validation_error.py   # Exception for input validation errors
│   │   │   ├── service_error.py      # Exception for service-related errors
│   │   │   └── repository_error.py   # Exception for data access errors
```


### **Folder Structure Explanation**

* * *

#### **`shared/`**

- **Purpose:** The `shared` folder is a central location for **reusable, cross-cutting utilities, components, and resources** that are used across multiple parts of the application. This folder helps promote code reuse, maintainability, and consistency by consolidating shared functionality. Common examples include helper functions, constants, configuration files, and adapters for external integrations. Hence, the folder is for cross-cutting concerns like **shared domain logic**, **constants**, or **DTOs** that **don’t neatly fit elsewhere**. This **avoids duplication** across the project.
    - **`exceptions/`**: Contains custom exception classes for consistent error handling across the application.
        - Examples:
            - `custom_exceptions.py`: Base and specific exception classes (e.g., `ValidationError`, `ServiceUnavailableError`).
            - `api_error.py`: Exceptions for API-specific errors.
            - `not_found_error.py`: Exception for "not found" cases.

* * *