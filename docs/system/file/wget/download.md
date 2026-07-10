---
sidebar_position: 1
---

# download

### 操作概述

从指定 URL 下载文件，支持超时设置、SSL 跳过、输出到文件或 stdout

### 命令参数

```bash
-u|--url=string                     必要参数，下载的URL地址，示例：http://127.0.0.1/api
-o|--output=string                  保存的本地文件路径，示例：/tmp/result.json
-O|--output-to-stdout=flag          输出到stdout
-t|--timeout=integer                超时时间（秒），示例：60
--no-check-certificate=flag         不检查SSL证书
```

### 使用示例

```bash
acli system file wget download --url http://127.0.0.1/test
```

### 结果示例

```bash
(命令执行成功，无输出)
```