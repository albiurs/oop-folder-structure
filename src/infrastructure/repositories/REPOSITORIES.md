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

- **Purpose:** Manages the **technical and integration details** of the application, including interaction with databases, external services, middleware, caching, and runtime guards.
    - **`repositories/`**: Interfaces with the database for CRUD operations and advanced queries.
        - Examples:
            - `UserRepository.php`: Handles database operations for users, such as fetching or updating user records.
            - `ProductRepository.php`: Manages data persistence and retrieval for products.
            - `OrderRepository.php`: Interfaces with the database for order-related actions.
            - `CategoryRepository.php`: Queries and manages product categories.
            - `ReviewRepository.php`: Handles retrieval and storage of product reviews.
            - `InvoiceRepository.php`: Manages invoice records in the database.
            - `CartRepository.php`: Handles shopping cart persistence.
            - `PaymentRepository.php`: Manages payment-related records and queries.
            - `NotificationRepository.php`: Stores and retrieves user notifications.
            - `SubscriptionRepository.php`: Handles recurring subscription data.

* * *
