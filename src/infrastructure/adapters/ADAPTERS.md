# Adapter pattern for external systems

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── infrastructure/     # Technical details and external system interaction
│   │   ├── adapters/       # Adapter pattern for external systems
│   │   │   ├── MailchimpAdapter.php
│   │   │   └── StripeAdapter.php
```


### **Folder Structure Explanation**

* * *

#### **`infrastructure/`**

- **Purpose:** Manages technical implementation details and external system interactions.
    - **`adapters/`**: Implements integrations with third-party systems.
        - Examples:
            - `StripeAdapter.php`: Integrates with Stripe for payment processing.
            - `MailchimpAdapter.php`: Handles email marketing through Mailchimp.
            - `AWSAdapter.php`: Interfaces with AWS services like S3 or SNS.

* * *
