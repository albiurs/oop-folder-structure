# # Event listeners (focused actions for events)

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── application/        # Application-specific logic
│   │   ├── listeners/        # Event listeners (focused actions for events)
│   │   │   ├── send_welcome_email_listener.py
│   │   │   ├── update_inventory_listener.py
│   │   │   └── notify_user_payment_listener.py
```


### **Folder Structure Explanation**

* * *

#### `application/`

- **Purpose:** Implements the main workflows and use cases of the application. This folder bridges domain logic with external systems and user actions, encapsulating high-level business logic.
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

* * *
