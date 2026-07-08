---
sidebar_position: 1
---

# set

### Overview

Set the value of /cfs/disable_admin.conf to control the disabled status of the platform admin user

### Command Parameters

```bash
-v|--value=integer                  Required parameter,Whether to disable admin. Enumeration values: 1 (disable), 0 (enable)

```

### Usage Example

```bash
acli platform cfs admin status set -v 1
```

### Output Example

```bash
Set the value of /cfs/disable_admin.conf successfully
```
