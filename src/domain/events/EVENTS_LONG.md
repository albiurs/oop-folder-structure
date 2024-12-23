# Domain events

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

* * *
