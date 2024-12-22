# Runtime checks for access or rules

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── infrastructure/     # Technical details and external system interaction
│   │   ├── guards/         # Runtime checks for access or rules
│   │   │   ├── AdminGuard.php
│   │   │   └── AgeVerificationGuard.php
```


### **Folder Structure Explanation**

* * *

#### **`infrastructure/`**

- **Purpose:** Manages technical implementation details and external system interactions.
    - **`guards/`**: Encapsulates access control or runtime checks.
        - Examples:
            - `AdminGuard.php`: Ensures only admins can access certain resources.
            - `AgeVerificationGuard.php`: Verifies if a user meets a minimum age requirement.
            - `FeatureFlagGuard.php`: Restricts access based on feature flags.

* * *
