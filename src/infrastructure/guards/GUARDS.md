# Runtime checks for access or rules

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── infrastructure/     # Technical details and external system interaction
│   │   ├── guards/         # Runtime checks for access or rules
│   │   │   ├── AdminGuard.php
│   │   │   └── AgeVerificationGuard.php
```


### **Folder Structure Explanation**

* * *

#### **`infrastructure/`**

- **Purpose:** Manages the **technical and integration details** of the application, including interaction with databases, external services, middleware, caching, and runtime guards.
    - **`guards/`**: Contains runtime checks for enforcing application rules or restrictions.
        - Examples:
            - `AdminGuard.php`: Ensures that only admin users can access certain routes or features.
            - `AgeVerificationGuard.php`: Restricts access based on user age (e.g., for age-restricted products).
            - `SubscriptionGuard.php`: Validates active subscriptions for premium features.
            - `OrderOwnershipGuard.php`: Ensures that users can only view or modify their own orders.
            - `PaymentVerificationGuard.php`: Verifies that payments are completed before granting access.
            - `ContentAccessGuard.php`: Restricts access to premium or restricted content.
            - `FeatureFlagGuard.php`: Enables or disables features based on feature flags.
            - `AuthenticationGuard.php`: Ensures that the user is logged in before accessing protected resources.
            - `EmailVerifiedGuard.php`: Ensures users have verified their email addresses before proceeding.
            - `CartGuard.php`: Verifies that the cart meets certain conditions (e.g., minimum total).

* * *
