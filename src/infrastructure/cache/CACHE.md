# Caching logic

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── infrastructure/     # Technical details and external system interaction
│   │   ├── cache/          # Caching logic
│   │   │   ├── ProductCache.php
│   │   │   └── UserCache.php
```


### **Folder Structure Explanation**

* * *

#### **`infrastructure/`**

- **Purpose:** Manages technical implementation details and external system interactions.
    - **`cache/`**: Implements caching logic for performance improvements.
        - Examples:
            - `UserCache.php`: Caches user data to reduce database load.
            - `ProductCache.php`: Stores frequently accessed product details.
            - `OrderCache.php`: Speeds up retrieval of recent order data.

* * *
