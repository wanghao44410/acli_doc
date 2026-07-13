---
sidebar_position: 1
---

# query

### 操作概述

执行 SQLite 数据库 SQL 查询，支持 csv、column、list 三种输出格式

### 命令参数

```bash
-d|--database=string    必要参数，数据库文件路径，示例：/sf/log/log_new.db
-s|--sql=string         必要参数，SQL语句，示例：SELECT * FROM alert LIMIT 10
-f|--format=string      输出格式，可选值：csv, column, list，默认column
```

### 使用示例

```bash
acli system file sqlite3 query --database /tmp/test.db --sql 'SELECT 1'
```

### 结果示例

```bash
1
```