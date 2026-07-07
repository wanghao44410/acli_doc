---
sidebar_position: 1
---

# set

### 操作概述

设置/cfs/disable_admin.conf的值，用于控制平台admin用户的禁用状态

### 命令参数

```bash
-v|--value=integer                  必要参数，是否禁用admin，枚举值：1（禁用），0（启用）

```

### 使用示例

```bash
acli platform cfs admin status set -v 1
```

### 结果示例

```bash
设置/cfs/disable_admin.conf的值成功
```
