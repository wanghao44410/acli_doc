---
sidebar_position: 1
---

# list

### Overview

List network connections and port listening status, supports filtering by TCP/UDP, listening, numeric format, and process

### Command Parameters

```bash
-t|--tcp=flag        Show TCP connections only
-u|--udp=flag        Show UDP connections
-a|--all=flag        Show all connections
-n|--numeric=flag    Display in numeric format
-p|--program=flag    Show process PID and name
-l|--listening=flag  Show only listening sockets
```

### Example

```bash
acli network nettools netstat list
```

### Sample Output

```bash
Active Internet connections (w/o servers)
Proto Recv-Q Send-Q Local Address           Foreign Address         State      
tcp        0      0 host-0050568e0c7e:6379  host-0050568e0c7e:42510 ESTABLISHED
tcp        0      0 localhost.local:3080    localhost.local:52942   TIME_WAIT  
tcp        0      0 host-0050568e0c7e:46252 host-0050568e0c7e:25020 TIME_WAIT  
tcp        0      0 localhost.local:85      localhost.local:35480   TIME_WAIT  
tcp        0      0 localhost.local:41220   localhost.local:15001   TIME_WAIT  
tcp        0      0 localhost.local:57808   localhost.local:3080    TIME_WAIT  
tcp        0      0 localhost.local:3080    localhost.local:52856   TIME_WAIT  
tcp        0      0 host-0050568e0c7e:37400 host-0050568e0c7e:13306 ESTABLISHED
tcp        0      0 localhost.local:nfs     localhost.local:34482   ESTABLISHED
tcp        0      0 localhost.local:23031   localhost.local:41078   CLOSE_WAIT 
tcp        0      0 localhost.local:58642   localhost.local:sgi-cad ESTABLISHED
tcp        0      0 host-0050568e0c7e:39170 host-0050568e0c7e:8787  ESTABLISHED
tcp        0      0 localhost.local:85      localhost.local:59330   TIME_WAIT  
tcp        0      0 host-0050568e0c7e:48226 host-0050568e0c7e:22010 ESTABLISHED
tcp        0      0 host-0050568e0c7e:42510 host-0050568e0c7e:6379  ESTABLISHED
tcp        0      0 host-0050568e0c7e:50342 host-0050568e0c7e:25020 TIME_WAIT  
tcp        0      0 host-0050568e0c7e:50178 host-0050568e0c7e:25020 TIME_WAIT  
tcp        0      0 localhost.local:51966   localhost.local:25020   TIME_WAIT  
tcp        0      0 host-0050568e0c7e:40688 host-0050568e0c7e:12188 TIME_WAIT  
```