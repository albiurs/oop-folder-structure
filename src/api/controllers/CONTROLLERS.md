# API controllers

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── api/                # API-specific components
│   │   ├── controllers/    # API controllers
│   │   │   ├── user_controller.py
│   │   │   ├── product_controller.py
│   │   │   └── order_controller.py
```


### **Folder Structure Explanation**

* * *

#### **`api/`**

- **Purpose:** Handles all API-related functionalities, exposing endpoints for client interactions and managing data flow between the backend and frontend or external services. It ensures consistent data representation and encapsulates logic related to HTTP requests and responses.
    - `controllers/`: These files process HTTP requests, call relevant services, and return appropriate responses (e.g., JSON or HTTP status codes). Controllers act as the interface between external requests and internal logic.
        - Examples:
            - `user_controller.py`: Processes requests like registering users, fetching user data, or updating profiles.
            - `order_controller.py`: Handles endpoints like placing an order, viewing order history, or canceling an order.
            - `auth_controller.py`: Manages authentication, including login, logout, and token refresh.
            - `product_controller.py`: Handles product-related CRUD operations like adding, updating, or deleting products.
            - `payment_controller.py`: Processes requests for initiating or validating payments.
            - `category_controller.py`: Manages endpoints for retrieving or modifying product categories.
            - `profile_controller.py`: Handles user profile updates or preferences.
            - `notification_controller.py`: Manages sending or retrieving notifications for users.
            - `report_controller.py`: Exposes endpoints to generate and download reports.
            - `review_controller.py`: Handles product review creation, updates, and retrieval.

* * *
