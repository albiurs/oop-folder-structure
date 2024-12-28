# Database access and data persistence

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── infrastructure/     # Technical details and external system interaction
│   │   └── repositories/   # Database access and data persistence
│   │       ├── user_repository.py
│   │       ├── product_repository.py
│   │       └── order_repository.py
```


### **Folder Structure Explanation**

* * *

#### **`infrastructure/`**

- **Purpose:** Manages the **technical and integration details** of the application, including interaction with databases, external services, middleware, caching, and runtime guards.
    - **`repositories/`**: Interfaces with the database for CRUD operations and advanced queries.
        - Examples:
            - `user_repository.py`: Handles database operations for users, such as fetching or updating user records.
            - `product_repository.py`: Manages data persistence and retrieval for products.
            - `order_repository.py`: Interfaces with the database for order-related actions.
            - `category_repository.py`: Queries and manages product categories.
            - `review_repository.py`: Handles retrieval and storage of product reviews.
            - `invoice_repository.py`: Manages invoice records in the database.
            - `cart_repository.py`: Handles shopping cart persistence.
            - `payment_repository.py`: Manages payment-related records and queries.
            - `notification_repository.py`: Stores and retrieves user notifications.
            - `subscription_repository.py`: Handles recurring subscription data.

* * *
