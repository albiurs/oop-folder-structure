# General-purpose utilities

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── utilities/          # General-purpose utilities
│   │   ├── DateFormatter.php
│   │   ├── Logger.php
│   │   └── Validator.php
```


### **Folder Structure Explanation**

* * *

#### **`utilities/`**

- **Purpose:** Contains **reusable helper classes and functions** for common, application-wide tasks that don't belong to specific features or layers.
    - **Examples:**
        - `DateFormatter.php`: Provides methods to format dates for various locales or use cases.
        - `Validator.php`: Validates data inputs across the application.
        - `Logger.php`: Centralized logging utility for debugging and error tracking.
        - `FileUploader.php`: Handles file uploads and storage (e.g., for user profiles or documents).
        - `JsonParser.php`: Processes JSON data, ensuring it adheres to expected structures.
        - `PasswordHasher.php`: Provides secure password hashing and verification.
        - `ApiResponseHelper.php`: Formats API responses in a consistent structure.
        - `MathHelper.php`: Contains utility functions for mathematical operations (e.g., percentages, rounding).
        - `CsvHandler.php`: Reads and writes CSV files for data import/export.
        - `StringSanitizer.php`: Cleans and sanitizes user input to prevent injection attacks.

* * *
