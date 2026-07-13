---
sidebar_position: 1
---

# check

### 操作概述

查询占用指定文件或目录的进程

### 命令参数

```bash
-p|--path=string    必要参数，指定文件或目录路径，示例：/sf/data/local/test.txt
```

### 使用示例

```bash
acli system proc fuser check --path /tmp
```

### 结果示例

```bash
 120557
```