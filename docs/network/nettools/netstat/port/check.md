---
sidebar_position: 1
---

# check

### 操作概述

检查指定端口是否处于监听状态，支持 TCP/UDP 协议

### 命令参数

```bash
-p|--port=integer    必要参数，指定端口号，取值范围1-65535，示例：24007
-P|--protocol=string 协议类型，枚举值：tcp, udp，默认tcp，示例：tcp
```

### 使用示例

```bash
acli network nettools netstat port check --port 22
```

### 结果示例

```bash
Port 22 (tcp) is LISTENING
tcp        0      0 0.0.0.0:22              0.0.0.0:*               LISTEN      21391/sshd [listene
tcp6       0      0 :::22                   :::*                    LISTEN      21391/sshd [listene
```