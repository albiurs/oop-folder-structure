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

- **Purpose:** Implements the main workflows and use cases of the application. This folder bridges domain logic with external systems and user actions, encapsulating high-level business logic.
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
