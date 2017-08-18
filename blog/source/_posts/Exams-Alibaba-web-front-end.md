---
title: 阿里巴巴笔试
date: 2017-08-24 10:43:22
tags: ["Interview", "Web"]
categories: ["Interview"]
description:
lang: zh-Hans
---
昨天参加了阿里第一轮的笔试，有几个重点内容记录一下，以后多留意。另外末尾有java相关知识点

### 1.TCP HTTP2 HTML5..相关
#### 关于HTTP2
选择题 挑出错的表述，
HTTP2是二进制协议，头部更小，
HTTP/1.0只允许一个请求显眼每次一个给定的连接上。HTTP/2.0提供了在单个连接上复用HTTP请求和响应的能力。 多个请求或响应可以同时在一个连接上使用流。因此，对请求划分优先级肯定也得支持咯。
还有sever push的特性，这个我连题目都没看懂。。。

HTTP post get update delete四种请求方法。是不是一点都不违和？！！！
写网站写傻了就是你了，GET POST PUT DELETE还有HEAD OPTION
上链接[HTTP2](http://www.cnblogs.com/ghj1976/p/4552583.html)
#### 关于TCP
里面大概有TCP可以确保数据的有序
上链接[TCP](http://www.jianshu.com/p/ef892323e68f)
<!-- more -->
### 2.ECMAScript6的新特性
这个，老实说，ES6我基本没用过，ES5很多特性我都以为是JS的，233333。
事后上网查了一下，总结一下吧。
#### ES5主要内容
strict模式，
Array增加方法forEach，isArray、map、reduce..
object增加方法 Object.create Object.getOwnPropertyNames，Object.preventExtensions..

#### ES6主要内容
块级作用域 * let, const * -----这个可重要了
关于作用域貌似出现在不只一道题，倒数第二道题代码里面也有关于作用域的。可惜忘了当时截图。
大概就是var作用有点坑人 [INFOQ ES6 教程 ](http://www.infoq.com/cn/articles/es6-in-depth-let-and-const/)
js最早只有全局作用域，函数作用域两个概念，然后try catch出现又多了异常变量的，eval出现又多了个，
es6加的更多了，块作用域，for循环作用域，新的全局let作用域，模块作用域，以及求参数的默认值时使用的附加作用域。
还有一个代理命名空间的描述，老实说，看过很多次，但根本没管过。
哦，对了，有个送分选项，ES6需要Babel之类转译，浏览器不支持，当时看到好感动啊。ES6我当时就这个选项能确定

### 3.主流框架如 React的相关知识，譬如 JSX Redux
JSX代码总归得能看懂吧，Redux双向单向数据流的内容
还有最后一个大题，就是让你完整描述一个前端框架的架构，优劣，和场景。这个我也不了解，感觉不该用vue的，诶，贼气，大家如果多上知乎之类的看布道师吹逼都可以写出来吧
### 4.BFC 前端渲染流程,页面性能优化方法等相关知识
呃，这个我在draft中，小伙伴可以自行搜索。
### 5.关于，跨域，Prototype，Cookie，缓存，ajax中断，DOM，function arguments,svg小知识点
譬如ajax abort方法，prototype 的 apply和js object ，js默认返回值是undefined
最后一个我当时真的就是猜的，估计不太可能是null
### 6.另外分享下朋友给的笔试JAVA岗位的内容范围


{% blockquote%}
 Object类有哪些方法
 Yeild功能
 介绍一下Java中volatitle关键字
 项目中你用到这个关键字吗，用于哪个场景
 Volatitle关键字声明之后，编译器不会优化的原理
 Java中Session和Cookie
 Java中Synchronized，Lock的区别
 Synchronized能被中断吗
 Lock中提供了中断的方法吗，这个方法是哪个
 消费者生产者模型你是怎么实现的
 如果当前线程被锁，其它线程干嘛
 具体在哪个场景中使用这个，业务背景
 在工程中用的还是分布式管理
 hashMap是怎么管理的
 线程安全版本你用过吗
 ConcurrentHashMap用过吗，讲一下原理
 怎么执行读时被锁
 除了分段锁还有什么原理
 怎么用于分布式
 线程本地变量原理和实现原理
 线程本地变量大概有什么数据结构，怎么实现的
 介绍一下java的内存模型
 除了堆，栈，常量区还有什么
 线程本地变量存在哪的
 JVM的DDM参数你有调优过吗，设置大小和原则你能介绍一下吗
 Xss默认大小，在实际项目中你一般会设置多大
 数据库主键和外键有什么区别
 数据库视图和表有什么区别
 数据事务你能简单介绍一下吗，ACCD
 事务特性分别什么特征，什么原理
 Mysql数据库隔离级别一般用哪个
 Hibernate隔离级别一般用的哪个
 数据库大概怎么实现的索引，底层用了什么数据结构，大概介绍一下
 B 树
 分布式系统，分布式工作原理
 介绍ARP协议是干什么的
 Http请求底层是用的什么协议
 Tcp连接过程
 连接时队列大小是什么原理
 DNS协议作用，底层用的什么协议
 语法解析
 词法解析
 编译步骤分几个部分
 编译程序常用表达方法
 进程通信有哪些方式
 进程和线程有什么区别
 文件描述符是共享的还是私有的
 什么是死锁
 Java中你碰到过死锁吗
 Mysql中碰到过死锁吗
 虚拟内存是什么原理
 一页大小大概多少
 换页中最近最长未使用算法简单的实现
 除外链表相应算法你了解过吗
 堆排序大概是怎么实现的
 堆排序你使用过吗，是用的怎样的底层存储，数据结构
 底层是用的数组，逻辑上是怎样的结构
 求第五大的算法是什么原理，直接求，不用排序
 搜索算法PN你知道吗，字符串查找
 介绍一下你学过哪些搜索算法
 B 用于外排为什么效率会比较高
 B 树结点大小一般是多大
 和磁盘块大小有什么关系
 Hash算法是什么，为什么会有Hash算法
 一般采用的Hash冲突有哪些解决方案
 一次性Hash你有了解吗
 Redis的哪些常见的数据结构
 怎么保证分布式Catch出现脏数据
 Maven包冲突怎么解决
 Linux中怎么看日志中某个时间段某个网站被各个ip访问的次数
 Linux中解压命令是什么
{% endblockquote %}

各位且行且珍惜。。。上面问题都能回答上来的，基本可以有offer的
