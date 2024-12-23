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

- **Purpose:** Manages the **technical and integration details** of the application, including interaction with databases, external services, middleware, caching, and runtime guards.
    - **`cache/`**: Implements caching mechanisms to reduce database load and improve response times.
        - Examples:
            - `UserCache.php`: Stores frequently accessed user data for quick retrieval.
            - `ProductCache.php`: Caches product listings or details for performance.
            - `OrderCache.php`: Caches order summaries or recent order data.
            - `CategoryCache.php`: Stores category hierarchies for quick navigation.
            - `SearchCache.php`: Caches search results for common queries.
            - `NotificationCache.php`: Stores notifications for quick delivery to clients.
            - `DiscountCache.php`: Caches active discount codes and their attributes.
            - `CartCache.php`: Temporarily stores user shopping carts for session persistence.
            - `InventoryCache.php`: Tracks product stock levels to avoid repeated database queries.
            - `UserPreferenceCache.php`: Caches user-specific settings or preferences.

* * *
