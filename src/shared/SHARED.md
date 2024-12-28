# Contains reusable utilities, adapters, and shared components

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── shared/                      # Contains reusable utilities, adapters, and shared components
│   │   ├── adapters/                # Interfaces or wrappers for external libraries or APIs
│   │   │   ├── api_adapter.py
│   │   │   ├── payment_adapter.py
│   │   │   └── cache_adapter.py
│   │   ├── dto/                     # Data Transfer Objects for inter-layer communication
│   │   │   ├── user_dto.py           # DTO for user-related data transfer
│   │   │   ├── product_dto.py        # DTO for product-related data transfer
│   │   │   ├── order_dto.py          # DTO for order-related data transfer
│   │   │   └── payment_dto.py        # DTO for payment-related data transfer
│   │   ├── exceptions/              # Custom exception classes for consistent error handling
│   │   │   ├── validation_error.py   # Exception for input validation errors
│   │   │   ├── service_error.py      # Exception for service-related errors
│   │   │   └── repository_error.py   # Exception for data access errors
│   │   ├── helpers/                 # General-purpose utility functions
│   │   │   ├── date_utils.py         # Functions for date and time manipulation
│   │   │   ├── string_utils.py       # String processing utilities
│   │   │   └── file_utils.py         # File handling utilities
│   │   ├── constants.py              # Centralized application constants
│   │   ├── logger.py                 # Utility for standardized logging
│   │   └── config.py                 # Configuration settings loader
```


### **Folder Structure Explanation**

* * *

#### **`shared/`**

- **Purpose:** The `shared` folder is a central location for **reusable, cross-cutting utilities, components, and resources** that are used across multiple parts of the application. This folder helps promote code reuse, maintainability, and consistency by consolidating shared functionality. Common examples include helper functions, constants, configuration files, and adapters for external integrations. Hence, the folder is for cross-cutting concerns like **shared domain logic**, **constants**, or **DTOs** that **don’t neatly fit elsewhere**. This **avoids duplication** across the project.
    - **`adapters/`**: Contains integrations and adapters for third-party services or libraries.
        - Examples:
            - `http_adapter.py`: Abstraction for making HTTP requests (e.g., using `requests`).
            - `cache_adapter.py`: Adapter for interacting with a caching service (e.g., Redis).
            - `email_adapter.py`: Utility for sending emails through external providers.
    - **`dto/`**: The **DTO (Data Transfer Object)** folder in the `shared/` directory is used to define reusable objects for transferring structured data between layers or components of the application. DTOs are often simple objects or classes that only contain properties and no business logic. They help: 1.  **Decouple Layers**: They provide a clean way to transfer data between the domain, application, infrastructure, or presentation layers without exposing internal implementation details. 2.  **Validation**: DTOs can enforce strict typing and validation to ensure only expected data is passed. 3.  **Reusability**: Common DTOs can be shared across modules, avoiding duplication. 4.  **Consistency**: Standardized data structures ensure consistent communication across application layers.
        - Examples:
            - `user_dto.py`: Represents user-related data for transfer between application and infrastructure layers.
            - `order_dto.py`: Represents order details for communication between services.
            - `pagination_dto.py`: Defines data structure for paginated API responses.
            - `auth_response_dto.py`: Represents authentication response data, e.g., tokens and expiration.
            - `product_dto.py`: Encapsulates product data for catalog or inventory systems.
            - `error_response_dto.py`: Represents standardized error responses for APIs or services.
            - `payment_dto.py`: Represents payment-related data for use in payment processing systems.
            - `address_dto.py`: Represents address data for shipping or billing.
            - `notification_dto.py`: Represents a notification object for sending alerts/messages.
            - `file_upload_dto.py`: Represents metadata for file uploads.
    - **`exceptions/`**: Contains custom exception classes for consistent error handling across the application.
        - Examples:
            - `custom_exceptions.py`: Base and specific exception classes (e.g., `ValidationError`, `ServiceUnavailableError`).
            - `api_error.py`: Exceptions for API-specific errors.
            - `not_found_error.py`: Exception for "not found" cases.
    - **`helpers/`**: Contains utility functions or modules that provide commonly used functionality across the application.
        - Examples:
            - `date_utils.py`: Functions for handling date and time formatting.
            - `string_utils.py`: Functions for string manipulation (e.g., slug generation).
            - `math_utils.py`: Functions for calculations and numeric processing.
    - **Examples:**
        - `config.py`: Centralized configuration management for the application (e.g., loading environment variables).
        - `logger.py`: Configurable logging utility for standardized application-wide logging.
        - `constants.py`: Centralized constants used throughout the application (e.g., magic numbers, API endpoints, or status codes).
        - `validators.py`: Collection of reusable input validation functions.
        - `encryption_utils.py`: Functions for encryption and decryption (e.g., hashing passwords or securing sensitive data).
        - `rate_limiter.py`: Utility for rate-limiting requests to APIs or services.
        - `http_adapter.py`: Adapter for making HTTP requests using `requests` or `httpx`.
        - `date_utils.py`: Utility functions for date manipulation (e.g., parsing, formatting).
        - `mock_services.py`: Mocks for external services or APIs used in testing or development environments.
        - `dependency_injection.py`: Dependency injection setup or shared service registries.

* * *