Java集合：
HashMap实现原理？
concurrentHashMap实现原理？

Java高级特性：
synchronized 和 lock的区别？





##2019-12-06 星期五 敦煌网

1. redis怎么解决高并发,从线程角度说

2. 原子类 atomic(考察乐观锁 悲观锁)

3. 分布式锁实现

4. mysql数据库 包括b树 索引 sql优化 innodb和myisam的区别

5. 多线程、线程池

6. 锁升级顺序 无锁->轻量级锁->偏斜锁->重量级锁

7. http协议详情



##2019-12-12 星期四 阿里巴巴电话面试

1. redis缓存穿透 解决方案

   - web服务器校验参数

   - syno 双重锁同步校验

   - 规范key的命名，将可能出现的key全部进行缓存，值为null 注意设置过期时间

2. 各个mq的对比 优缺点

   - kafka支持消费完信息后保存信息，可以将信息持久化，速度快，吞吐量高

3. concurrenthashmap 怎么加的锁

   - 分段锁，锁住代码块

4. rpc框架 dubbo？？

 

5. jvm垃圾收集器

6. cpu占用率过高

 -top命令查看出错进程

 -jdump打印SC日志找到出问题的线程，具体到代码块

7. list各个实现的区别

 -arraylist 查找快，增删慢

-linkedlist 增删快，查找慢，移动指针

到千万级别以上时 arraylist 增删会比linkedlist快



##2019-12-14 慧聪网

1. kafka消息失败怎么办

2. 内存屏障



##2019-12-16 长城信息

1. 线程池实现

2. 线程池拒绝策略

3. gc回收算法

4. jvm内存结构



## 2019-12-23 千里马招标网

1. 线程池拒绝策略

2. springboot注解

3. innod heqmy 区别 哪个效率高

4. atomic

5. jvm内存结构

6. union和union all

7. 索引

8. age=25索引失效不失效

9. start跟run的区别



## 2019-12-27 滴滴出行

1. aop底层原理

2. sql索引

3. 前端跨域，浏览器同源策略

4. set list区别
5. 多线程计算1 + 2 + 3 + 4 +5 +......+n





##2020-01-08 搜狐

1. kafka零拷贝 nio

2. io多路复用好好了解一遍

3. 全排列算法

4. 哨兵机制为什么是单节点



