---
sidebar_position: 1
---

# backup

### 操作概述

备份 SQLite 数据库到指定输出文件

### 命令参数

```bash
-d|--database=string    必要参数，源数据库文件路径，示例：/sf/data/test.db
-o|--output=string      必要参数，备份文件保存路径，示例：/sf/data/test.db.bak
```

### 使用示例

```bash
acli system file sqlite3 backup --database /tmp/test.db --output /tmp/test.db.bak
```

### 结果示例

```bash
(命令执行成功，无输出)
```