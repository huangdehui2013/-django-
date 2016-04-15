# -django-
python进阶学习---> django框架解析 --->领悟编程语言共性与特性
1.python语言介绍
  python解释型脚本语言
2.python执行原理
  python解释器执行python字节码
3.python basic基础语法
  
4.python高级进阶 网络框架
  迭代器
  装饰器
  单例
  垃圾回收机制
  twisted网络通信
  
5.python django frameword 应用之一web框架-django学习
  
6.django advanced learning 高级进阶
7.python web framework and wsgi web框架 与wsgi关系
  Webserver<--->Wsgi>--->Application
  
8.python web application deploy 部署
  nginx+django+uwsgi+supervisord
9.python web server  内置webserver uwsgi gunicorn tornado
  uwsgi
  gunicorn
  tornado
10 探讨不同语言 python php java golang 以及框架共性与特性
  解释性语言: python php 每次执行需重新编译
       python 由python解释器（cpython C语言实现）执行字节码文件.pyc；对象常驻内存，支持多线程 多进程；
       PHP语言是一种解释型的脚本语言，这种运行机制使得每个PHP页面被解释执行后，所有的相关资源都会被回收。PHP在语言级别上没有办法让对象常驻内存；不支持多线程
  编译性语言: java golang 编译后执行
  
  语言框架的共性：大部分采用mvc模式开发
     1.框架封装的Request Response对象
       Request请求对象对http请求内容的封装：请求行【协议版本号 querystring】 请求头【cookie数据 client信息】 请求体【post put delete数据】等
       Response ：响应对象包含 响应行 响应头 响应体
     2.Route机制
       依据请求资源定位uri 定位执行的controller
     3.缓存机制
       a1.基于内存缓存  注意：当清除更新缓存时多进程会存在问题，gunicorn；生产环境推荐采用分布式缓存 a3  a4  a5
       a2.基于文件缓存
       a3.基于memcache缓存
       a4.基于redis缓存
       a5.自定义缓存，比如基于mongodb存储缓存数据
     4.session管理
       创建session表，表结构{sessionid data ctime expire}； web框架中session的添加 删除 更新机制和时机；redis mysql 可存储session
     5.模板引擎
       a1 模板语法 a2模板解释器
     6.静态资源管理
       1.资源存储本地磁盘
       2.上传第三方存储服务
     7.ORM
       
     8.middleware中间件或者拦截器
       过滤 校验
     9.Auth认证机制
       基于rbac实现一套认证机制
     10.国际化机制
     11.框架工具
       json序列化与反序列化
       时间格式
       字符串处理
       html xml
       。。。
    12.python拓展
       scrapy爬虫框架--》源码分析-->自定义分布式网络爬虫
       ansible saltstack 自动化运维工具
       pyqt UI客户端
       。。。
  
  
