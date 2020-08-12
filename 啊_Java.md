## 一、基础

1. **集合**

   - SET  

     无序；不重复

   - LIST

     有序；可重复

     ​        ArrayList

     ​		LinkedList

   - MAP

     无序；键不可重复，值可重复

     ​		HashMap

     ​		HashTable

     ​		ConcurrentHashMap

2. **线程池**

   - ThreadPoolExecutor、Cache、Fix、Single、Scheduled
   - 核心线程数，最大线程数，线程存活时间，任务队列，任务拒绝策略
   - 任务 ----> 核心线程数 ----> 任务队列 ----> 最大线程数 ----> 拒绝策略
   - 拒绝策略 :   直接拒绝不抛异常   直接拒绝抛异常      丢弃队头任务再提交     返回给提交任务线程

3. **锁**

   - 乐观锁

     ​       CAS，比较替换，ABA--加版本号

   - 悲观锁

     ​      操作加锁

   - Synchronized

     无锁 ----> 偏向锁 ----> 轻量级锁 ----> 重量级锁；

     JVM，可重入锁；

     锁方法，锁类：acc_synchronized 

     锁对象:  monitorenter和monitorexit

   - Lock

     可以实现公平锁和非公平锁，有可重入锁和非可重入锁

     API，需要 lock() 和 unlock() 方法配合 try/finally 语句块来完成
     
     AQS：voletile 维护一个线程可见的变量和线程队列
     
     高级功能：
     
     **① 等待可中断；② 可实现公平锁；③ 可实现选择性通知（锁可以绑定多个条件）**

4. IO/NIO

   ​       AIO：异步非阻塞IO

   ​	   BIO：同步阻塞IO

   ​       NIO：同步非阻塞IO，channel Buffer Selector ，select poll epoll 

5. **虚拟机**

 ## 二、框架 

1. **Spring** 

    - AOP  IOC

    - bean 三级缓存 解决循环依赖

      [一文轻松搞懂 Spring 中 bean 的作用域与生命周期](https://mp.weixin.qq.com/s?__biz=Mzg2OTA0Njk0OA==&mid=2247484865&idx=2&sn=178c6e64e6c12172e77efdd669eb86a7&source=41#wechat_redirect)

    - 事务传播行为（为了解决业务层方法之间互相调用的事务问题）：
      当事务方法被另一个事务方法调用时，必须指定事务应该如何传播。例如：方法可能继续在现有事务中运行，也可能开启一个新事务，并在自己的事务中运行。在 TransactionDefinition 定义中包括了如下几个表示传播行为的常量：

      **支持当前事务的情况：**

      - TransactionDefinition.PROPAGATION_REQUIRED： 如果当前存在事务，则加入该事务；如果当前没有事务，则创建一个新的事务。
      - TransactionDefinition.PROPAGATION_SUPPORTS： 如果当前存在事务，则加入该事务；如果当前没有事务，则以非事务的方式继续运行。
      - TransactionDefinition.PROPAGATION_MANDATORY： 如果当前存在事务，则加入该事务；如果当前没有事务，则抛出异常。（mandatory：强制性）

      **不支持当前事务的情况：**

      - TransactionDefinition.PROPAGATION_REQUIRES_NEW： 创建一个新的事务，如果当前存在事务，则把当前事务挂起。
      - TransactionDefinition.PROPAGATION_NOT_SUPPORTED： 以非事务方式运行，如果当前存在事务，则把当前事务挂起。
      - TransactionDefinition.PROPAGATION_NEVER： 以非事务方式运行，如果当前存在事务，则抛出异常。

      **其他情况：**

      - TransactionDefinition.PROPAGATION_NESTED： 如果当前存在事务，则创建一个事务作为当前事务的嵌套事务来运行；如果当前没有事务，则该取值等

    - 隔离级别

      TransactionDefinition 接口中定义了五个表示隔离级别的常量：

      - **TransactionDefinition.ISOLATION_DEFAULT:** 使用后端数据库默认的隔离级别，Mysql 默认采用的 REPEATABLE_READ 隔离级别 Oracle 默认采用的 READ_COMMITTED 隔离级别.
      - **TransactionDefinition.ISOLATION_READ_UNCOMMITTED:** 最低的隔离级别，允许读取尚未提交的数据变更，可能会导致脏读、幻读或不可重复读
      - **TransactionDefinition.ISOLATION_READ_COMMITTED:** 允许读取并发事务已经提交的数据，可以阻止脏读，但是幻读或不可重复读仍有可能发生
      - **TransactionDefinition.ISOLATION_REPEATABLE_READ:** 对同一字段的多次读取结果都是一致的，除非数据是被本身事务自己所修改，可以阻止脏读和不可重复读，但幻读仍有可能发生。
      - **TransactionDefinition.ISOLATION_SERIALIZABLE:** 最高的隔离级别，完全服从 ACID 的隔离级别。所有的事务依次逐个执行，这样事务之间就完全不可能产生干扰，也就是说，该级别可以防止脏读、不可重复读以及幻读。但是这将严重影响程序的性能。通常情况下也不会用到该级别。

2. **Mybatis**

   动态代理模式 责任链

   ​     架构设计：

   ![](http://dl.iteye.com/upload/attachment/0065/2605/6a59d52b-db76-3737-b164-f366bb2fbce7.png)

   ![](https://img-blog.csdn.net/20180624002302854?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3UwMTQ3NDUwNjk=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

3. **Sping Boot**

4. **Spring Cloud**

5. **dubbo**

## 三、缓存(Redis)

## 四、消息队列

![](https://tva1.sinaimg.cn/large/006y8mN6ly1g93o256nqtj30mq0puwih.jpg)

##五、数据库(Mysql)

   开发规范：

1. 避免数据类型的隐式转换
2. 充分利用索引，避免索引失效
3. 程序连接不同数据库时使用不同的账号，禁止跨库查询
4. 禁止使用select *，指定列名查询
5. 禁止使用不含字段列表的insert语句
   6. 避免使用子查询，将子查询优化为join操作(子查询结果集不使用索引)
7. 避免使用join关联太多表
8. 减少数据库交互次数



 MyISAM和InnoDB的区别

1. MyIssAM使用表级锁；InnoDb使用行级锁和表级锁

2. MyIssAM不支持事务；InnoDB支持事务

3. MylssAM不支持崩溃回复；InnoDB支持崩溃回复

4. MylssAM不支持外键；InnoDB支持外键

   

事务的四大特性：

   1. 原子性（Atomicity）
        事务是一个不可分割的工作单位，事务中的操作要么都发生，要么都不发生。
    2. 一致性（Consistency）
        事务前后数据的完整性必须保持一致。
        - 事务开始和结束时，外部数据一致
        - 在整个事务过程中，操作是连续的
    3. 隔离性（Isolation）
        多个用户并发访问数据库时，一个用户的事务不能被其它用户的事物所干扰，多个并发事务之间的数据要相互隔离。
    4. 持久性（Durability）
        一个事务一旦被提交，它对数据库中的数据改变就是永久性的。



 隔离级别：

- 读未提交

- 读已提交

- 可重复读(default)

- 串行化

MVVC实现读未提交和可重复度，

- Record Lock : 单个记录行锁
- Gap Lock ：间隙锁，不包含记录本身
- next-key lock ：锁定一个范围，包含记录本身



索引：

- 主键索引

  数据表的主键列使用的就是主键索引。

  一张数据表有只能有一个主键，并且主键不能为null，不能重复。

  在mysql的InnoDB的表中，当没有显示的指定表的主键时，InnoDB会自动先检查表中是否有唯一索引的字段，如果有，则选择该字段为默认的主键，否则InnoDB将会自动创建一个6Byte的自增主键。

- 二级索引

  二级索引又称为辅助索引，是因为二级索引的叶子节点存储的数据是主键。也就是说，通过二级索引，可以定位主键的位置。

  唯一索引，普通索引，前缀索引等索引属于二级索引。

1. **唯一索引(Unique Key)** ：唯一索引也是一种约束。**唯一索引的属性列不能出现重复的数据，但是允许数据为NULL，一张表允许创建多个唯一索引。**建立唯一索引的目的大部分时候都是为了该属性列的数据的唯一性，而不是为了查询效率。
2. **普通索引(Index)** ：**普通索引的唯一作用就是为了快速查询数据，一张表允许创建多个普通索引，并允许数据重复和NULL。**
3. **前缀索引(Prefix)** ：前缀索引只适用于字符串类型的数据。前缀索引是对文本的前几个字符创建索引，相比普通索引建立的数据更小，
   因为只取前几个字符。
4. **全文索引(Full Text)** ：全文索引主要是为了检索大文本数据中的关键字的信息，是目前搜索引擎数据库使用的一种技术。Mysql5.6之前只有MYISAM引擎支持全文索引，5.6之后InnoDB也支持了全文索引。 

- 索引创建注意点
  1. 不为null的字段
  2. 被频繁查询的字段
  3. 被作为条件查询的字段
  4. 被经常用于连接的字段
  5. 尽可能创建联合索引
  6. 避免冗余索引和重复索引
     - 重复索引示例：primary key(id)、index(id)、unique index(id)
     - 冗余索引示例：index(a,b,c)、index(a,b)、index(a)
  7. 单张表上的索引不超过5个



​    基本架构(8.0之后没有查询缓存)

​		![](https://user-gold-cdn.xitu.io/2019/3/23/169a8bc60a083849?w=950&h=1062&f=jpeg&s=38189)



最开始 MySQL 并没与 InnoDB 引擎( InnoDB 引擎是其他公司以插件形式插入 MySQL 的) ，MySQL 自带的引擎是 MyISAM，但是我们知道 redo log 是 InnoDB 引擎特有的，其他存储引擎都没有，这就导致会没有 crash-safe 的能力(crash-safe 的能力即使数据库发生异常重启，之前提交的记录都不会丢失)，binlog 日志只能用来归档。

并不是说只用一个日志模块不可以，只是 InnoDB 引擎就是通过 redo log 来支持事务的。那么，又会有同学问，我用两个日志模块，但是不要这么复杂行不行，为什么 redo log 要引入 prepare 预提交状态？这里我们用反证法来说明下为什么要这么做？

* **先写 redo log 直接提交，然后写 binlog**，假设写完 redo log 后，机器挂了，binlog 日志没有被写入，那么机器重启后，这台机器会通过 redo log 恢复数据，但是这个时候 bingog 并没有记录该数据，后续进行机器备份的时候，就会丢失这一条数据，同时主从同步也会丢失这一条数据。
* **先写 binlog，然后写 redo log**，假设写完了 binlog，机器异常重启了，由于没有 redo log，本机是无法恢复这一条记录的，但是 binlog 又有记录，那么和上面同样的道理，就会产生数据不一致的情况。

如果采用 redo log 两阶段提交的方式就不一样了，写完 binglog 后，然后再提交 redo log 就会防止出现上述的问题，从而保证了数据的一致性。那么问题来了，有没有一个极端的情况呢？假设 redo log 处于预提交状态，binglog 也已经写完了，这个时候发生了异常重启会怎么样呢？
这个就要依赖于 MySQL 的处理机制了，MySQL 的处理过程如下：

* 判断 redo log 是否完整，如果判断是完整的，就立即提交。
* 如果 redo log 只是预提交但不是 commit 状态，这个时候就会去判断 binlog 是否完整，如果完整就提交 redo log, 不完整就回滚事务。

这样就解决了数据一致性的问题。



## 六、设计模式

- 工厂模式
- 单例模式
- 代理模
- 装饰器模式
- 模版方法模式
- 适配器模式



## 七、网络

- Nginx

  - **正向代理：**某些情况下，代理我们用户去访问服务器，需要用户手动的设置代理服务器的 ip 和端口号。正向代理比较常见的一个例子就是 VPN 了。
  - **反向代理：** 是用来代理服务器的，代理我们要访问的目标服务器。代理服务器接受请求，然后将请求转发给内部网络的服务器，并将从服务器上得到的结果返回给客户端，此时代理服务器对外就表现为一个服务器。

  ![正向代理](http://my-blog-to-use.oss-cn-beijing.aliyuncs.com/18-11-15/60925795.jpg)

![反向代理](http://my-blog-to-use.oss-cn-beijing.aliyuncs.com/18-11-15/62563930.jpg)



Nginx 有以下 5 个优点：

1. 高并发、高性能（这是其他 web 服务器不具有的）
2. 可扩展性好（模块化设计，第三方插件生态圈丰富）
3. 高可靠性（可以在服务器行持续不间断的运行数年）
4. 热部署（这个功能对于 Nginx 来说特别重要，热部署指可以在不停止 Nginx 服务的情况下升级 Nginx）
5. BSD 许可证（意味着我们可以将源代码下载下来进行修改然后使用自己的版本）



Nginx 的四个主要组成部分

- Nginx 二进制可执行文件：由各模块源码编译出一个文件

- nginx.conf 配置文件：控制 Nginx 行为
- acess.log 访问日志： 记录每一条 HTTP 请求信息
- error.log 错误日志：定位问题