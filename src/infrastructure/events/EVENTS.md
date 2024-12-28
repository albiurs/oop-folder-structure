# Event dispatching infrastructure

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── infrastructure/     # Technical details and external system interaction
│   │   ├── events/           # Event dispatching infrastructure
│   │   │   ├── event_bus.py
│   │   │   ├── event_dispatcher.py
│   │   │   └── event_logger.py
```


### **Folder Structure Explanation**

* * *

#### **`infrastructure/`**

- **Purpose:** Manages the **technical and integration details** of the application, including interaction with databases, external services, middleware, caching, and runtime guards.
    - **`events/`**: Defines **infrastructure-specific events** that are raised when significant actions occur. These events deal with **technical/system-level concerns**, such as logging, monitoring, and communication between different parts of the application or external systems. These events are related to the **technical infrastructure** and support the application’s runtime environment. An **event** represents something that has occurred in the system. It’s a plain data object or class encapsulating information about the occurrence. Events are typically created by a component when it completes a significant action, such as a user login, a file upload, or a transaction completion. Events trigger specific reactions (handled by **listeners** or **subscribers**).
        - Examples:
            - `cache_invalidation_event.py`: Represents invalidation of a cache entry.
            - `api_request_received_event.py`: Represents when an API request is received.
            - `database_replication_event.py`: Indicates that data needs to be replicated to another database.
            - `message_queue_event.py`: Represents the publication or consumption of a message from a queue (e.g., RabbitMQ, Kafka).
            - `log_event.py`: Represents a logging action within the system.
            - `email_delivery_event.py`: dicates that an email was successfully delivered or failed.
            - `file_upload_completed_event.py`: Represents the successful upload of a file.
            - `third_party_api_response_event.py`: Represents the response from an external API.
            - `background_job_completed_event.py`: Represents the completion of an asynchronous task.
            - `service_shutdown_event.py`: Indicates that a service (e.g., a worker or web server) is shutting down.

* * *
