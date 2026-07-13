---
sidebar_position: 1
---

# status

### Overview

Query the running status of the SDN (Software Defined Network) service

### Command Parameters

```bash
No parameters
```

### Example

```bash
acli service anet sdn status
```

### Sample Output

```bash
app dataplane.o is dead already!
app appinitd(38557) is alive
app dataplane(42472) is alive
app networkd(42719) is alive
app monitord(42655) is alive
app cfgdbd(42684) is alive
app dhcpd(42568) is alive
app tunneld(42735) is alive
app mrouted(42495) is alive
app dnsd(42611) is alive
app locald(42526) is alive
app dhcp6d(42548) is alive
app flow_exporter(42628) is alive
```