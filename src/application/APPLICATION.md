# Application-specific logic

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
│   │   ├── factories/      # Factory classes for object creation
│   │   │   ├── ProductFactory.php
│   │   │   └── UserFactory.php
│   │   ├── queries/        # Query objects for fetching data
│   │   │   ├── GetUserByIdQuery.php
│   │   │   └── ListOrdersQuery.php
│   │   ├── services/       # Business logic and reusable services
│   │   │   ├── EmailService.php
│   │   │   ├── PaymentService.php
│   │   │   └── UserService.php
│   │   └── use_cases/      # Use case logic
│   │       ├── ProcessOrder.php
│   │       └── RegisterUser.php
│   │
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
    - **`factories/`**: Handles object creation, abstracting complexity.
        - Examples:
            - `UserFactory.php`: Builds user objects with default or test data.
            - `OrderFactory.php`: Creates order objects preconfigured for tests or scenarios.
            - `NotificationFactory.php`: Generates notification objects for different types of alerts.
    - **`queries/`**: Manages data retrieval logic, typically for read-only operations.
        - Examples:
            - `GetUserByIdQuery.php`: Retrieves a user by their unique identifier.
            - `ListOrdersQuery.php`: Fetches a paginated list of orders.
            - `GetProductDetailsQuery.php`: Retrieves detailed information about a product.
    - **`services/`**: Contains reusable business logic used across the app.
        - Examples:
            - `PaymentService.php`: Processes payments using a third-party API.
            - `EmailService.php`: Sends email notifications to users.
            - `UserService.php`: Manages user-related business logic, like profile updates.
    - **`use_cases/`**: Coordinates core application workflows.
        - Examples:
            - `RegisterUser.php`: Handles all logic for user registration.
            - `ProcessOrder.php`: Orchestrates the steps for placing an order.
            - `SendInvoice.php`: Manages the workflow for generating and sending invoices.

* * *
