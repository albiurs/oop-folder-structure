# Business/domain models

# OOP Folder Structure Best Practices

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── domain/             # Core domain models and business logic
│   │   ├── models/         # Business/domain models
│   │   │   ├── Order.php
│   │   │   ├── Product.php
│   │   │   └── User.php
```


### **Folder Structure Explanation**

* * *

#### **`domain/`**

- **Purpose:** Encapsulates core business logic and domain-specific models.
    - **`models/`**: Represents business entities and core data structures.
        - Examples:
            - `User.php`: Represents a user in the system.
            - `Order.php`: Represents an order with details like status and items.
            - `Product.php`: Models a product with attributes like name, price, and stock.

* * *
