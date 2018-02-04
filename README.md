
* [如何掌握所有的程序语言](http://www.yinwang.org/blog-cn/2017/07/06/master-pl)
  - 重视语言特性，而不是语言
  - 掌握关键语言特性，忽略次要特性
  - 自己动手实现语言特性
* [简述 OAuth 2.0 的运作流程](http://www.barretlee.com/blog/2016/01/10/oauth2-introduce/)
  - 服务商提供第三方ClientID和ClientSecret
  - 用户拿着ClientID请求服务商并授权，通过跳转链接到AuthToken传给第三方
  - 第三方用AuthToken和ClientSecret请求服务商，拿到AccessToken
  - 使用AccessToken调用服务商API，拿到用户信息及进行操作
* [假如我是计算机系老师](https://mp.weixin.qq.com/s?__biz=MzAxOTc0NzExNg==&mid=413878948&idx=1&sn=70986470ce1957e302680da0ad71f22b&scene=21#wechat_redirect)
  - 《编码：隐匿在计算机软硬件背后的语言》
  - 《深入理解计算机系统》-> 《图灵的秘密》
  - K&R 合著的《C程序设计语言》
  - Sedgewick 和 Wayne合著《算法》 -> 《算法导论》
  - 《30天自制操作系统》
  - SQLite的源码
  - 《TCP/IP详解》
  - 《编译原理》《编程语言实现模式》
* [干货 | 分布式架构系统生成全局唯一序列号的一个思路](https://mp.weixin.qq.com/s?__biz=MjM5MDI3MjA5MQ==&mid=2697266651&idx=2&sn=77a5b0d4cabcbb00fafeb6a409b93cd7&scene=21#wechat_redirect)
  - 1、利用数据库递增，全数据库唯一。
  - 2、UUID， 生成的是length=32的16进制格式的字符串
  - 3、Snowflake
  - 4、Redis生成ID
  - 5、Flicker的解决方案
* [Redis读写分离典型场景](http://www.jianshu.com/p/18041ffbdd9a?utm_source=tuicool&utm_medium=referral)
  - 利用浏览器缓存和CDN抗压静态页面流量
  - 利用主从版Redis缓存加速库存扣量
  - 消息队列异步下单入库
* [系统设计的万能解法](https://mp.weixin.qq.com/s/u8NDvKcYv4ztVVRT_HaUJw)
  - SNAKE (Scenario场景、Necessary限制、Application应用、Kilobit数据、Evolve进化)
  - 系统设计四大要素
    - 第一，是要满足一个需求即Requirements
    - 第二，对内容进行一个定义
    - 第三，从不同维度去考虑宏观的架构层、组件层、模块层
    - 第四，也要考虑到互相间交流的接口和相关传递的数据
* [彻底终结MySQL同步延迟问题](https://www.jianshu.com/p/ed19bb0e748a)
  - 网络：主从之间带宽及延迟
  - 机器性能：
    - 从机配置低：主机用SSD，从机用SATA
    - 从机高负载：在从机上做统计
    - 从机硬件问题：iostat
  - 大事务：查看processlist
  - 锁：查看processlist
  - 参数：innodb_flush_log_at_trx_commit， sync_binlog等
  - 多线程：`show variables like '%slave_parallel%'`
  - 组提交：