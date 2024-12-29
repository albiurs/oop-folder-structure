# General-purpose utilities

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   └── utilities/          # General-purpose utilities
│       ├── validator.py
│       ├── date_formatter.py
│       └── logger.py
```


### **Folder Structure Explanation**

* * *

#### **`utilities/`**

- **Purpose:** Contains **reusable helper classes and functions** for common, application-wide tasks that don't belong to specific features or layers.
    - **Examples:**
        - `date_formatter.py`: Provides methods to format dates for various locales or use cases.
        - `validator.py`: Validates data inputs across the application.
        - `logger.py`: Centralized logging utility for debugging and error tracking.
        - `file_uploader.py`: Handles file uploads and storage (e.g., for user profiles or documents).
        - `json_parser.py`: Processes JSON data, ensuring it adheres to expected structures.
        - `password_hasher.py`: Provides secure password hashing and verification.
        - `api_response_helper.py`: Formats API responses in a consistent structure.
        - `math_helper.py`: Contains utility functions for mathematical operations (e.g., percentages, rounding).
        - `csv_handler.py`: Reads and writes CSV files for data import/export.
        - `string_sanitizer.py`: Cleans and sanitizes user input to prevent injection attacks.

* * *
