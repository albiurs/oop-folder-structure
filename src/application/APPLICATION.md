# Application-specific logic

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
│   │   ├── factories/      # Factory classes for object creation
│   │   │   ├── user_factory.py
│   │   │   └── product_factory.py
│   │   ├── listeners/        # Event listeners (focused actions for events)
│   │   │   ├── send_welcome_email_listener.py
│   │   │   ├── update_inventory_listener.py
│   │   │   └── notify_user_payment_listener.py
│   │   ├── queries/        # Query objects for fetching data
│   │   │   ├── get_user_by_id_query.py
│   │   │   └── list_orders_query.py
│   │   ├── services/       # Business logic and reusable services
│   │   │   ├── user_service.py
│   │   │   ├── payment_service.py
│   │   │   └── email_service.py
│   │   ├── subscribers/      # Event subscribers (manage multiple events)
│   │   │   ├── user_activity_subscriber.py
│   │   │   ├── order_lifecycle_subscriber.py
│   │   │   └── audit_trail_subscriber.py
│   │   └── use_cases/      # Use case logic
│   │       ├── register_user.py
│   │       └── process_order.py
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

    - `factories/`: Responsible for creating and configuring objects, abstracting away complex initialization logic, especially when multiple dependencies are involved.
        - Examples:
            - `user_factory.py`: Creates user objects with default or custom configurations.
            - `order_factory.py`: Generates order instances for testing or production use.
            - `product_factory.py`: Builds product objects with sample or specified data.
            - `category_factory.py`: Creates category instances for use in the application.
            - `payment_factory.py`: Builds payment objects with default configurations.
            - `notification_factory.py`: Generates notification objects for various use cases.
            - `profile_factory.py`: Constructs user profile objects with mock or real data.
            - `discount_factory.py`: Creates discount codes or coupon objects.
            - `review_factory.py`: Builds review objects for products or services.
            - `report_factory.py`: Prepares report objects for analysis or output.
    - `listeners`: A **listener** is a component that **reacts to an event**. It is responsible for implementing the logic that needs to be executed when an event occurs. A listener is typically tied to **specific events** and performs a **single, well-defined task**.
        - Examples:
            - `send_welcome_email_listener.py`: Sends a welcome email after `user_logged_in_event.py`.
            - `update_inventory_listener.py`: Updates inventory records upon `order_placed_event.py`.
            - `log_file_upload_listener.py`: Logs details of file uploads upon `file_uploaded_event.py`.
            - `notify_user_payment_listener.py`: Sends payment confirmation emails upon `payment_processed_event.py`.
            - `mark_task_as_completed_listener.py`: Updates the database to mark a task as completed upon `task_completed_event.py`.
            - `reindex_product_listener.py`: Updates search indexes upon `inventory_updated_event.py`.
            - `send_review_acknowledgement_listener.py`: Notifies a user that their review was successfully submitted upon `product_reviewed_event.py`.
            - `log_session_expiry_listener.py`: Logs the session expiry details when `session_expired_event.py` occurs.
            - `generate_invoice_listener.py`: Creates an invoice after `order_placed_event.py`.
            - `notify_moderator_listener.py`: Alerts moderators about a comment added with `comment_added_event.py`.

    - `queries/`: Handles read-only operations by encapsulating data-fetching logic. Queries are responsible for retrieving specific data efficiently and clearly.
        - Examples:
            - `get_user_by_id_query.py`: Retrieves a user by their unique ID.
            - `list_orders_query.py`: Returns all orders for a specific user or timeframe.
            - `get_product_details_query.py`: Fetches detailed product information by ID.
            - `search_products_query.py`: Retrieves products matching search criteria.
            - `get_category_by_id_query.py`: Retrieves a category by its identifier.
            - `get_order_history_query.py`: Fetches a user’s past orders.
            - `fetch_notifications_query.py`: Retrieves unread notifications for a user.
            - `list_reviews_query.py`: Retrieves product reviews from the database.
            - `get_report_data_query.py`: Retrieves data required for generating reports.
            - `get_discounts_query.py`: Fetches available discount codes or coupons.

    - `services/`: Implements reusable business logic, designed to be shared across multiple parts of the application.
        - Examples:
            - `user_service.py`: Handles user-specific operations like password hashing.
            - `payment_service.py`: Encapsulates logic for payment processing.
            - `email_service.py`: Sends emails for transactional or marketing purposes.
            - `notification_service.py`: Manages the logic for sending notifications.
            - `order_service.py`: Encapsulates logic related to order placement or modification.
            - `discount_service.py`: Calculates discounts for a user’s order.
            - `category_service.py`: Handles category management operations.
            - `inventory_service.py`: Manages product stock and availability.
            - `analytics_service.py`: Gathers and processes app usage metrics.
            - `profile_service.py`: Updates and retrieves user profile data.
    - `subscribers`: A **subscriber** is a component that **listens for multiple events** and typically defines **which events it reacts to and how**. Subscribers are more versatile than listeners and are usually employed in frameworks or libraries that support event-driven systems.
        - Examples:
            - `user_activity_subscriber.py`: Reacts to `user_logged_in_event.py` and `session_expired_event.py` to log user activity.
            - `order_lifecycle_subscriber.py`: Handles `order_placed_event.py`, `payment_processed_event.py`, and `order_shipped_event.py`.
            - `file_management_subscriber.py`: Responds to `file_uploaded_event.py` and `file_deleted_event.py`.
            - `notification_subscriber.py`: Sends notifications for `comment_added_event.py`, `task_completed_event.py`, and `email_sent_event.py`.
            - `audit_trail_subscriber.py`: Records audit trails for `user_logged_in_event.py`, `order_placed_event.py`, and `payment_processed_event.py`.
            - `inventory_subscriber.py`: Updates inventory for `inventory_updated_event.py` and alerts low stock on `order_placed_event.py`.
            - `error_handling_subscriber.py`: Logs errors for `payment_failed_event.py` and `file_upload_failed_event.py`.
            - `analytics_subscriber.py`: Tracks analytics for `user_logged_in_event.py`, `order_placed_event.py`, and `task_completed_event.py`.
            - `lifecycle_subscriber.py`: Manages lifecycle hooks for `session_started_event.py`, `session_expired_event.py`, and `user_logged_out_event.py`.
            - `post_lifecycle_subscriber.py`: Handles post-related events like `post_published_event.py` and `comment_added_event.py`.

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
