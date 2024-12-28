# Business/domain models

# OOP Folder Structure Best Practices

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   │   ├── models/         # Business/domain models
│   │   │   ├── user.py
│   │   │   ├── product.py
│   │   │   └── order.py
```


### **Folder Structure Explanation**

* * *

#### **`domain/`**

- **Purpose:** Represents the **core business logic and rules** of the application. This folder encapsulates the domain-specific models, value objects, and domain events, ensuring that business logic remains independent of technical or application concerns.
    - **`models/`**: Defines the entities that are central to the business domain, often tied to database records or key objects in the system.
        - Examples:
            - `user.py`: Represents a user entity with attributes like `id`, `name`, `email`, and `roles`.
                - `product.py`: Encapsulates product data such as `name`, `price`, and `description`.
                - `order.py`: Represents an order with details like items, totals, and shipping information.
                - `category.py`: Defines categories for products in a hierarchical structure.
                - `cart.py`: Models a shopping cart with associated items and quantities.
                - `review.py`: Represents a product review with attributes like `rating` and `comments`.
                - `invoice.py`: Tracks invoice details like amount, due date, and status.
                - `payment.py`: Represents payment transactions, including methods and statuses.
                - `address.py`: Stores user or order address details.
                - `subscription.py`: Models recurring subscriptions for users or products.

* * *
