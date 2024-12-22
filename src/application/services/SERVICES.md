# Business logic and reusable services

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── application/        # Application-specific logic
│   │   ├── services/       # Business logic and reusable services
│   │   │   ├── EmailService.php
│   │   │   ├── PaymentService.php
│   │   │   └── UserService.php
```


### **Folder Structure Explanation**

* * *

#### **`application/`**

- **Purpose:** Implements application-specific logic, bridging APIs with domain logic.
    - **`services/`**: Contains reusable business logic used across the app.
        - Examples:
            - `PaymentService.php`: Processes payments using a third-party API.
            - `EmailService.php`: Sends email notifications to users.
            - `UserService.php`: Manages user-related business logic, like profile updates.

* * *
