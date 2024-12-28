# OOP Folder Structure Best Practices

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── domain/             # Core domain models and business logic
│   │   ├── events/         # Domain events
│   │   │   ├── user_registered_event.py
│   │   │   └── order_placed_event.py
│   │   ├── models/         # Business/domain models
│   │   │   ├── user.py
│   │   │   ├── product.py
│   │   │   └── order.py
│   │   └── value_objects/  # Value objects (e.g., immutable types)
│   │       ├── money.py
│   │       └── address.py
```


### **Folder Structure Explanation**

* * *

#### **`domain/`**

- **Purpose:** Represents the **core business logic and rules** of the application. This folder encapsulates the domain-specific models, value objects, and domain events, ensuring that business logic remains independent of technical or application concerns.
    - **`events/`**: Defines **domain-specific events** that are raised when significant actions occur. These events are **business-domain-focused** and represent **what has occurred** within the application’s core domain. They encapsulate immutable facts about a specific action or state change. An **event** represents something that has occurred in the system. It’s a plain data object or class encapsulating information about the occurrence. Events are typically created by a component when it completes a significant action, such as a user login, a file upload, or a transaction completion. Events trigger specific reactions (handled by **listeners** or **subscribers**).
        - Examples:
            - `user_registered_event.py`: Triggered when a new user registers.
                - `order_placed_event.py`: Raised when an order is successfully placed.
                - `product_created_event.py`: Triggered when a new product is added to the catalog.
                - `order_shipped_event.py`: Raised when an order is shipped.
                - `payment_failed_event.py`: Triggered when a payment attempt fails.
                - `user_logged_in_event.py`: Raised when a user successfully logs in.
                - `discount_applied_event.py`: Triggered when a discount is applied to an order.
                - `subscription_renewed_event.py`: Raised when a recurring subscription is renewed.
                - `cart_abandoned_event.py`: Triggered when a cart is left inactive for too long.
                - `profile_updated_event.py`: Raised when a user updates their profile.
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
    - **`value_objects/`**: Represents immutable, domain-specific data types like money, dates, or units.
        - Examples:
            - `money.py`: Handles monetary values with precision and currency types.
            - `address.py`: Represents a postal address, including `street`, `city`, and `postal_code`.
            - `email.py`: Validates and stores email addresses as immutable objects.
            - `phone_number.py`: Encapsulates and validates phone number data.
            - `coordinates.py`: Represents latitude and longitude for geolocation purposes.
            - `tax_rate.py`: Models tax rates applicable to transactions.
            - `discount_code.py`: Encodes discount codes and their validity.
            - `currency.py`: Represents different currencies for global transactions.
            - `date_range.py`: Encapsulates a range of dates, e.g., for promotions or reports.
            - `order_status.py`: Represents the possible states of an order (e.g., `Pending`, `Shipped`, `Completed`).

* * *
