---
sidebar_position: 1
---

# status

### 操作概述

查询 VTP 集群的整体状态

### 命令参数

```bash
-q|--quiet=flag    安静模式
```

### 使用示例

```bash
acli system vtpclustat status
```

### 结果示例

```bash
Cluster Status:

Member Name		ID		Status		IP
host-0050568e0c7e	1452149886	Online, Local	10.131.136.45
host-0050568eaffa	1452191738	Offline		

Cluster Stable:	Yes
```