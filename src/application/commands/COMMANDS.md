# Command objects for task-based actions

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── application/        # Application-specific logic
│   │   ├── commands/       # Command objects for task-based actions
│   │   │   ├── CreateUserCommand.php
│   │   │   └── UpdateOrderCommand.php
```


### **Folder Structure Explanation**

* * *

#### **`application/`**

- **Purpose:** Implements the main workflows and use cases of the application. This folder bridges domain logic with external systems and user actions, encapsulating high-level business logic.
    - **`commands/`**: Encapsulates actions triggered by the user or system. Commands focus on "doing" rather than "querying," ensuring task execution is isolated and reusable.
        - Examples:
            - `CreateUserCommand.php`: Handles the creation of a new user.
            - `UpdateOrderCommand.php`: Updates an order’s status or properties.
            - `DeleteProductCommand.php`: Removes a product from the system.
            - `ResetPasswordCommand.php`: Initiates the password reset process for a user.
            - `CreateCategoryCommand.php`: Adds a new product category to the database.
            - `SendNotificationCommand.php`: Triggers a notification for a user or group.
            - `GenerateReportCommand.php`: Initiates the process of creating a new report.
            - `ApplyDiscountCommand.php`: Applies a discount code to a user’s cart or order.
            - `CreateReviewCommand.php`: Adds a new review for a product.
            - `UpdateProfileCommand.php`: Modifies a user’s profile settings or data.

* * *
