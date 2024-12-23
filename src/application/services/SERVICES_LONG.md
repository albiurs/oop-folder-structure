# Business logic and reusable services

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── application/        # Application-specific logic
│   │   ├── services/       # Business logic and reusable services
│   │   │   ├── EmailService.php
│   │   │   ├── PaymentService.php
│   │   │   └── UserService.php
```


### **Folder Structure Explanation**

* * *

#### **`application/`**

- **Purpose:** Implements the main workflows and use cases of the application. This folder bridges domain logic with external systems and user actions, encapsulating high-level business logic.
    - **`services/`**: Implements reusable business logic, designed to be shared across multiple parts of the application.
        - Examples:
            - `UserService.php`: Handles user-specific operations like password hashing.
            - `PaymentService.php`: Encapsulates logic for payment processing.
            - `EmailService.php`: Sends emails for transactional or marketing purposes.
            - `NotificationService.php`: Manages the logic for sending notifications.
            - `OrderService.php`: Encapsulates logic related to order placement or modification.
            - `DiscountService.php`: Calculates discounts for a user’s order.
            - `CategoryService.php`: Handles category management operations.
            - `InventoryService.php`: Manages product stock and availability.
            - `AnalyticsService.php`: Gathers and processes app usage metrics.
            - `ProfileService.php`: Updates and retrieves user profile data.

* * *
