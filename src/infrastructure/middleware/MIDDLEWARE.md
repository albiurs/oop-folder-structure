# Middleware logic (e.g., for HTTP requests)

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── infrastructure/     # Technical details and external system interaction
│   │   ├── middleware/     # Middleware logic (e.g., for HTTP requests)
│   │   │   ├── authentication_middleware.py
│   │   │   └── logging_middleware.py
```


### **Folder Structure Explanation**

* * *

#### **`infrastructure/`**

- **Purpose:** Manages the **technical and integration details** of the application, including interaction with databases, external services, middleware, caching, and runtime guards.
    - **`middleware/`**: Contains logic for processing HTTP requests and responses, such as authentication or logging.
        - Examples:
            - `authentication_middleware.py`: Ensures that users are authenticated for protected routes.
            - `logging_middleware.py`: Logs incoming requests and responses for debugging purposes.
            - `rate_limiting_middleware.py`: Enforces request rate limits for APIs.
            - `cors_middleware.py`: Handles Cross-Origin Resource Sharing policies.
            - `authorization_middleware.py`: Checks user permissions for requested actions.
            - `localization_middleware.py`: Sets the language/locale for the current request.
            - `request_validation_middleware.py`: Validates incoming request data against predefined schemas.
            - `error_handling_middleware.py`: Centralizes error handling and formatting for client responses.
            - `session_middleware.py`: Manages session data for authenticated users.
            - `cache_middleware.py`: Implements caching for specific requests to improve performance.

* * *
