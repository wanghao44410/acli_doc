---
sidebar_position: 1
---

# check

### Overview

Query processes occupying a specified file or directory

### Command Parameters

```bash
-p|--path=string    Required parameter,Specified file or directory path. Example: /sf/data/local/test.txt
```

### Example

```bash
acli system proc fuser check --path /tmp
```

### Sample Output

```bash
 120557
```