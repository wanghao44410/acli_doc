---
sidebar_position: 1
---

# download

### Overview

Download a file from a specified URL, supports timeout setting, SSL skip, output to file or stdout

### Command Parameters

```bash
-u|--url=string                     Required parameter,URL to download. Example: http://127.0.0.1/api
-o|--output=string                  Local file save path. Example: /tmp/result.json
-O|--output-to-stdout=flag          Output to stdout
-t|--timeout=integer                Timeout in seconds. Example: 60
--no-check-certificate=flag         Do not check SSL certificates
```

### Example

```bash
acli system file wget download --url http://127.0.0.1/test
```

### Sample Output

```bash
(Command executed successfully, no output)
```