# Query objects for fetching data

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── application/        # Application-specific logic
│   │   ├── queries/        # Query objects for fetching data
│   │   │   ├── GetUserByIdQuery.php
│   │   │   └── ListOrdersQuery.php
```


### **Folder Structure Explanation**

* * *

#### **`application/`**

- **Purpose:** Implements application-specific logic, bridging APIs with domain logic.
    - **`queries/`**: Manages data retrieval logic, typically for read-only operations.
        - Examples:
            - `GetUserByIdQuery.php`: Retrieves a user by their unique identifier.
            - `ListOrdersQuery.php`: Fetches a paginated list of orders.
            - `GetProductDetailsQuery.php`: Retrieves detailed information about a product.

* * *
