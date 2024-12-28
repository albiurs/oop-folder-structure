# Adapter pattern for external systems

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── infrastructure/     # Technical details and external system interaction
│   │   ├── adapters/       # Adapter pattern for external systems
│   │   │   ├── stripe_adapter.py
│   │   │   └── mailchimp_adapter.py
```


### **Folder Structure Explanation**

* * *

#### **`infrastructure/`**

- **Purpose:** Manages the **technical and integration details** of the application, including interaction with databases, external services, middleware, caching, and runtime guards.
    - **`adapters/`**: Implements the Adapter Pattern for interacting with external systems or APIs.
        - Examples:
            - `stripe_adapter.py`: Handles payment processing with Stripe.
            - `mailchimp_adapter.py`: Manages email campaigns and lists via Mailchimp.
            - `paypal_adapter.py`: Integrates with PayPal for payment handling.
            - `sms_adapter.py`: Sends SMS messages through a third-party provider.
            - `google_maps_adapter.py`: Retrieves geolocation data using Google Maps API.
            - `facebook_adapter.py`: Integrates social login or other interactions with Facebook.
            - `twilio_adapter.py`: Sends SMS or manages voice calls via Twilio.
            - `s3_adapter.py`: Manages file storage and retrieval in Amazon S3.
            - `slack_adapter.py`: Sends notifications to Slack channels.
            - `auth0_adapter.py`: Interfaces with Auth0 for authentication and authorization.

* * *
