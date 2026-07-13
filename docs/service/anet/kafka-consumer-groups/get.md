---
sidebar_position: 1
---

# get

### 操作概述

查询 Kafka 消费者组的详细信息，包括 topic、partition、offset、lag 等

### 命令参数

```bash
-b|--bootstrap-server=string    Kafka服务地址，示例：anet-master:22012
-a|--all-groups=flag            查询所有消费者组
-t|--timeout=integer            超时时间（毫秒），示例：30000
-c|--command-config=string      配置文件路径，示例：/sf/cfg/vn/kafka/client-ssl.properties
```

### 使用示例

```bash
acli service anet kafka-consumer-groups get --bootstrap-server anet-master:22012 --all-groups
```

### 结果示例

```bash

GROUP                                TOPIC           PARTITION  CURRENT-OFFSET  LOG-END-OFFSET  LAG             CONSUMER-ID                                  HOST            CLIENT-ID
00000000-0000-0000-0000-0050568e0c7e ccp-lcp-22      0          1315            1315            0               rdkafka-d0fa3035-368b-41b1-8742-8f9333096787 /10.131.136.45  rdkafka
00000000-0000-0000-0000-0050568e0c7e ccp-lcp-22      1          -               0               -               rdkafka-d0fa3035-368b-41b1-8742-8f9333096787 /10.131.136.45  rdkafka
00000000-0000-0000-0000-0050568e0c7e ccp-lcp-22      2          -               0               -               rdkafka-d0fa3035-368b-41b1-8742-8f9333096787 /10.131.136.45  rdkafka

GROUP                                TOPIC           PARTITION  CURRENT-OFFSET  LOG-END-OFFSET  LAG             CONSUMER-ID     HOST            CLIENT-ID
00000000-0000-0000-0000-0050568eaffa ccp-lcp-5       0          1291            1315            24              -               -               -

GROUP           TOPIC           PARTITION  CURRENT-OFFSET  LOG-END-OFFSET  LAG             CONSUMER-ID                                                               HOST            CLIENT-ID
ccp             mp-ccp          1          4498            4498            0               cb504ed5-7751-48ee-92f1-fae053b0f2b3-d56927ff-c108-496a-9a4d-7f36ebe7d1b5 /10.131.136.45  consumer-ccp-cb504ed5-7751-48ee-92f1-fae053b0f2b3
ccp             mp-ccp-fullsync 0          129             129             0               cb504ed5-7751-48ee-92f1-fae053b0f2b3-d56927ff-c108-496a-9a4d-7f36ebe7d1b5 /10.131.136.45  consumer-ccp-cb504ed5-7751-48ee-92f1-fae053b0f2b3
ccp             mp-ccp-fullsync 2          -               0               -               cb504ed5-7751-48ee-92f1-fae053b0f2b3-d56927ff-c108-496a-9a4d-7f36ebe7d1b5 /10.131.136.45  consumer-ccp-cb504ed5-7751-48ee-92f1-fae053b0f2b3
ccp             mp-ccp          2          387             387             0               cb504ed5-7751-48ee-92f1-fae053b0f2b3-d56927ff-c108-496a-9a4d-7f36ebe7d1b5 /10.131.136.45  consumer-ccp-cb504ed5-7751-48ee-92f1-fae053b0f2b3
ccp             mp-ccp          0          21672           21672           0               cb504ed5-7751-48ee-92f1-fae053b0f2b3-d56927ff-c108-496a-9a4d-7f36ebe7d1b5 /10.131.136.45  consumer-ccp-cb504ed5-7751-48ee-92f1-fae053b0f2b3
ccp             mp-ccp-fullsync 1          -               0               -               cb504ed5-7751-48ee-92f1-fae053b0f2b3-d56927ff-c108-496a-9a4d-7f36ebe7d1b5 /10.131.136.45  consumer-ccp-cb504ed5-7751-48ee-92f1-fae053b0f2b3
```