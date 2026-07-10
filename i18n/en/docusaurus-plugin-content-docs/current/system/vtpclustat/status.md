---
sidebar_position: 1
---

# status

### Overview

Query the overall status of the VTP cluster

### Command Parameters

```bash
-q|--quiet=flag    Quiet mode
```

### Example

```bash
acli system vtpclustat status
```

### Sample Output

```bash
Cluster Status:

Member Name		ID		Status		IP
host-0050568e0c7e	1452149886	Online, Local	10.131.136.45
host-0050568eaffa	1452191738	Offline		

Cluster Stable:	Yes
```