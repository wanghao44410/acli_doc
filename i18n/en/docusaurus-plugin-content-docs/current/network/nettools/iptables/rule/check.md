---
sidebar_position: 1
---

# check

### Overview

Check whether the specified iptables rule exists on a chain, supports filtering by protocol, port, and target action

### Command Parameters

```bash
-c|--chain=string    Required parameter,Specify the chain name. Enumeration values: INPUT, VS_MANAGER_INPUT, VS_CLUSTER_INPUT, ANET_MEMBERS_INPUT, VTPLOG_INPUT, CLUSTER_MEMBERS_INPUT. Example: INPUT
-P|--protocol=string Protocol type. Enumeration values: tcp, udp, icmp, all. Example: tcp
-p|--port=integer    Port number, range 1-65535. Example: 22
-t|--target=string   Target action. Enumeration values: ACCEPT, DROP, REJECT. Example: ACCEPT
```

### Example

```bash
acli network nettools iptables rule check --chain INPUT --target ACCEPT
```

### Sample Output

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