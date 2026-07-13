---
sidebar_position: 1
---

# backup

### Overview

Backup a SQLite database to a specified output file

### Command Parameters

```bash
-d|--database=string    Required parameter,Source database file path. Example: /sf/data/test.db
-o|--output=string      Required parameter,Backup file save path. Example: /sf/data/test.db.bak
```

### Example

```bash
acli system file sqlite3 backup --database /tmp/test.db --output /tmp/test.db.bak
```

### Sample Output

```bash
(Command executed successfully, no output)
```