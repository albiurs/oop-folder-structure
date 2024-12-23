# Middleware logic (e.g., for HTTP requests)

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── infrastructure/     # Technical details and external system interaction
│   │   ├── middleware/     # Middleware logic (e.g., for HTTP requests)
│   │   │   ├── AuthenticationMiddleware.php
│   │   │   └── LoggingMiddleware.php
```


### **Folder Structure Explanation**

* * *

#### **`infrastructure/`**

- **Purpose:** Manages the **technical and integration details** of the application, including interaction with databases, external services, middleware, caching, and runtime guards.
    - **`middleware/`**: Contains logic for processing HTTP requests and responses, such as authentication or logging.
        - Examples:
            - `AuthenticationMiddleware.php`: Ensures that users are authenticated for protected routes.
            - `LoggingMiddleware.php`: Logs incoming requests and responses for debugging purposes.
            - `RateLimitingMiddleware.php`: Enforces request rate limits for APIs.
            - `CorsMiddleware.php`: Handles Cross-Origin Resource Sharing policies.
            - `AuthorizationMiddleware.php`: Checks user permissions for requested actions.
            - `LocalizationMiddleware.php`: Sets the language/locale for the current request.
            - `RequestValidationMiddleware.php`: Validates incoming request data against predefined schemas.
            - `ErrorHandlingMiddleware.php`: Centralizes error handling and formatting for client responses.
            - `SessionMiddleware.php`: Manages session data for authenticated users.
            - `CacheMiddleware.php`: Implements caching for specific requests to improve performance.

* * *
