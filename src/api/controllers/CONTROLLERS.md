# API controllers

## Folder Structure

```
project/
│
├── src/                    # Source code
│   ├── api/                # API-specific components
│   │   ├── controllers/    # API controllers
│   │   │   ├── OrderController.php
│   │   │   ├── ProductController.php
│   │   │   └── UserController.php
```


### **Folder Structure Explanation**

* * *

#### **`api/`**

- **Purpose:** Contains components for interacting with external APIs (e.g., REST, GraphQL).
    - **`controllers/`**: Handles HTTP requests and API-specific routing logic.
        - Examples:
            - `UserController.php`: Processes user-related API requests.
            - `OrderController.php`: Handles order-related endpoints.
            - `AuthController.php`: Manages authentication-related requests like login or registration.

* * *
