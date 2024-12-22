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

- **Purpose:** Encapsulates core business logic and domain-specific models.
    - **`value_objects/`**: Represents immutable objects with specific value logic.
        - Examples:
            - `Money.php`: Handles currency and arithmetic for monetary values.
            - `Address.php`: Represents a user's address in a standardized way.
            - `Coordinates.php`: Encapsulates latitude and longitude for geolocation.

* * *
