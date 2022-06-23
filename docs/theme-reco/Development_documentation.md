---
title: 电商
date: 2022-06-23
sidebar: 'auto'
publish: true
---



# 电商项目

## 1、流程

- **准备开发环境：数据库、redis、mq、es......（虚拟机的环境）**
- **准备maven环境**
- 8张表8个操作，（64个接口）

## 2、技术架构

1. SpringBoot：简化新Spring应用的初始搭建以及开发过程
2. SpringCloud：基于SpringBoot实现的云原生应用开发工具，SpringCloud使用的技术：（Spring Cloud Gateway、Alibaba Nacos、Spring Cloud Alibaba Sentinel、Spring Cloud Task 和 Spring Cloud Feign等）
3. MyBatis-Plus：持久层框架
4. Redis：内存缓存
5. Redisson：基于redis的java驻内存数据网络-框架
6. RabbitMQ：消息中间件
7. ElasticSearch + Kibana：全文检索服务器 + 可视化数据监控
8. ThreadPoolExecutor：线程池来实现异步操作，提供效率
9. Thymeleaf：页面模板技术
10. Swagger：Api接口文档工具
11. Fastdfs：分布式文件存储 类似于oss
12. 支付宝支付/微信支付：alipay.com
13. Mysql：关系型数据库{mycat/sharding-jdbc进行分库，分表}
14. Lombok：实体类的中get、set生成的jar包
15. ngrok：内网穿透
16. Docker：容器技术
17. Git：代码管理工具
18. DockerFile：管理Docker镜像命令文本
19. jenkins：持续集成工具
20. Vue.js：web界面的渐进式框架
21. Node.js：JavaScript运行环境
22. NPM：包管理器

## 2、技术亮点

分布式架构、缓存管理、分布式事务、单点登录、商品后台管理、文件管理系统

## 3、项目流程

### maven搭建

```properties
省略。。。。。。
```

------



### 虚拟机搭建

#### ·1、设置虚拟机中虚拟机的IP网段

![1655229816185](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1655229816185.png)

![1655229849753](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1655229849753.png)

![1655229943275](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1655229943275.png)

#### 2、设置本地虚拟机的IP

![1655230010149](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1655230010149.png)

![1655230040526](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1655230040526.png)

![1655230072314](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1655230072314.png)

#### 3、关闭防火墙

![1655230132507](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1655230132507.png)

![1655230157511](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1655230157511.png)

------



### 启动Telnet客户端

```properties
telnet命令是用来测试端口是否通畅
例如：telnet 192.168.200.128 3306 
端口号：
3306 -> mysql
6379 -> redis
9200 -> es
5672 -> RabbitMQ
```

![1655230402866](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1655230402866.png)

![1655230422023](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1655230422023.png)

![1655230445387](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1655230445387.png)

![1655230641492](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1655230641492.png)

### 虚拟机测试

#### 1、通过命令ip addr查看虚拟机IP地址

#### 2、用主机ping虚拟机

#### 3、用虚拟机ping主机

#### 4、用虚拟机ping外网，例如：www.baidu.com

​			全部通过说明环境没有问题

------



### 通过第三方软件连接虚拟机

#### xshell 或者 fianlshell 对虚拟机进行链接



### 初始工程搭建

#### 搭建gmall-parent

使用DependencyManagement固定了依赖的版本号

定义了pom代表是一个父工程



#### 搭建common父模块

是一个公共模块，所有微服务都会使用到的工具放这里面

配置 web工程

lombok、swagger、fastjson、openfeign的依赖



#### 搭建common-util模块

是一个微服务都可能使用到的公共的工具类模块

只有一个httpclient的依赖，用来发送http请求的

##### execption：

有一个自定义全局异常类

##### result：

1、result：全局统一返回结果，（给客户用的api返回Result）

2、ResultCodeEnum：枚举类，定义了状态码对应的消息的内容

##### util：

1、AuthContexHolder：做登录使用到的用来获取用户名的工具类

2、HttpClientUtil：专门用来发送http请求的工具类

3、IpUtil：IP地址工具类，用来获取用户的IP地址

4、MD5：做MD5加密的

#### 搭建service-util模块

微服务可能需要使用的功能的公共模块，例如

mysql数据库，redis，es等中间件放进来

依赖有：redis、redis连接池、redisson、mybatisplus

##### cache

###### 	-GmallCacheAspect：切面类

##### config：配置包

###### 	-MybatisPlusConfig：配置mybatis-plus框架的信息

(配置了分页插件)

###### 	-RedisConfig：配置了Redis的配置信息

(初始化redis，实现了redisTemplate的序列化和反序列化)

###### 	-RedissonConfig：配置信息

###### 	-swagger2Config：API的配置类

0

### Linux命令

```properties
docker ps: 查看容器
ip addr: 查看虚拟机IP地址

```

