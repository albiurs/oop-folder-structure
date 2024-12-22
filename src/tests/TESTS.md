## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   └── tests/              # Test cases
│       ├── e2e/            # End-to-end tests
│       ├── fixtures/       # Test data
│       ├── integration/    # Integration tests
│       ├── mocks/          # Mock objects
│       └── unit/           # Unit tests
```


### **Folder Structure Explanation**

* * *

#### **`tests/`**

- **Purpose:** Stores all test cases to validate the application.
    - **Examples:**
        - `unit/UserTest.php`: Validates the functionality of the `User` model.
        - `integration/OrderServiceTest.php`: Tests interactions between services and repositories.
        - `e2e/CheckoutFlowTest.php`: Ensures the checkout process works end-to-end.

* * *
