---
maxWidth: 600
---

# redis

## 高可用

- 持久化机制
  - aof
  - rdb
- 主从复制
- 哨兵集群

## 高性能

### 线程模型
  - 其他线程：持久化、TTL淘汰、集群管理
  - API线程
    - redis < 6.0 单线程
    -  redis >=6.0 多线程
  
### 网络IO模型
  - IO多路复用
  - Reactor模型：单Reactor多IO线程

### 数据结构
- string：SDS，懒回收
- list：quicklist，双端链表，ziplist
- hash：dict字典，zipmap，渐进式hash
- szet：skiplist跳表，ziplist
- set：dict字典，整形数组
- bitmap：string
- HyperLogLog： 
- geo：zset(scope=geohash)

### 内存操作
- 直接CURD内存
- 定期+惰性淘汰减少CPU消耗，LRU优化



## 高拓展

- cluster部署 


