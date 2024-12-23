# Technical details and external system interaction

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
│   │   ├── cache/          # Caching logic
│   │   │   ├── ProductCache.php
│   │   │   └── UserCache.php
│   │   ├── exceptions/     # Custom exception classes
│   │   │   ├── PaymentFailedException.php
│   │   │   └── UserNotFoundException.php
│   │   ├── guards/         # Runtime checks for access or rules
│   │   │   ├── AdminGuard.php
│   │   │   └── AgeVerificationGuard.php
│   │   ├── middleware/     # Middleware logic (e.g., for HTTP requests)
│   │   │   ├── AuthenticationMiddleware.php
│   │   │   └── LoggingMiddleware.php
│   │   └── repositories/   # Database access and data persistence
│   │       ├── OrderRepository.php
│   │       ├── ProductRepository.php
│   │       └── UserRepository.php
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
    - **`cache/`**: Implements caching mechanisms to reduce database load and improve response times.
        - Examples:
            - `UserCache.php`: Stores frequently accessed user data for quick retrieval.
            - `ProductCache.php`: Caches product listings or details for performance.
            - `OrderCache.php`: Caches order summaries or recent order data.
            - `CategoryCache.php`: Stores category hierarchies for quick navigation.
            - `SearchCache.php`: Caches search results for common queries.
            - `NotificationCache.php`: Stores notifications for quick delivery to clients.
            - `DiscountCache.php`: Caches active discount codes and their attributes.
            - `CartCache.php`: Temporarily stores user shopping carts for session persistence.
            - `InventoryCache.php`: Tracks product stock levels to avoid repeated database queries.
            - `UserPreferenceCache.php`: Caches user-specific settings or preferences.
    - **`exceptions/`**: Defines custom exception classes for application-specific errors.
        - Examples:
            - `UserNotFoundException.php`: Thrown when a user is not found in the database.
            - `PaymentFailedException.php`: Raised when a payment attempt fails.
            - `InvalidDiscountCodeException.php`: Thrown when a discount code is invalid or expired.
            - `UnauthorizedAccessException.php`: Raised when a user attempts to access restricted resources.
            - `OrderProcessingException.php`: Indicates errors during order processing.
            - `ProductOutOfStockException.php`: Raised when a user attempts to purchase an out-of-stock product.
            - `SubscriptionExpiredException.php`: Thrown when a user’s subscription has lapsed.
            - `EmailAlreadyUsedException.php`: Raised when a duplicate email is encountered during registration.
            - `CategoryNotFoundException.php`: Thrown when a category is not found in the database.
            - `ValidationException.php`: Raised when input data fails validation rules.
    - **`guards/`**: Contains runtime checks for enforcing application rules or restrictions.
        - Examples:
            - `AdminGuard.php`: Ensures that only admin users can access certain routes or features.
            - `AgeVerificationGuard.php`: Restricts access based on user age (e.g., for age-restricted products).
            - `SubscriptionGuard.php`: Validates active subscriptions for premium features.
            - `OrderOwnershipGuard.php`: Ensures that users can only view or modify their own orders.
            - `PaymentVerificationGuard.php`: Verifies that payments are completed before granting access.
            - `ContentAccessGuard.php`: Restricts access to premium or restricted content.
            - `FeatureFlagGuard.php`: Enables or disables features based on feature flags.
            - `AuthenticationGuard.php`: Ensures that the user is logged in before accessing protected resources.
            - `EmailVerifiedGuard.php`: Ensures users have verified their email addresses before proceeding.
            - `CartGuard.php`: Verifies that the cart meets certain conditions (e.g., minimum total).
    - **`middleware/`**: Contains logic for processing HTTP requests and responses, such as authentication or logging.
        - Examples:
            - `AuthenticationMiddleware.php`: Ensures that users are authenticated for protected routes.
            - `LoggingMiddleware.php`: Logs incoming requests and responses for debugging purposes.
            - `RateLimitingMiddleware.php`: Enforces request rate limits for APIs.
            - `CorsMiddleware.php`: Handles Cross-Origin Resource Sharing policies.
            - `AuthorizationMiddleware.php`: Checks user permissions for requested actions.
            - `LocalizationMiddleware.php`: Sets the language/locale for the current request.
            - `RequestValidationMiddleware.php`: Validates incoming request data against predefined schemas.
            - `ErrorHandlingMiddleware.php`: Centralizes error handling and formatting for client responses.
            - `SessionMiddleware.php`: Manages session data for authenticated users.
            - `CacheMiddleware.php`: Implements caching for specific requests to improve performance.
    - **`repositories/`**: Interfaces with the database for CRUD operations and advanced queries.
        - Examples:
            - `UserRepository.php`: Handles database operations for users, such as fetching or updating user records.
            - `ProductRepository.php`: Manages data persistence and retrieval for products.
            - `OrderRepository.php`: Interfaces with the database for order-related actions.
            - `CategoryRepository.php`: Queries and manages product categories.
            - `ReviewRepository.php`: Handles retrieval and storage of product reviews.
            - `InvoiceRepository.php`: Manages invoice records in the database.
            - `CartRepository.php`: Handles shopping cart persistence.
            - `PaymentRepository.php`: Manages payment-related records and queries.
            - `NotificationRepository.php`: Stores and retrieves user notifications.
            - `SubscriptionRepository.php`: Handles recurring subscription data.

* * *
