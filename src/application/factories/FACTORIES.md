# Factory classes for object creation

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── application/        # Application-specific logic
│   │   ├── factories/      # Factory classes for object creation
│   │   │   ├── ProductFactory.php
│   │   │   └── UserFactory.php
```

### **Folder Structure Explanation**

* * *

#### **`application/`**

- **Purpose:** Implements application-specific logic, bridging APIs with domain logic.
    - **`factories/`**: Handles object creation, abstracting complexity.
        - Examples:
            - `UserFactory.php`: Builds user objects with default or test data.
            - `OrderFactory.php`: Creates order objects preconfigured for tests or scenarios.
            - `NotificationFactory.php`: Generates notification objects for different types of alerts.

* * *
