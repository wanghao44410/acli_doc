---
sidebar_position: 1
---

# list

### Overview

Query the list of iptables firewall rules, supports filtering by chain name and table name, displayed in numeric format by default

### Command Parameters

```bash
-c|--chain=string    Specify the chain name. Enumeration values: INPUT, VS_MANAGER_INPUT, VS_CLUSTER_INPUT, ANET_MEMBERS_INPUT, VTPLOG_INPUT, CLUSTER_MEMBERS_INPUT, all. Default value: all. Example: INPUT
-n|--numeric=flag    Display addresses and ports in numeric format, enabled by default
-v|--verbose=flag    Verbose mode
-t|--table=string    Specify the table name. Default value: filter. Example: filter
```

### Example

```bash
acli network nettools iptables list
```

### Sample Output

```bash
Chain INPUT (policy DROP)
target     prot opt source               destination         
TMP_RULES  all  --  0.0.0.0/0            0.0.0.0/0           
VS_TMP_RULES  all  --  0.0.0.0/0            0.0.0.0/0           
USER_INPUT_MYSQL  all  --  0.0.0.0/0            0.0.0.0/0           
ACCEPT     all  --  0.0.0.0/0            0.0.0.0/0            state RELATED,ESTABLISHED
USER_INPUT_MYSQL  tcp  --  0.0.0.0/0            0.0.0.0/0           
USER_INPUT_MYSQL  udp  --  0.0.0.0/0            0.0.0.0/0           
ACCEPT     all  --  0.0.0.0/0            0.0.0.0/0           
DROP       icmp --  0.0.0.0/0            0.0.0.0/0            icmptype 13
DROP       icmp --  0.0.0.0/0            0.0.0.0/0            icmptype 17
ACCEPT     icmp --  0.0.0.0/0            0.0.0.0/0           
ACCEPT     2    --  0.0.0.0/0            0.0.0.0/0           
NFS_INPUT  udp  --  0.0.0.0/0            0.0.0.0/0            udp dpt:2049
NFS_INPUT  tcp  --  0.0.0.0/0            0.0.0.0/0            tcp dpt:5049
ACCEPT     udp  --  10.131.128.0/20      0.0.0.0/0            udp dpt:2011
DROP       udp  --  0.0.0.0/0            0.0.0.0/0            udp dpt:2011
CLUSTER_MEMBERS_INPUT  udp  --  0.0.0.0/0            0.0.0.0/0            udp dpt:2010
SSH_INPUT  tcp  --  0.0.0.0/0            0.0.0.0/0            tcp dpt:22
SSH_INPUT  tcp  --  0.0.0.0/0            0.0.0.0/0            tcp dpt:22346
WHITELIST_INPUT  tcp  --  0.0.0.0/0            10.131.136.45        tcp dpt:80
WHITELIST_INPUT  tcp  --  0.0.0.0/0            10.131.132.168       tcp dpt:80
WHITELIST_INPUT  tcp  --  0.0.0.0/0            10.131.136.45        tcp dpt:443
WHITELIST_INPUT  tcp  --  0.0.0.0/0            10.131.132.168       tcp dpt:443
ACCEPT     tcp  --  0.0.0.0/0            0.0.0.0/0            tcp dpt:80
ACCEPT     tcp  --  0.0.0.0/0            0.0.0.0/0            tcp dpt:443
ACCEPT     tcp  --  0.0.0.0/0            0.0.0.0/0            tcp dpt:4480
USER_INPUT_SF_SDK  tcp  --  0.0.0.0/0            0.0.0.0/0            tcp dpt:4433
VDI_ACCESS_INPUT  tcp  --  0.0.0.0/0            0.0.0.0/0            tcp dpt:8888
USER_INPUT_NTP  udp  --  0.0.0.0/0            0.0.0.0/0            udp dpt:123
CLUSTER_MEMBERS_INPUT  tcp  --  0.0.0.0/0            0.0.0.0/0            tcp dpt:1984
CLUSTER_MEMBERS_INPUT  tcp  --  0.0.0.0/0            0.0.0.0/0            tcp dpt:6666
CLUSTER_MEMBERS_INPUT  tcp  --  0.0.0.0/0            0.0.0.0/0            tcp dpt:7329
CLUSTER_MEMBERS_INPUT  tcp  --  0.0.0.0/0            0.0.0.0/0            tcp dpt:15001
CLUSTER_MEMBERS_INPUT  tcp  --  0.0.0.0/0            0.0.0.0/0            tcp dpt:8001
VNC_INPUT  tcp  --  0.0.0.0/0            0.0.0.0/0            tcp dpts:14500:15000
VNC_INPUT  tcp  --  0.0.0.0/0            0.0.0.0/0            tcp dpts:14000:14499
USER_INPUT_SAMBA  tcp  --  0.0.0.0/0            0.0.0.0/0            tcp dpt:139
USER_INPUT_SAMBA  tcp  --  0.0.0.0/0            0.0.0.0/0            tcp dpt:445
DROP       udp  --  0.0.0.0/0            0.0.0.0/0            udp dpts:53:54
USER_INPUT_HOST_FOUND  udp  --  10.131.128.0/20      0.0.0.0/0            udp dpt:4099
DROP       udp  --  0.0.0.0/0            0.0.0.0/0            udp dpt:4099
```