# Configuration files

## Folder Structure

```
project/
│
├── config/             # Configuration files
│   ├── env/            # Environment configuration
│   │   ├── development.env
│   │   ├── production.env
│   │   ├── staging.env
│   │   └── testing.env
│   ├── db_config.py
│   ├── app_config.py
│   └── cache_config.py
```


### **Folder Structure Explanation**

* * *

#### **`config/`**

- **Purpose:** Stores **configuration files** for various aspects of the application, such as database connections, caching, API keys, or feature toggles.
    - **Examples:**
        - `database.py`: Contains database connection settings, credentials, and driver details.
        - `app.py`: Configures application-level settings (e.g., environment, timezone, debug mode).
        - `cache.py`: Defines caching strategies, backends (e.g., Redis, Memcached), and expiration times.
        - `api.py`: Stores API-specific settings, such as rate limits or base URLs.
        - `mail.py`: Configures mail servers and templates for outgoing emails.
        - `logging.py`: Defines logging levels, destinations (e.g., files, cloud services), and formats.
        - `queue.py`: Configures job queues, workers, and retry policies.
        - `services.py`: Stores credentials and endpoints for third-party services (e.g., Stripe, AWS).
        - `features.py`: Enables or disables application features using feature flags.
        - `security.py`: Configures security settings (e.g., encryption keys, allowed IPs, CORS rules).
    - **`env/`**: The project/config/env folder is designed to house environment-specific configuration files, which help manage different setups for various environments like development, testing, staging, and production. These files typically store environment variables and settings that are specific to each deployment scenario.
        - **Examples:**
            - `development.env`: Settings for development environment.
            - `production.env`:  Settings for production environment.
            - `staging.env`: Settings for staging/pre-production environment.
            - `testing.env`: Settings for testing environment.

* * *
