---
sidebar_position: 1
---

# integrity-check

### Overview

Check the integrity of a SQLite database (PRAGMA integrity_check and quick_check) 

### Command Parameters

```bash
-d|--database=string    Required parameter,Database file path. Example: /sf/data/test.db
```

### Example

```bash
acli system file sqlite3 integrity-check --database /tmp/test.db
```

### Sample Output

```bash
ok
ok
```