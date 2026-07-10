---
sidebar_position: 1
---

# integrity-check

### 操作概述

检查 SQLite 数据库的完整性（PRAGMA integrity_check 和 quick_check）

### 命令参数

```bash
-d|--database=string    必要参数，数据库文件路径，示例：/sf/data/test.db
```

### 使用示例

```bash
acli system file sqlite3 integrity-check --database /tmp/test.db
```

### 结果示例

```bash
ok
ok
```