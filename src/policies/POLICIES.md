# Authorization policies

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── policies/           # Authorization policies
│   │   ├── PostPolicy.php
│   │   └── UserPolicy.php
```


### **Folder Structure Explanation**

* * *

#### **`policies/`**

- **Purpose:** Defines authorization rules for various user actions.
    - **Examples:**
        - `UserPolicy.php`: Manages rules for user-related actions (e.g., editing profiles).
        - `OrderPolicy.php`: Determines permissions for managing orders.
        - `PostPolicy.php`: Handles authorization for creating or updating posts.

* * *
