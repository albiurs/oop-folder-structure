# Asynchronous or background tasks

## Folder Structure

```
project/
│
├── src/                    # Source code
│   │
│   ├── jobs/               # Asynchronous or background tasks
│   │   ├── DataCleanupJob.php
│   │   ├── GenerateReportJob.php
│   │   └── SendEmailJob.php
```


### **Folder Structure Explanation**

* * *

#### **`jobs/`**

- **Purpose:** Encapsulates asynchronous tasks executed in the background.
    - **Examples:**
        - `SendEmailJob.php`: Sends email notifications in the background.
        - `GenerateReportJob.php`: Creates reports without blocking main processes.
        - `DataCleanupJob.php`: Removes obsolete data periodically.

* * *
