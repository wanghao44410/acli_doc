---
sidebar_position: 1
---

# exist

### 操作概述

检查指定路径是否存在，可指定类型为文件、目录或任意

### 命令参数

```bash
-p|--path=string    必要参数，待检测的路径，示例：/sf/data/test
-t|--type=string    检测类型，枚举值：file(检测文件), dir(检测目录), any(检测存在即可，默认)，示例：file
```

### 使用示例

```bash
acli system file test exist --path /tmp
```

### 结果示例

```bash
路径存在
```