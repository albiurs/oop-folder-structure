# Value objects (e.g., immutable types)

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── domain/             # Core domain models and business logic
│   │   └── value_objects/  # Value objects (e.g., immutable types)
│   │       ├── Address.php
│   │       └── Money.php
```


### **Folder Structure Explanation**

* * *

#### **`domain/`**

- **Purpose:** Represents the **core business logic and rules** of the application. This folder encapsulates the domain-specific models, value objects, and domain events, ensuring that business logic remains independent of technical or application concerns.
    - **`value_objects/`**: Represents immutable, domain-specific data types like money, dates, or units.
        - Examples:
            - `Money.php`: Handles monetary values with precision and currency types.
            - `Address.php`: Represents a postal address, including `street`, `city`, and `postalCode`.
            - `Email.php`: Validates and stores email addresses as immutable objects.
            - `PhoneNumber.php`: Encapsulates and validates phone number data.
            - `Coordinates.php`: Represents latitude and longitude for geolocation purposes.
            - `TaxRate.php`: Models tax rates applicable to transactions.
            - `DiscountCode.php`: Encodes discount codes and their validity.
            - `Currency.php`: Represents different currencies for global transactions.
            - `DateRange.php`: Encapsulates a range of dates, e.g., for promotions or reports.
            - `OrderStatus.php`: Represents the possible states of an order (e.g., `Pending`, `Shipped`, `Completed`).

* * *
