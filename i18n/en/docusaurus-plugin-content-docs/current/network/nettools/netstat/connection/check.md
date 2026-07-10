---
sidebar_position: 1
---

# check

### Overview

Check the number of network connections on a specified port, supports filtering by connection state

### Command Parameters

```bash
-p|--port=integer    Required parameter,Specify the port number, range 1-65535. Example: 22
-s|--state=string    Connection state filter. Enumeration values: ESTABLISHED, LISTEN, all. Default value: all. Example: ESTABLISHED
```

### Example

```bash
acli network nettools netstat connection check --port 22
```

### Sample Output

```bash
Port 22 connections (state=all): 7
---
tcp        0      0 0.0.0.0:22              0.0.0.0:*               LISTEN      21391/sshd [listene
tcp        0      0 10.131.132.168:22       10.131.137.2:36700      ESTABLISHED 87464/sshd: root@no
tcp        0      0 10.131.136.45:43588     10.131.136.45:22        TIME_WAIT   -               
tcp        0      0 10.131.136.45:53242     10.131.136.45:22        TIME_WAIT   -               
tcp        0      0 10.131.136.45:53274     10.131.136.45:22        TIME_WAIT   -               
tcp        0      0 10.131.136.45:43608     10.131.136.45:22        TIME_WAIT   -               
tcp6       0      0 :::22                   :::*                    LISTEN      21391/sshd [listene
```