# Asynchronous or background tasks

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── jobs/               # Asynchronous or background tasks
│   │   ├── send_email_job.py
│   │   ├── generate_report_job.py
│   │   └── data_cleanup_job.py
```


### **Folder Structure Explanation**

* * *

#### **`jobs/`**

- **Purpose:** Contains classes for **asynchronous tasks** or background jobs that can be queued and executed independently of the main application workflow. Hence, these tasks are executed outside the main application thread, often handled by task queues or schedulers. Jobs improve application performance and scalability by offloading heavy or time-consuming tasks.
    - **Examples:**
        - `send_email_job.py`: Sends emails asynchronously (e.g., account confirmation, notifications).
        - `generate_report_job.py`: Generates large or time-consuming reports in the background (e.g., sales reports).
        - `data_cleanup_job.py`: Periodically removes outdated or redundant data from the database.
        - `process_refunds_job.py`: Handles refund processing asynchronously.
        - `sync_inventory_job.py`: Updates inventory levels from suppliers.
        - `send_push_notification_job.py`: Sends push notifications to users.
        - `schedule_backup_job.py`: Creates backups of application data.
        - `refresh_access_tokens_job.py`: Refreshes expired OAuth tokens.
        - `archive_logs_job.py`: Archives application logs for long-term storage.
        - `resize_images_job.py`: Optimizes uploaded images for better performance.

* * *
