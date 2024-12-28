# Custom exception classes

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── infrastructure/     # Technical details and external system interaction
│   │   ├── exceptions/     # Custom exception classes
│   │   │   ├── user_not_found_exception.py
│   │   │   └── payment_failed_exception.py
```


### **Folder Structure Explanation**

* * *

#### **`infrastructure/`**

- **Purpose:** Manages the **technical and integration details** of the application, including interaction with databases, external services, middleware, caching, and runtime guards.
            - `service_shutdown_event.py`: Indicates that a service (e.g., a worker or web server) is shutting down.
    - **`exceptions/`**: Defines custom exception classes for application-specific errors.
        - Examples:
            - `user_not_found_exception.py`: Raised when a user is not found in the database.
            - `payment_failed_exception.py`: Raised when a payment attempt fails.
            - `invalid_discount_code_exception.py`: Thrown when a discount code is invalid or expired.
            - `unauthorized_access_exception.py`: Raised when a user attempts to access restricted resources.
            - `order_processing_exception.py`: Indicates errors during order processing.
            - `product_out_of_stock_exception.py`: Raised when a user attempts to purchase an out-of-stock product.
            - `subscription_expired_exception.py`: Thrown when a user’s subscription has lapsed.
            - `email_already_used_exception.py`: Raised when a duplicate email is encountered during registration.
            - `category_not_found_exception.py`: Thrown when a category is not found in the database.
            - `validation_exception.py`: Raised when input data fails validation rules.

* * *
