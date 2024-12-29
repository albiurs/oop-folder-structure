# End-to-end tests

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── tests/              # Test cases
│   │   ├── e2e/            # End-to-end tests
│   │   │   ├── test_user_registration.py
│   │   │   ├── test_checkout_process.py
│   │   │   └── test_admin_panel_access.py

```


### **Folder Structure Explanation**

* * *

#### **`tests/`**

- **Purpose:** Contains all **test cases** to ensure the application works as expected. Organized into unit tests, integration tests, end-to-end (e2e) tests, and other specialized test resources.
    - **`e2e/`**: Simulates full workflows as the user would experience them.
        - Examples:
            - `test_user_registration.py`: Tests the full registration process from start to finish.
            - `test_checkout_process.py`: Simulates a user purchasing items.
            - `test_admin_panel_access.py`: Ensures admin users can access all necessary features.
            - `test_search_functionality.py`: Validates user-facing search workflows.
            - `test_localization.py`: Tests end-to-end functionality for multiple locales.
            - `test_password_reset.py`: Simulates a user resetting their password.
            - `test_social_login.py`: Verifies login via social media platforms.
            - `test_multi_language_support.py`: Ensures the application supports various languages end-to-end.
            - `test_subscription_workflow.py`: Tests subscription management from signup to cancellation.
            - `test_order_refund.py`: Verifies the complete refund workflow.

* * *
