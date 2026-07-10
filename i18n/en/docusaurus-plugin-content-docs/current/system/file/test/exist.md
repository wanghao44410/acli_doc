---
sidebar_position: 1
---

# exist

### Overview

Check whether a specified path exists, can specify type as file, directory, or any

### Command Parameters

```bash
-p|--path=string    Required parameter,Path to check. Example: /sf/data/test
-t|--type=string    Check type. Enumeration values: file, dir, any. Default value: any. Example: file
```

### Example

```bash
acli system file test exist --path /tmp
```

### Sample Output

```bash
Path exists
```