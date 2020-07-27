# salary-increment
主题 ： 分析 ConcurrentHashMap 

 ConcurrentHashMap

HashMap 是非线程安全的，在执行put时候会引起死循环，会引起CPU爆满，在并发时候不能使用HashMap 。HashTable 使用 Synchronized 保证线程安全，线程竞争激烈时效率非常低。ConcurrentHashMap 采用分段锁技术 。

1.6 版本 ， ConcurrentHashMap 是由 Segment 数据和HashEntry 结构组成。

1.8 版本 ， ConcurrentHashMap 采用Node ，Node是链表结构

