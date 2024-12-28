# Caching logic

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── infrastructure/     # Technical details and external system interaction
│   │   ├── cache/          # Caching logic
│   │   │   ├── user_cache.py
│   │   │   └── product_cache.py
```


### **Folder Structure Explanation**

* * *

#### **`infrastructure/`**

- **Purpose:** Manages the **technical and integration details** of the application, including interaction with databases, external services, middleware, caching, and runtime guards.
    - **`cache/`**: Implements caching mechanisms to reduce database load and improve response times.
        - Examples:
            - `user_cache.py`: Stores frequently accessed user data for quick retrieval.
            - `product_cache.py`: Caches product listings or details for performance.
            - `order_cache.py`: Caches order summaries or recent order data.
            - `category_cache.py`: Stores category hierarchies for quick navigation.
            - `search_cache.py`: Caches search results for common queries.
            - `notification_cache.py`: Stores notifications for quick delivery to clients.
            - `discount_cache.py`: Caches active discount codes and their attributes.
            - `cart_cache.py`: Temporarily stores user shopping carts for session persistence.
            - `inventory_cache.py`: Tracks product stock levels to avoid repeated database queries.
            - `user_preference_cache.py`: Caches user-specific settings or preferences.

* * *
