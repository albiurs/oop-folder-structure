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

- **Purpose:** Defines **authorization logic** to enforce access control for resources and actions. Policies determine whether a user is allowed to perform certain actions, ensuring the security of the application.
    - **Examples:**
        - `UserPolicy.php`: Governs what actions a user can perform on other users (e.g., admin can delete users).
        - `PostPolicy.php`: Controls whether a user can edit, delete, or publish posts.
        - `OrderPolicy.php`: Restricts order viewing and modification to order owners.
        - `PaymentPolicy.php`: Ensures only authorized users can initiate refunds or cancellations.
        - `SubscriptionPolicy.php`: Governs access to subscription-based features.
        - `CommentPolicy.php`: Determines who can delete or report comments.
        - `CategoryPolicy.php`: Restricts category creation or deletion to admins.
        - `InvoicePolicy.php`: Limits invoice access to relevant users or admins.
        - `ProductPolicy.php`: Controls whether users can add, edit, or delete products.
        - `RolePolicy.php`: Ensures only specific roles (e.g., admin) can assign or remove roles from users.

* * *
