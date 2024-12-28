# Runtime checks for access or rules

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── infrastructure/     # Technical details and external system interaction
│   │   ├── guards/         # Runtime checks for access or rules
│   │   │   ├── admin_guard.py
│   │   │   └── age_verification_guard.py
```


### **Folder Structure Explanation**

* * *

#### **`infrastructure/`**

- **Purpose:** Manages the **technical and integration details** of the application, including interaction with databases, external services, middleware, caching, and runtime guards.
    - **`guards/`**: Contains runtime checks for enforcing application rules or restrictions.
        - Examples:
            - `admin_guard.py`: Ensures that only admin users can access certain routes or features.
            - `age_verification_guard.py`: Restricts access based on user age (e.g., for age-restricted products).
            - `subscription_guard.py`: Validates active subscriptions for premium features.
            - `order_ownership_guard.py`: Ensures that users can only view or modify their own orders.
            - `payment_verification_guard.py`: Verifies that payments are completed before granting access.
            - `content_access_guard.py`: Restricts access to premium or restricted content.
            - `feature_flag_guard.py`: Enables or disables features based on feature flags.
            - `authentication_guard.py`: Ensures that the user is logged in before accessing protected resources.
            - `email_verified_guard.py`: Ensures users have verified their email addresses before proceeding.
            - `cart_guard.py`: Verifies that the cart meets certain conditions (e.g., minimum total).

* * *
