# API controllers

## Folder Structure

```
project/
│
├── src/                    # Source code
│   ├── api/                # API-specific components
│   │   ├── controllers/    # API controllers
│   │   │   ├── OrderController.php
│   │   │   ├── ProductController.php
│   │   │   └── UserController.php
```


### **Folder Structure Explanation**

* * *

#### **`api/`**

- **Purpose:** Handles all API-related functionalities, exposing endpoints for client interactions and managing data flow between the backend and frontend or external services. It ensures consistent data representation and encapsulates logic related to HTTP requests and responses.
    - **`controllers/`**: These files process HTTP requests, call relevant services, and return appropriate responses (e.g., JSON or HTTP status codes). Controllers act as the interface between external requests and internal logic.
        - Examples:
            - `UserController.php`: Processes requests like registering users, fetching user data, or updating profiles.
            - `OrderController.php`: Handles endpoints like placing an order, viewing order history, or canceling an order.
            - `AuthController.php`: Manages authentication, including login, logout, and token refresh.
            - `ProductController.php`: Handles product-related CRUD operations like adding, updating, or deleting products.
            - `PaymentController.php`: Processes requests for initiating or validating payments.
            - `CategoryController.php`: Manages endpoints for retrieving or modifying product categories.
            - `ProfileController.php`: Handles user profile updates or preferences.
            - `NotificationController.php`: Manages sending or retrieving notifications for users.
            - `ReportController.php`: Exposes endpoints to generate and download reports.
            - `ReviewController.php`: Handles product review creation, updates, and retrieval.

* * *
