# Query objects for fetching data

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── application/        # Application-specific logic
│   │   ├── queries/        # Query objects for fetching data
│   │   │   ├── GetUserByIdQuery.php
│   │   │   └── ListOrdersQuery.php
```


### **Folder Structure Explanation**

* * *

#### **`application/`**

- **Purpose:** Implements the main workflows and use cases of the application. This folder bridges domain logic with external systems and user actions, encapsulating high-level business logic.
    - **`queries/`**: Handles read-only operations by encapsulating data-fetching logic. Queries are responsible for retrieving specific data efficiently and clearly.
        - Examples:
            - `GetUserByIdQuery.php`: Retrieves a user by their unique ID.
            - `ListOrdersQuery.php`: Returns all orders for a specific user or timeframe.
            - `GetProductDetailsQuery.php`: Fetches detailed product information by ID.
            - `SearchProductsQuery.php`: Retrieves products matching search criteria.
            - `GetCategoryByIdQuery.php`: Retrieves a category by its identifier.
            - `GetOrderHistoryQuery.php`: Fetches a user’s past orders.
            - `FetchNotificationsQuery.php`: Retrieves unread notifications for a user.
            - `ListReviewsQuery.php`: Retrieves product reviews from the database.
            - `GetReportDataQuery.php`: Retrieves data required for generating reports.
            - `GetDiscountsQuery.php`: Fetches available discount codes or coupons.

* * *
