---
sidebar_position: 1
---

# get

### Overview

Get routing information to the specified destination address

### Command Parameters

```bash
-d|--dest=string    Required parameter,Destination address. Example: 1.1.1.1
```

### Example

```bash
acli network ip route get --dest 10.131.136.1
```

### Sample Output

```bash
10.131.136.1 dev eth0  src 10.131.136.45 
    cache
```