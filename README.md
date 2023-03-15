# 缓存实现方案对比

**主流缓存方案：**

+ 本地缓存

  + 成员变量/局部变量/静态变量
  + **Guava Cache**
  + **Caffeine**

+ 分布式缓存

  + **Redis**

    > Redis 是一个开源的，基于内存存储亦可持久化的 Key-Value 存储系统，可用作数据库、高速缓存、锁和消息队列。它支持字符串、哈希表、列表、集合、有序集合、位图、HyperLogLogs 等数据类型。内置复制、Lua 脚本、老化逐出、事务以及不同级别磁盘持久化功能，同时，Redis还支持Sentinel和Cluster(从3.0开始)等高可用集群方案。

  + **Ehcache**

    既可以作为本地缓存也可以作为分布式缓存。

    特性：

    + 支持多级缓存（堆内缓存[heap]、堆外缓存[off-heap]、磁盘缓存[disk]、集群缓存[cluster]）

  + **Memcached**
  + Tair

**评判指标：**

或者说选型指标

+ 读/写速度

+ 内存占用（管理、回收机制）

  + 存储介质
  + 内存管理机制
  + 数据持久化机制
  + 数据淘汰策略

+ 是否支持分布式存储和共享

+ 可靠性与可用性

  + 高可用方案

  > 可用性：服务可以正常服务时间与总时间的占比；
  >
  > 可靠性：服务可以持续无故障运行的时间长度。

+ 易用性（接口与功能方面）



## 参考

+ Java标准缓存API规范：[JSR-107 (JCache)](https://github.com/jsr107/jsr107spec)