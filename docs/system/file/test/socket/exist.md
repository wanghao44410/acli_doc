---
sidebar_position: 1
---

# exist

### 操作概述

检查指定 Unix socket 是否存在

### 命令参数

```bash
-p|--path=string    必要参数，socket路径，示例：/var/run/docker.sock
```

### 使用示例

```bash
acli system file test socket exist --path /tmp/nonexistent.sock
```

### 结果示例

```bash
Unix socket不存在
```