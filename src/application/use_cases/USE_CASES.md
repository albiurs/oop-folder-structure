# Use case logic

# OOP Folder Structure Best Practices

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── application/        # Application-specific logic
│   │   └── use_cases/      # Use case logic
│   │       ├── ProcessOrder.php
│   │       └── RegisterUser.php
```


### **Folder Structure Explanation**

* * *

#### **`application/`**

- **Purpose:** Implements application-specific logic, bridging APIs with domain logic.
    - **`use_cases/`**: Coordinates core application workflows.
        - Examples:
            - `RegisterUser.php`: Handles all logic for user registration.
            - `ProcessOrder.php`: Orchestrates the steps for placing an order.
            - `SendInvoice.php`: Manages the workflow for generating and sending invoices.

* * *
