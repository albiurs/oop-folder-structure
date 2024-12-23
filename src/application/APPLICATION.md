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
    - **`factories/`**: Responsible for creating and configuring objects, abstracting away complex initialization logic, especially when multiple dependencies are involved.
        - Examples:
            - `UserFactory.php`: Creates user objects with default or custom configurations.
            - `OrderFactory.php`: Generates order instances for testing or production use.
            - `ProductFactory.php`: Builds product objects with sample or specified data.
            - `CategoryFactory.php`: Creates category instances for use in the application.
            - `PaymentFactory.php`: Builds payment objects with default configurations.
            - `NotificationFactory.php`: Generates notification objects for various use cases.
            - `ProfileFactory.php`: Constructs user profile objects with mock or real data.
            - `DiscountFactory.php`: Creates discount codes or coupon objects.
            - `ReviewFactory.php`: Builds review objects for products or services.
            - `ReportFactory.php`: Prepares report objects for analysis or output.
    - **`queries/`**: Handles read-only operations by encapsulating data-fetching logic. Queries are responsible for retrieving specific data efficiently and clearly.
        - Examples:
            - `GetUserByIdQuery.php`: Retrieves a user by their unique ID.
            - `ListOrdersQuery.php`: Returns all orders for a specific user or timeframe.
            - `GetProductDetailsQuery.php`: Fetches detailed product information by ID.
            - `SearchProductsQuery.php`: Retrieves products matching search criteria.
            - `GetCategoryByIdQuery.php`: Retrieves a category by its identifier.
            - `GetOrderHistoryQuery.php`: Fetches a user’s past orders.
            - `FetchNotificationsQuery.php`: Retrieves unread notifications for a user.
            - `ListReviewsQuery.php`: Retrieves product reviews from the database.
            - `GetReportDataQuery.php`: Retrieves data required for generating reports.
            - `GetDiscountsQuery.php`: Fetches available discount codes or coupons.
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
    - **`use_cases/`**: Implements workflows that require coordination between services, queries, and commands. They represent high-level business use cases and often define specific application features.
        - Examples:
            - `RegisterUser.php`: Coordinates user registration, including validation, saving, and sending confirmation emails.
            - `ProcessOrder.php`: Manages the workflow for placing an order.
            - `SendNotification.php`: Handles the process of sending a notification.
            - `GenerateInvoice.php`: Orchestrates the generation of an invoice.
            - `ResetUserPassword.php`: Manages the end-to-end password reset process.
            - `ApplyDiscountToOrder.php`: Combines discount calculations with order updates.
            - `UpdateUserProfile.php`: Handles profile update requests.
            - `AddProductToCatalog.php`: Adds a new product to the catalog with associated data.
            - `FetchDashboardMetrics.php`: Prepares analytics for the admin dashboard.
            - `CreateReport.php`: Manages the process of generating and formatting reports.

* * *
