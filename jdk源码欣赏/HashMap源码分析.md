# salary-increment
主题 ： 分析 HashMap 源码

 HashMap

HashMap ， k-v 形式存储，无序的，非线程安全的 ，是对Map 接口的实现 。

1.7  版本 ， 采用

1.8 版本 ， 采用数组+链表+红黑树 。

HashMap 采用Entry 数组存储key-value 

HashMap 源码中重要的方法

- 构造方法
- 添加方法 put
- addEntry ()
- 查找方法 get()
- 删除方法 remove()
- 判断key值方法 containsKey()

HashMap 数据结构

HashMap 内部的数据结构是数组+单链表，以键值对形式存储。

横排是一个数组 table [] ，纵排是一个hash桶 bucket ，bucket里面放的是 Map.Entry 对象。

![](https://images2017.cnblogs.com/blog/1267939/201712/1267939-20171208192413515-1027907259.png)





```
public class HashMap<K,V>
    extends AbstractMap<K,V>
    implements Map<K,V>, Cloneable, Serializable
{
   // 初始化容量大小 默认 16
    static final int DEFAULT_INITIAL_CAPACITY = 16;
    // 最大容量大小
    static final int MAXIMUM_CAPACITY = 1 << 30;
    // 负载因子 默认值 0.75 负载因子越小，hash冲突机率越低
    static final int MAXIMUM_CAPACITY = 1 << 30;
    // 初始化一个空数组
    static final Entry<?,?>[] EMPTY_TABLE = {};
    // 将初始化好的空数组赋值给table，table数组是HashMap实际存储数据的地方，并不在EMPTY_TABLE数组中
    ransient Entry<K,V>[] table = (Entry<K,V>[]) EMPTY_TABLE;
    // HashMap 中实际存储的元素个数
    transient int size;
    //  临界值（HashMap 实际能存储的大小）,公式为(threshold = capacity * loadFactor)
    int threshold;
    // 负载因子 , 为 60 元素申请100个存储空间，60/100 = 0.6
    final float loadFactor;
    // HashMap的结构被修改的次数，用于迭代器
    transient int modCount
    
}
```







