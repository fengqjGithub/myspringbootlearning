给这个项目写个说明吧，方便以后查阅用：
1、项目起因纯属是觉得自己从来没总结过所学、所用过的东西，而且本项目学习性质居多吧，
   以前学习起来都比较零碎，这次是想总结整理一下，顺便做个笔记吧。
2、项目不定期更新，看自己什么时候想写了。

项目技术栈：
1、springboot2.0为基础，集成一些基础的常用的框架，但是这个框架的一部分实际上已在真是项目中用过了。
2、数据库：两个关系型数据库，两个NOSQL数据库：sqlserver/mysql，redis、MongoDB。
3、消息队列：一开始用了activemq，也写了个demo，后来发现网上用的阿里的rabbitmq比较多，所以改了一哈，用了rabbitmq。
4、在util包中加了一堆工具类，有自己写的，也有从网上找的，有点乱，但是相对来说还是比较全面的。

代码说明：
1、基础是springboot2.0
2、用两种关系型数据库试了一下多数据源配置，mysql和sqlserver。连接池用了阿里的druid，据说比较稳定吧。
   持久层用了spring-data-jpa和mybatis两种，分别写了demo，mybatis是现学的，感觉写配置文件写的有点不爽。
   
   PS:mybatis集成多数据源比较成功，用的切面和自定义注解，但是jpa搞了很长时间，前后加起来用了两三天吧，
   官方文档查了，网上资料找了，但是就是失败，应该是包扫描问题，但是各种尝试都不行，有点恶心，1.5的我试了一下，
   很好弄，但是2.0的，怎么搞都不行，最后jpa用的主数据源，以后有空再看吧，我得看集群和分布式了，这个先放这儿吧，以后用到了再完善。
3、NOSql用了redis和mongodb，算是缓存吧，对memcached也不了解，以后用到再看吧。一开始使用了boot本身集成的redis，
   但是boot2.0配置起来有点小问题，就是序列化方式除了string方式之外，其他的都会多个双引号。
   后来听某位大神说用Jedis比较方便也比较流行，所以又改成了Jedis，原来的redis配置没有冲突的也没删，扔那了。
   MongoDB也没啥说的，一个映射，估计没做分布式，用的都是皮毛吧。
4、mq现在没什么业务场景，等闲下来，找个业务场景实现一下可能理解更深吧。


PS：1、目前springboot只是用了一个皮毛，等把这个项目完结之后再学学进阶篇吧。
    2、当前比较流行的微服务cloud也没接触过，随后学学cloud吧。
    3、集群和分布式也都没接触，但是估计这个得对多线程了解很深吧，现在正在学多线程，
       学多线程还得学java内存模型、同步之类的东西，哎，头疼，为以后打基础吧。
    
    本框架最大缺点：基于单机版构建的，没有任何集群和分布式思想，因为老子现在不会分布式呀，没业务场景啊！！！！！！！！！！！
    后面就开始往这边靠了，路漫漫其修远。。。。。。。。
    
    
    
   对于学习，我是真没兴趣，只好坚持了，每天进步一点点！！！加油！！！