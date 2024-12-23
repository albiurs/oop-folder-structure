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

- **Purpose:** Represents the **core business logic and rules** of the application. This folder encapsulates the domain-specific models, value objects, and domain events, ensuring that business logic remains independent of technical or application concerns.
    - **`models/`**: Defines the entities that are central to the business domain, often tied to database records or key objects in the system.
        - Examples:
            - `User.php`: Represents a user entity with attributes like `id`, `name`, `email`, and `roles`.
            - `Product.php`: Encapsulates product data such as `name`, `price`, and `description`.
            - `Order.php`: Represents an order with details like items, totals, and shipping information.
            - `Category.php`: Defines categories for products in a hierarchical structure.
            - `Cart.php`: Models a shopping cart with associated items and quantities.
            - `Review.php`: Represents a product review with attributes like `rating` and `comments`.
            - `Invoice.php`: Tracks invoice details like amount, due date, and status.
            - `Payment.php`: Represents payment transactions, including methods and statuses.
            - `Address.php`: Stores user or order address details.
            - `Subscription.php`: Models recurring subscriptions for users or products.

* * *
