# Test data

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── tests/              # Test cases
│   │   │
│   │   ├── fixtures/       # Test data
│   │   │   ├── sample_users.json
│   │   │   ├── test_orders.csv
│   │   │   └── sample_products.json

```


### **Folder Structure Explanation**

* * *

#### **`tests/`**

- **Purpose:** Contains all **test cases** to ensure the application works as expected. Organized into unit tests, integration tests, end-to-end (e2e) tests, and other specialized test resources.
    - **`fixtures/`**: Provides sample test data (e.g., mock users, products, or orders).
        - Examples:
            - `sample_users.json`: Contains test user data for authentication and profiles.
            - `sample_products.json`: Includes mock product data for testing catalog features.
            - `test_orders.csv`: Provides sample orders for validating order processing.
            - `sample_categories.json`: Test data for product categories.
            - `sample_inventory.yaml`: Mock inventory data for stock-level tests.
            - `test_addresses.json`: Addresses used in shipping and billing workflows.
            - `sample_transactions.json`: Simulated transaction data for payment tests.
            - `test_reviews.json`: Sample product reviews for testing review features.
            - `sample_discounts.csv`: Test data for validating discount calculations.
            - `test_notifications.json`: Mock notifications for testing notification systems.

* * *
