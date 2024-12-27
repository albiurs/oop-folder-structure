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
```


### **Folder Structure Explanation**

* * *

#### **`config/`**

- **Purpose:** Stores **configuration files** for various aspects of the application, such as database connections, caching, API keys, or feature toggles.
    - **Examples:**
    - **`env/`**: The project/config/env folder is designed to house environment-specific configuration files, which help manage different setups for various environments like development, testing, staging, and production. These files typically store environment variables and settings that are specific to each deployment scenario.
        - **Examples:**
            - `development.env`: Settings for development environment.
            - `production.env`:  Settings for production environment.
            - `staging.env`: Settings for staging/pre-production environment.
            - `testing.env`: Settings for testing environment.

* * *
