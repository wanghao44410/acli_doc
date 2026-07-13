---
sidebar_position: 1
---

# query

### Overview

Execute a SQLite database SQL query, supports three output formats: csv, column, list

### Command Parameters

```bash
-d|--database=string    Required parameter,Database file path. Example: /sf/log/log_new.db
-s|--sql=string         Required parameter,SQL statement. Example: SELECT * FROM alert LIMIT 10
-f|--format=string      Output format. Optional values: csv, column, list. Default: column
```

### Example

```bash
acli system file sqlite3 query --database /tmp/test.db --sql 'SELECT 1'
```

### Sample Output

```bash
1
```