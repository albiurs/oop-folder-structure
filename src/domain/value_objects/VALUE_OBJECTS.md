# Value objects (e.g., immutable types)

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   │   └── value_objects/  # Value objects (e.g., immutable types)
│   │       ├── money.py
│   │       └── address.py
```


### **Folder Structure Explanation**

* * *

#### **`domain/`**

- **Purpose:** Represents the **core business logic and rules** of the application. This folder encapsulates the domain-specific models, value objects, and domain events, ensuring that business logic remains independent of technical or application concerns.
    - **`value_objects/`**: Represents immutable, domain-specific data types like money, dates, or units.
        - Examples:
            - `money.py`: Handles monetary values with precision and currency types.
            - `address.py`: Represents a postal address, including `street`, `city`, and `postal_code`.
            - `email.py`: Validates and stores email addresses as immutable objects.
            - `phone_number.py`: Encapsulates and validates phone number data.
            - `coordinates.py`: Represents latitude and longitude for geolocation purposes.
            - `tax_rate.py`: Models tax rates applicable to transactions.
            - `discount_code.py`: Encodes discount codes and their validity.
            - `currency.py`: Represents different currencies for global transactions.
            - `date_range.py`: Encapsulates a range of dates, e.g., for promotions or reports.
            - `order_status.py`: Represents the possible states of an order (e.g., `Pending`, `Shipped`, `Completed`).

* * *
