# Query objects for fetching data

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── application/        # Application-specific logic
│   │   ├── queries/        # Query objects for fetching data
│   │   │   ├── get_user_by_id_query.py
│   │   │   └── list_orders_query.py
```


### **Folder Structure Explanation**

* * *

#### `application/`

- **Purpose:** Implements the main workflows and use cases of the application. This folder bridges domain logic with external systems and user actions, encapsulating high-level business logic.
    - `queries/`: Handles read-only operations by encapsulating data-fetching logic. Queries are responsible for retrieving specific data efficiently and clearly.
        - Examples:
            - `get_user_by_id_query.py`: Retrieves a user by their unique ID.
            - `list_orders_query.py`: Returns all orders for a specific user or timeframe.
            - `get_product_details_query.py`: Fetches detailed product information by ID.
            - `search_products_query.py`: Retrieves products matching search criteria.
            - `get_category_by_id_query.py`: Retrieves a category by its identifier.
            - `get_order_history_query.py`: Fetches a user’s past orders.
            - `fetch_notifications_query.py`: Retrieves unread notifications for a user.
            - `list_reviews_query.py`: Retrieves product reviews from the database.
            - `get_report_data_query.py`: Retrieves data required for generating reports.
            - `get_discounts_query.py`: Fetches available discount codes or coupons.

* * *
