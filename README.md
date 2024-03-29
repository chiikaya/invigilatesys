﻿# 系统程序设计课程设计后端
基于原项目做代码重构  
## 技术栈
> SpringBoot2.0 \+ MySql 5.6 \+ Lombok等  
> 接口按照标准REST风格进行设计,[参考博客](https://www.jianshu.com/p/84568e364ee8),[GitHub官方说明文档](https://developer.github.com/v3/)
## 基本功能  
* 用户注册、登录模块  
* 个人信息管理模块  
* 管理员对用户信息、监考信息、任务信息的增删改查模块  
* 用户查询监考信息、任务信息的模块等等  ## E-R图
![](./E-R图.png)  
## 项目记录
### 2019.4.10  
后端环境搭建完成，数据库创建完成  
使用BCryptPasswordEncoder对密码进行多次加密，使得明文相同密文不同   
使用Encryptors基于秘钥和盐值对用户id和操作权限进行加密得到token  
完成用户部分的拦截器，对未携带Token的访问进行拦截  
基于原生的HttpStatus状态码进行错误返回，减少资源使用  
对于非受检异常进行统一异常处理  
### 2019.4.14   
完成管理员的接口编写
### 2019.5.26
更改了实体命名规则
添加了所有功能的增删改查接口
完成管理员的接口编写  
### 2019.5.28
后端服务基本搭建完毕,接口请见[API文档](./API文档.md)
