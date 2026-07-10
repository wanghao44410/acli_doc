---
sidebar_position: 1
---

# check

### 操作概述

检查指定端口的网络连接数，支持按连接状态过滤

### 命令参数

```bash
-p|--port=integer    必要参数，指定端口号，取值范围1-65535，示例：22
-s|--state=string    连接状态过滤，枚举值：ESTABLISHED, LISTEN, all，默认all，示例：ESTABLISHED
```

### 使用示例

```bash
acli network nettools netstat connection check --port 22
```

### 结果示例

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