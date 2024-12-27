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
│   │       ├── register_user.py
│   │       └── process_order.py
```


### **Folder Structure Explanation**

* * *

#### `application/`

- **Purpose:** Implements the main workflows and use cases of the application. This folder bridges domain logic with external systems and user actions, encapsulating high-level business logic.
    - `use_cases/`: Implements workflows that require coordination between services, queries, and commands. They represent high-level business use cases and often define specific application features.
        - Examples:
            - `register_user.py`: Coordinates user registration, including validation, saving, and sending confirmation emails.
            - `process_order.py`: Manages the workflow for placing an order.
            - `send_notification.py`: Handles the process of sending a notification.
            - `generate_invoice.py`: Orchestrates the generation of an invoice.
            - `reset_user_password.py`: Manages the end-to-end password reset process.
            - `apply_discount_to_order.py`: Combines discount calculations with order updates.
            - `update_user_profile.py`: Handles profile update requests.
            - `add_product_to_catalog.py`: Adds a new product to the catalog with associated data.
            - `fetch_dashboard_metrics.py`: Prepares analytics for the admin dashboard.
            - `create_report.py`: Manages the process of generating and formatting reports.

* * *
