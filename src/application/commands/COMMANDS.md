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

- **Purpose:** Implements application-specific logic, bridging APIs with domain logic.
    - **`commands/`**: Represents specific actions or tasks within the app.
        - Examples:
            - `CreateUserCommand.php`: Encapsulates data and validation for creating a user.
            - `UpdateOrderCommand.php`: Updates an order's status or details.
            - `ResetPasswordCommand.php`: Handles the reset password workflow.

* * *
