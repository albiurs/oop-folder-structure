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

- **Purpose:** Manages the **technical and integration details** of the application, including interaction with databases, external services, middleware, caching, and runtime guards.
    - **`adapters/`**: Implements the Adapter Pattern for interacting with external systems or APIs.
        - Examples:
            - `StripeAdapter.php`: Handles payment processing with Stripe.
            - `MailchimpAdapter.php`: Manages email campaigns and lists via Mailchimp.
            - `PayPalAdapter.php`: Integrates with PayPal for payment handling.
            - `SMSAdapter.php`: Sends SMS messages through a third-party provider.
            - `GoogleMapsAdapter.php`: Retrieves geolocation data using Google Maps API.
            - `FacebookAdapter.php`: Integrates social login or other interactions with Facebook.
            - `TwilioAdapter.php`: Sends SMS or manages voice calls via Twilio.
            - `S3Adapter.php`: Manages file storage and retrieval in Amazon S3.
            - `SlackAdapter.php`: Sends notifications to Slack channels.
            - `Auth0Adapter.php`: Interfaces with Auth0 for authentication and authorization.

* * *
