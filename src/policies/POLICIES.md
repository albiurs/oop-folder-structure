# Authorization policies

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── policies/           # Authorization policies
│   │   ├── post_policy.py
│   │   └── user_policy.py
```


### **Folder Structure Explanation**

* * *

#### **`policies/`**

- **Purpose:**  
  Defines **authorization logic** to enforce access control for resources and actions. Policies determine whether a user is allowed to perform certain actions, ensuring the security of the application. These files centralize authorization logic, reducing duplication and ensuring consistency.
- **Examples:**
    - `user_policy.py`: Governs what actions a user can perform on other users (e.g., admins can delete users, or users can only edit their own profiles).
    - `post_policy.py`: Controls whether a user can edit, delete, or publish posts, ensuring only authors or authorized users have access.
    - `order_policy.py`: Restricts order viewing and modification to order owners or administrators.
    - `payment_policy.py`: Ensures only authorized users can initiate refunds, chargebacks, or cancellations.
    - `subscription_policy.py`: Governs access to subscription-based features, such as premium content or tiered plans.
    - `comment_policy.py`: Determines who can delete, edit, or report comments, often limited to the original author or moderators.
    - `category_policy.py`: Restricts category creation, editing, or deletion to administrators or users with specific permissions.
    - `invoice_policy.py`: Limits invoice access to relevant users (e.g., the customer) or administrative users.
    - `product_policy.py`: Controls whether users can add, edit, or delete products, typically reserved for vendors or admins.
    - `role_policy.py`: Ensures only specific roles (e.g., admin or super-admin) can assign or remove roles from users, preventing privilege escalation.

* * *
