---
sidebar_position: 1
---

# exist

### Overview

Check whether a specified Unix socket exists

### Command Parameters

```bash
-p|--path=string    Required parameter,Socket path. Example: /var/run/docker.sock
```

### Example

```bash
acli system file test socket exist --path /tmp/nonexistent.sock
```

### Sample Output

```bash
Unix socket does not exist
```