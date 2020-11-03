学习计划

## 一、Spring-boot

### 第一阶段

- 环境准备：Java开发环境，Spring-boot开发环境，MySQL环境
- 自己创建项目并成功运行
- 多跑几个项目，总结步骤

### 第二阶段

- 熟悉IDEA的使用

- 了解项目目录结构和配置
- 学习Maven 多模块项目，Maven打包

### 第三阶段

待更新

## 进度

- 2020/10/20
  - [x] 了解 Github 的多人协作
    - 分支的操作
    - 解决冲突

  - [x] 创建一个简单的demo并熟悉项目结构

  - [x] IDEA中的快捷键

    - 内容辅助键

    - 快捷键
    
  - [x] IDEA中的模块操作

    - 新建模块、删除模块、导入模块

  - [x] 配置环境

    - [x] Java环境

    - [x] IDEA安装

    - [x] 上传一个项目到GitHub(真的太方便了吧)

    - [x] Maven镜像配置

- 2020/10/21

  - [x] 配置MySQL环境+安装Navicat

    - [x] 在IDEA上配置好环境

  - [x] 安装Tomcat并在IDEA上配置好

  - [ ] 熟悉IDEA使用git插件

    - [x] [多人协作场景](https://blog.csdn.net/Y125348369/article/details/87907729)

  - [x] 确认springboot环境配置完毕

  - [x] 创建一个HelloSpringboot项目

  - [x] SSM入门

- 2020/10/22

  - 熟悉IDEA的使用

    - [x] 了解安装目录和设置目录

    - [x] 设置常见视图、查看ProjectStructure和设置常用的settings
    - [x] 关联数据库、导入初始化数据库文件

    - [x] 版本控制之git

      - [x] 跑起来一个[Maven的单模块SSM项目](https://github.com/judasn/IntelliJ-IDEA-TutorialMaven)

- 2020/10/23

  - 补充学习昨天跑项目疑惑的Javaweb基础

    - [x] xml

      - 复习xml概念、语法、组成部分
      - 学会在xml中引入约束文档(DTD和Schema)
      - 简单的读懂约束文档

    - [x] Tomcat

      - 目录结构
      - 启动并访问、关闭

      - 配置


      - 能看懂IDEA集成的tomcat设置了


      - 创建一个web项目
    
    - [x] Servlet：sever applet
    
      - 执行原理
      - 生命周期


- 2020/10/24

  - [x] 跑起来一个[Maven的多模块SSM项目](https://github.com/judasn/Basic-Multi-Module-SSM)

  - [ ] 跑一个Springboot项目

    - 没有跑起来，去了解了一下Springboot项目的基本设置
    
    - pom.xml
    
    - 配置类注解
    - 参数传递的方式
    - 创建Springboot项目的三种方式
    - Springboot项目的两种运行方式

- 2020/10/25

  - 学习了队友的CURD demo然后去了解了相关知识

    - 对写CURD有整体的思路
  
  - 了解了Mybatis映射文件的组成
  
  - 数据操作的注意事项
  
  - 实现接口代理的接口规范
- 2020/10/26
  - 了解了SpringMVC的开发过程和执行流程
  - 练习了SpringMVC的常用注解
  - 用postman测试CURD demo的请求出现问题，正在解决

- 2020/10/27-28

  - 学习Maven
    - 项目工程目录结构
    - 常用命令
    - 依赖范围
    - 依赖传递、解决依赖冲突
    - 继承、聚合

  - 创建单模块和多模块的Maven项目实现了简单的查询请求
  - 对比学习队友的多模块CURD demo

- 2020/10/29

  - 对比学习的感受：

    > 用Spring Boot以后，项目初始化方法变了，配置文件变了，另外就是不需要单独安装Tomcat这类容器服务器了，maven打出jar包直接跑起来就是个网站，但业务逻辑实现与业务流程实现没有变化。

  - 纠正了一个学习误区：spring和springboot的关系

    记录目前比较认可的一个说法：

    > Spring 最初利用“工厂模式”（DI）和“代理模式”（AOP）解耦应用组件。
    >
    > 大家觉得挺好用，于是按照这种模式搞了一个 MVC框架（一些用Spring 解耦的组件），用开发 web 应用（ SpringMVC ）。
    >
    > 然后发现每次开发都写很多样板代码，为了简化工作流程，于是开发出了一些“懒人整合包”（starter），这套就是 Spring Boot。

  - 了解了springboot整合SpringMVC和Mybatis
  - 学习spring
    - spring解耦的思路
    - 控制反转IOC
    - bean标签
    - spring的依赖注入
    - 基于xml和注解的IOC配置
    - 常用注解

- 2020/11/1

  - [ ] 学习SSM+easyui的项目

    - 掌握了eclipse项目导入IDEA的方法

    - 学习了SSM+easyui的CURD demo：大致了解数据操作返回的结果渲染到ui模板上的思路

    - 学习jsp：运行原理、执行过程、内置对象、域对象

    - 学习el表达式：运算、常见对象、特定域的属性、pageContext 对象

    - request对象

      ```
      获取虚拟目录：/curd
      String getContextPath()
      
      获取请求URI：/curd/demo1
      String getRequestURI():		/curd/demo1
      StringBuffer getRequestURL()  :http://localhost/curd/demo1
      
      请求转发
      request.getRequestDispatcher(String path).forward(request,response) 
      
      共享数据
      void setAttribute(String name,Object obj)
      Object getAttitude(String name)
      void removeAttribute(String name)
      ```

- 2020/11/2-3

  - [ ] 学习SSM+easyui的项目
    - 学习easyui
    - 尝试理解更复杂数据的交互

  - 学习困难：
    - 数据操作返回的结果如何转化为easyui中组件渲染所需要的格式