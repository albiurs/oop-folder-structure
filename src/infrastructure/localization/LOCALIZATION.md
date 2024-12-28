# Handles locales and related logic

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── infrastructure/     # Technical details and external system interaction
│   │   ├── localization/   # Handles locales and related logic
│   │   │   ├── locale_manager.py
│   │   │   ├── locale_adapter.py
│   │   │   └── locale_parser.py
```


### **Folder Structure Explanation**

* * *

#### **`infrastructure/`**

- **Purpose:** Manages the **technical and integration details** of the application, including interaction with databases, external services, middleware, caching, and runtime guards.
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

* * *
