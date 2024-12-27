# Command objects for task-based actions

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── application/        # Application-specific logic
│   │   ├── commands/       # Command objects for task-based actions
│   │   │   ├── create_user_command.py
│   │   │   └── update_order_command.py
```


### **Folder Structure Explanation**

* * *

#### `application/`

- **Purpose:** Implements the main workflows and use cases of the application. This folder bridges domain logic with external systems and user actions, encapsulating high-level business logic.
    - `commands/`: Encapsulates actions triggered by the user or system. Commands focus on "doing" rather than "querying," ensuring task execution is isolated and reusable.
        - Examples:
            - `create_user_command.py`: Handles the creation of a new user.
            - `update_order_command.py`: Updates an order’s status or properties.
            - `delete_product_command.py`: Removes a product from the system.
            - `reset_password_command.py`: Initiates the password reset process for a user.
            - `create_category_command.py`: Adds a new product category to the database.
            - `send_notification_command.py`: Triggers a notification for a user or group.
            - `generate_report_command.py`: Initiates the process of creating a new report.
            - `apply_discount_command.py`: Applies a discount code to a user’s cart or order.
            - `create_review_command.py`: Adds a new review for a product.
            - `update_profile_command.py`: Modifies a user’s profile settings or data.

* * *
