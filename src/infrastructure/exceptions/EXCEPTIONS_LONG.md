# Custom exception classes

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── infrastructure/     # Technical details and external system interaction
│   │   ├── exceptions/     # Custom exception classes
│   │   │   ├── PaymentFailedException.php
│   │   │   └── UserNotFoundException.php
```


### **Folder Structure Explanation**

* * *

#### **`infrastructure/`**

- **Purpose:** Manages the **technical and integration details** of the application, including interaction with databases, external services, middleware, caching, and runtime guards.
    - **`exceptions/`**: Defines custom exception classes for application-specific errors.
        - Examples:
            - `UserNotFoundException.php`: Thrown when a user is not found in the database.
            - `PaymentFailedException.php`: Raised when a payment attempt fails.
            - `InvalidDiscountCodeException.php`: Thrown when a discount code is invalid or expired.
            - `UnauthorizedAccessException.php`: Raised when a user attempts to access restricted resources.
            - `OrderProcessingException.php`: Indicates errors during order processing.
            - `ProductOutOfStockException.php`: Raised when a user attempts to purchase an out-of-stock product.
            - `SubscriptionExpiredException.php`: Thrown when a user’s subscription has lapsed.
            - `EmailAlreadyUsedException.php`: Raised when a duplicate email is encountered during registration.
            - `CategoryNotFoundException.php`: Thrown when a category is not found in the database.
            - `ValidationException.php`: Raised when input data fails validation rules.

* * *
