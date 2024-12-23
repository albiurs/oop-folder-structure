# Configuration files

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── config/             # Configuration files
│   │   ├── app.php
│   │   ├── cache.php
│   │   └── database.php
```


### **Folder Structure Explanation**

* * *

#### **`config/`**

#### **`config/`**

- **Purpose:** Stores **configuration files** for various aspects of the application, such as database connections, caching, API keys, or feature toggles.
    - **Examples:**
        - `database.php`: Contains database connection settings, credentials, and driver details.
        - `app.php`: Configures application-level settings (e.g., environment, timezone, debug mode).
        - `cache.php`: Defines caching strategies, backends (e.g., Redis, Memcached), and expiration times.
        - `api.php`: Stores API-specific settings, such as rate limits or base URLs.
        - `mail.php`: Configures mail servers and templates for outgoing emails.
        - `logging.php`: Defines logging levels, destinations (e.g., files, cloud services), and formats.
        - `queue.php`: Configures job queues, workers, and retry policies.
        - `services.php`: Stores credentials and endpoints for third-party services (e.g., Stripe, AWS).
        - `features.php`: Enables or disables application features using feature flags.
        - `security.php`: Configures security settings (e.g., encryption keys, allowed IPs, CORS rules).

* * *
