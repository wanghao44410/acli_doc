---
sidebar_position: 1
---

# check

### Overview

Check whether a specified port is in listening state, supports TCP/UDP protocols

### Command Parameters

```bash
-p|--port=integer    Required parameter,Specify the port number, range 1-65535. Example: 24007
-P|--protocol=string Protocol type. Enumeration values: tcp, udp. Default value: tcp. Example: tcp
```

### Example

```bash
acli network nettools netstat port check --port 22
```

### Sample Output

```bash
Port 22 (tcp) is LISTENING
tcp        0      0 0.0.0.0:22              0.0.0.0:*               LISTEN      21391/sshd [listene
tcp6       0      0 :::22                   :::*                    LISTEN      21391/sshd [listene
```