# Technical details and external system interaction

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
│   │   ├── cache/          # Caching logic
│   │   │   ├── user_cache.py
│   │   │   └── product_cache.py
│   │   ├── events/           # Event dispatching infrastructure
│   │   │   ├── event_bus.py
│   │   │   ├── event_dispatcher.py
│   │   │   └── event_logger.py
│   │   ├── exceptions/     # Custom exception classes
│   │   │   ├── user_not_found_exception.py
│   │   │   └── payment_failed_exception.py
│   │   ├── guards/         # Runtime checks for access or rules
│   │   │   ├── admin_guard.py
│   │   │   └── age_verification_guard.py
│   │   ├── localization/   # Handles locales and related logic
│   │   │   ├── locale_manager.py
│   │   │   ├── locale_adapter.py
│   │   │   └── locale_parser.py
│   │   ├── middleware/     # Middleware logic (e.g., for HTTP requests)
│   │   │   ├── authentication_middleware.py
│   │   │   └── logging_middleware.py
│   │   └── repositories/   # Database access and data persistence
│   │       ├── user_repository.py
│   │       ├── product_repository.py
│   │       └── order_repository.py
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
    - **`events/`**: Defines **infrastructure-specific events** that are raised when significant actions occur. These events deal with **technical/system-level concerns**, such as logging, monitoring, and communication between different parts of the application or external systems. These events are related to the **technical infrastructure** and support the application’s runtime environment. An **event** represents something that has occurred in the system. It’s a plain data object or class encapsulating information about the occurrence. Events are typically created by a component when it completes a significant action, such as a user login, a file upload, or a transaction completion. Events trigger specific reactions (handled by **listeners** or **subscribers**).
        - Examples:
            - `cache_invalidation_event.py`: Represents invalidation of a cache entry.
            - `api_request_received_event.py`: Represents when an API request is received.
            - `database_replication_event.py`: Indicates that data needs to be replicated to another database.
            - `message_queue_event.py`: Represents the publication or consumption of a message from a queue (e.g., RabbitMQ, Kafka).
            - `log_event.py`: Represents a logging action within the system.
            - `email_delivery_event.py`: dicates that an email was successfully delivered or failed.
            - `file_upload_completed_event.py`: Represents the successful upload of a file.
            - `third_party_api_response_event.py`: Represents the response from an external API.
            - `background_job_completed_event.py`: Represents the completion of an asynchronous task.
            - `service_shutdown_event.py`: Indicates that a service (e.g., a worker or web server) is shutting down.
    - **`exceptions/`**: Defines custom exception classes for application-specific errors.
        - Examples:
            - `user_not_found_exception.py`: Raised when a user is not found in the database.
            - `payment_failed_exception.py`: Raised when a payment attempt fails.
            - `invalid_discount_code_exception.py`: Thrown when a discount code is invalid or expired.
            - `unauthorized_access_exception.py`: Raised when a user attempts to access restricted resources.
            - `order_processing_exception.py`: Indicates errors during order processing.
            - `product_out_of_stock_exception.py`: Raised when a user attempts to purchase an out-of-stock product.
            - `subscription_expired_exception.py`: Thrown when a user’s subscription has lapsed.
            - `email_already_used_exception.py`: Raised when a duplicate email is encountered during registration.
            - `category_not_found_exception.py`: Thrown when a category is not found in the database.
            - `validation_exception.py`: Raised when input data fails validation rules.
    - **`guards/`**: Contains runtime checks for enforcing application rules or restrictions.
        - Examples:
            - `admin_guard.py`: Ensures that only admin users can access certain routes or features.
            - `age_verification_guard.py`: Restricts access based on user age (e.g., for age-restricted products).
            - `subscription_guard.py`: Validates active subscriptions for premium features.
            - `order_ownership_guard.py`: Ensures that users can only view or modify their own orders.
            - `payment_verification_guard.py`: Verifies that payments are completed before granting access.
            - `content_access_guard.py`: Restricts access to premium or restricted content.
            - `feature_flag_guard.py`: Enables or disables features based on feature flags.
            - `authentication_guard.py`: Ensures that the user is logged in before accessing protected resources.
            - `email_verified_guard.py`: Ensures users have verified their email addresses before proceeding.
            - `cart_guard.py`: Verifies that the cart meets certain conditions (e.g., minimum total).
    - **`localization/`**: The src/infrastructure/localization/ folder is dedicated to handling the logic and technical implementation of localization (L10N) and internationalization (I18N). This folder typically interacts with user-facing locales/ files and provides the underlying functionality to manage translations, formatting, and other locale-specific behavior (e.g., date formatting, currency). The logic here could include managing translations, detecting user preferences, or interfacing with third-party libraries like ICU, gettext, or custom locale parsers.
        - Examples:
            - `locale_manager.py`: Main class or module managing localization features.
            - `locale_loader.py`: Logic for loading locale files into memory.
            - `locale_detector.py`: Detects user's preferred locale from settings or request headers.
            - `locale_adapter.py`: Adapts external libraries or APIs for localization.
            - `locale_cache.py`: Implements caching for frequently used translations.
            - `translation_service.py`: Handles retrieving translations for specific keys.
            - `date_formatter.py`: Formats dates/times based on locale.
            - `number_formatter.py`: Formats numbers, currencies, and percentages.
            - `locale_parser.py`: Parses locale files (e.g., JSON, YAML) into usable structures.
            - `locale_validator.py`: Validates locale files and checks for missing translations.
    - **`middleware/`**: Contains logic for processing HTTP requests and responses, such as authentication or logging.
        - Examples:
            - `authentication_middleware.py`: Ensures that users are authenticated for protected routes.
            - `logging_middleware.py`: Logs incoming requests and responses for debugging purposes.
            - `rate_limiting_middleware.py`: Enforces request rate limits for APIs.
            - `cors_middleware.py`: Handles Cross-Origin Resource Sharing policies.
            - `authorization_middleware.py`: Checks user permissions for requested actions.
            - `localization_middleware.py`: Sets the language/locale for the current request.
            - `request_validation_middleware.py`: Validates incoming request data against predefined schemas.
            - `error_handling_middleware.py`: Centralizes error handling and formatting for client responses.
            - `session_middleware.py`: Manages session data for authenticated users.
            - `cache_middleware.py`: Implements caching for specific requests to improve performance.
    - **`repositories/`**: Interfaces with the database for CRUD operations and advanced queries.
        - Examples:
            - `user_repository.py`: Handles database operations for users, such as fetching or updating user records.
            - `product_repository.py`: Manages data persistence and retrieval for products.
            - `order_repository.py`: Interfaces with the database for order-related actions.
            - `category_repository.py`: Queries and manages product categories.
            - `review_repository.py`: Handles retrieval and storage of product reviews.
            - `invoice_repository.py`: Manages invoice records in the database.
            - `cart_repository.py`: Handles shopping cart persistence.
            - `payment_repository.py`: Manages payment-related records and queries.
            - `notification_repository.py`: Stores and retrieves user notifications.
            - `subscription_repository.py`: Handles recurring subscription data.

* * *
