---
sidebar_position: 1
---

# get

### 操作概述

获取到指定目的地址的路由信息

### 命令参数

```bash
-d|--dest=string    必要参数，目的地址，示例：1.1.1.1
```

### 使用示例

```bash
acli network ip route get --dest 10.131.136.1
```

### 结果示例

```bash
10.131.136.1 dev eth0  src 10.131.136.45 
    cache
```