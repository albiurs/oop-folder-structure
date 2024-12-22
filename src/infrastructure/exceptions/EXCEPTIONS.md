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

- **Purpose:** Manages technical implementation details and external system interactions.
    - **`exceptions/`**: Custom exceptions for application-specific error handling.
        - Examples:
            - `UserNotFoundException.php`: Thrown when a user cannot be found.
            - `PaymentFailedException.php`: Used for payment processing failures.
            - `OrderValidationException.php`: Raised when an order is invalid.

* * *
