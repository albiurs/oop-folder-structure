# OOP Folder Structure Best Practices

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── domain/             # Core domain models and business logic
│   │   ├── events/         # Domain events
│   │   │   ├── OrderPlacedEvent.php
│   │   │   └── UserRegisteredEvent.php
│   │   ├── models/         # Business/domain models
│   │   │   ├── Order.php
│   │   │   ├── Product.php
│   │   │   └── User.php
│   │   └── value_objects/  # Value objects (e.g., immutable types)
│   │       ├── Address.php
│   │       └── Money.php
│   │
```


### **Folder Structure Explanation**

* * *

#### **`domain/`**

- **Purpose:** Represents the **core business logic and rules** of the application. This folder encapsulates the domain-specific models, value objects, and domain events, ensuring that business logic remains independent of technical or application concerns.
    - **`events/`**: Defines domain-specific events that are raised when significant actions occur.
        - Examples:
            - `UserRegisteredEvent.php`: Triggered when a new user registers.
            - `OrderPlacedEvent.php`: Raised when an order is successfully placed.
            - `ProductCreatedEvent.php`: Triggered when a new product is added to the catalog.
            - `OrderShippedEvent.php`: Raised when an order is shipped.
            - `PaymentFailedEvent.php`: Triggered when a payment attempt fails.
            - `UserLoggedInEvent.php`: Raised when a user successfully logs in.
            - `DiscountAppliedEvent.php`: Triggered when a discount is applied to an order.
            - `SubscriptionRenewedEvent.php`: Raised when a recurring subscription is renewed.
            - `CartAbandonedEvent.php`: Triggered when a cart is left inactive for too long.
            - `ProfileUpdatedEvent.php`: Raised when a user updates their profile.
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
    - **`value_objects/`**: Represents immutable, domain-specific data types like money, dates, or units.
        - Examples:
            - `Money.php`: Handles monetary values with precision and currency types.
            - `Address.php`: Represents a postal address, including `street`, `city`, and `postalCode`.
            - `Email.php`: Validates and stores email addresses as immutable objects.
            - `PhoneNumber.php`: Encapsulates and validates phone number data.
            - `Coordinates.php`: Represents latitude and longitude for geolocation purposes.
            - `TaxRate.php`: Models tax rates applicable to transactions.
            - `DiscountCode.php`: Encodes discount codes and their validity.
            - `Currency.php`: Represents different currencies for global transactions.
            - `DateRange.php`: Encapsulates a range of dates, e.g., for promotions or reports.
            - `OrderStatus.php`: Represents the possible states of an order (e.g., `Pending`, `Shipped`, `Completed`).

* * *
