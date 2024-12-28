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
│   │   │   ├── user_registered_event.py
│   │   │   └── order_placed_event.py
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

* * *
