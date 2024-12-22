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

- **Purpose:** Encapsulates core business logic and domain-specific models.
    - **`events/`**: Defines domain events triggered by business logic.
        - Examples:
            - `UserRegisteredEvent.php`: Triggered when a new user registers.
            - `OrderPlacedEvent.php`: Fired when an order is successfully placed.
            - `ProductUpdatedEvent.php`: Dispatched when a product's details are updated.
    - **`models/`**: Represents business entities and core data structures.
        - Examples:
            - `User.php`: Represents a user in the system.
            - `Order.php`: Represents an order with details like status and items.
            - `Product.php`: Models a product with attributes like name, price, and stock.
    - **`value_objects/`**: Represents immutable objects with specific value logic.
        - Examples:
            - `Money.php`: Handles currency and arithmetic for monetary values.
            - `Address.php`: Represents a user's address in a standardized way.
            - `Coordinates.php`: Encapsulates latitude and longitude for geolocation.

* * *
