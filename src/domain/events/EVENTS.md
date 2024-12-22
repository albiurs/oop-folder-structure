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

- **Purpose:** Encapsulates core business logic and domain-specific models.
    - **`events/`**: Defines domain events triggered by business logic.
        - Examples:
            - `UserRegisteredEvent.php`: Triggered when a new user registers.
            - `OrderPlacedEvent.php`: Fired when an order is successfully placed.
            - `ProductUpdatedEvent.php`: Dispatched when a product's details are updated.

* * *
