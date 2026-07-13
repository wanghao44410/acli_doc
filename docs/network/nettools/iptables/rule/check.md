---
sidebar_position: 1
---

# check

### 操作概述

检查 iptables 指定链上是否存在符合条件的规则，支持按协议、端口、目标动作过滤

### 命令参数

```bash
-c|--chain=string    必要参数，指定链名，枚举值：INPUT, VS_MANAGER_INPUT, VS_CLUSTER_INPUT, ANET_MEMBERS_INPUT, VTPLOG_INPUT, CLUSTER_MEMBERS_INPUT，示例：INPUT
-P|--protocol=string 协议类型，枚举值：tcp, udp, icmp, all，示例：tcp
-p|--port=integer    端口号，取值范围1-65535，示例：22
-t|--target=string   目标动作，枚举值：ACCEPT, DROP, REJECT，示例：ACCEPT
```

### 使用示例

```bash
acli network nettools iptables rule check --chain INPUT --target ACCEPT
```

### 结果示例

```bash
ACCEPT     all  --  0.0.0.0/0            0.0.0.0/0            state RELATED,ESTABLISHED
ACCEPT     all  --  0.0.0.0/0            0.0.0.0/0           
ACCEPT     icmp --  0.0.0.0/0            0.0.0.0/0           
ACCEPT     2    --  0.0.0.0/0            0.0.0.0/0           
ACCEPT     udp  --  10.131.128.0/20      0.0.0.0/0            udp dpt:2011
ACCEPT     tcp  --  0.0.0.0/0            0.0.0.0/0            tcp dpt:80
ACCEPT     tcp  --  0.0.0.0/0            0.0.0.0/0            tcp dpt:443
ACCEPT     tcp  --  0.0.0.0/0            0.0.0.0/0            tcp dpt:4480
CLUSTER_ACCEPT_INPUT  tcp  --  0.0.0.0/0            0.0.0.0/0            tcp dpts:12182:12183
ACCEPT     udp  --  0.0.0.0/0            0.0.0.0/0
```