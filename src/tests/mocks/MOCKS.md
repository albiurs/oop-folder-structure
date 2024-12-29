# Mock objects

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── tests/              # Test cases
│   │   │
│   │   ├── mocks/          # Mock objects
│   │   │   ├── mock_payment_gateway.py
│   │   │   ├── mock_email_service.py
│   │   │   └── mock_inventory_service.py

```


### **Folder Structure Explanation**

* * *

#### **`tests/`**

- **Purpose:** Contains all **test cases** to ensure the application works as expected. Organized into unit tests, integration tests, end-to-end (e2e) tests, and other specialized test resources.
    - **`mocks/`**: Contains mock objects to simulate external services or dependencies.
        - Examples:
            - `mock_payment_gateway.py`: Simulates external payment processing.
            - `mock_email_service.py`: Mock implementation for sending emails.
            - `mock_cache_service.py`: Simulates caching functionality.
            - `mock_inventory_service.py`: Simulates interactions with inventory systems.
            - `mock_shipping_service.py`: Mock shipping service to test order delivery.
            - `mock_logger.py`: Simulates logging functionality.
            - `mock_auth_provider.py`: Mocks external authentication providers.
            - `mock_pdf_generator.py`: Simulates PDF generation services.
            - `mock_search_service.py`: Mock implementation of search APIs.
            - `mock_notification_service.py`: Simulates notification delivery systems.

* * *
