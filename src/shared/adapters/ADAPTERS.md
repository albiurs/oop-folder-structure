# Interfaces or wrappers for external libraries or APIs

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

* * *