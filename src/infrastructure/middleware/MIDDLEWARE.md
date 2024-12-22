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

- **Purpose:** Manages technical implementation details and external system interactions.
    - **`middleware/`**: Processes requests and responses in a pipeline.
        - Examples:
            - `AuthenticationMiddleware.php`: Checks if the user is authenticated.
            - `LoggingMiddleware.php`: Logs request/response data for debugging.
            - `RateLimitingMiddleware.php`: Enforces request rate limits.

* * *
