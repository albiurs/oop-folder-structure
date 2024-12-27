# # Event subscribers (manage multiple events)

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── application/        # Application-specific logic
│   │   ├── subscribers/      # Event subscribers (manage multiple events)
│   │   │   ├── user_activity_subscriber.py
│   │   │   ├── order_lifecycle_subscriber.py
│   │   │   └── audit_trail_subscriber.py
```


### **Folder Structure Explanation**

* * *

#### `application/`

- **Purpose:** Implements the main workflows and use cases of the application. This folder bridges domain logic with external systems and user actions, encapsulating high-level business logic.
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

* * *
