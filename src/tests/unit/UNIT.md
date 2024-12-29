# Unit tests

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── tests/              # Test cases
│   │   │
│   │   └── unit/           # Unit tests
│   │       ├── test_user_model.py
│   │       ├── test_order_validation.py
│   │       └── test_product_price_calculation.py

```


### **Folder Structure Explanation**

* * *

#### **`tests/`**

- **Purpose:** Contains all **test cases** to ensure the application works as expected. Organized into unit tests, integration tests, end-to-end (e2e) tests, and other specialized test resources.
    - **`unit/`**: Tests individual components or functions in isolation.
        - Examples:
            - `test_user_model.py`: Validates the behavior of the `User` model.
            - `test_order_validation.py`: Tests order-related validation logic.
            - `test_product_price_calculation.py`: Ensures correct price calculations for products.
            - `test_email_formatter.py`: Verifies email formatting functions.
            - `test_api_response_helper.py`: Tests helper methods for API responses.
            - `test_cart_service.py`: Tests the cart service for adding, removing, and updating items.
            - `test_date_parser.py`: Verifies date parsing utility functions.
            - `test_discount_calculator.py`: Validates logic for applying discounts.
            - `test_notification_sender.py`: Ensures notifications are triggered correctly.
            - `test_authentication_validator.py`: Tests user authentication validation logic.

* * *
