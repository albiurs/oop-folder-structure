# Database access and data persistence

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── infrastructure/     # Technical details and external system interaction
│   │   └── repositories/   # Database access and data persistence
│   │       ├── OrderRepository.php
│   │       ├── ProductRepository.php
│   │       └── UserRepository.php
```


### **Folder Structure Explanation**

* * *

#### **`infrastructure/`**

- **Purpose:** Manages technical implementation details and external system interactions.
    - **`repositories/`**: Handles database access and data persistence.
        - Examples:
            - `UserRepository.php`: Manages CRUD operations for users.
            - `OrderRepository.php`: Handles data persistence for orders.
            - `ProductRepository.php`: Manages product-related database queries.

* * *
