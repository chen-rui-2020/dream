# Spring Boot

## 计划
1. 安装好IDEA，MySQL，配置好spring boot开发环境
2. 新建web项目，跟着教程把项目跑起来。
3. 多跑几个项目，总结步骤，细化每一个步骤。
4. 学习spring boot基础
5. 学习Maven多模块项目
6. 未更


## 总结
- 2020.10.20
  - 了解github和git的使用，清楚了git上传项目的步骤
  - 对markdown的一些语法有了认识，但是还不够熟练，要多练练
  - 细心，耐心，加油！！
---

- 2020.10.21
  - 下载jdk8，配置。下载IDEA，配置Maven，基本完成java spring boot基本配置。
  - 今天转向学习用IDEA提交计划
  - 跟着创建了项目并运行，但结果好像有点不一样，不知道是不是因为Tomcat还没安装和配置的原因，网上好像说有内置的？所以到底要不要安装呢？（思考，明天再看看
    [教程]: https://blog.csdn.net/qq_40147863/article/details/84194493
---

- 2020.10.22

- 熟悉了idea多人协作场景，分支的建立与合并。

- project和module的建立与彻底删除。

- > - mybatis内部封装了JDBC（java数据库连接），不需要花费精力去加载驱动、创建连接、创建Statement等繁杂过程。
  >
  > - SpringbootApplication： 一个带有 main() 方法的类，用于启动应用程序
  >
  > - SpringbootApplicationTests：一个空的 Junit 测试了，它加载了一个使用 Spring Boot 字典配置功能的 Spring 应用程序上下文
  >
  > - application.properties：一个空的 properties 文件，可以根据需要添加配置属性
  > - pom.xml： Maven 构建说明文件
  > - 映射个URL：@RequestMapping({"",""}) 或 @RequestMapping(value={"",""}

- 解决了昨天遗留的问题：安装并配置了tomcat环境

-  完成web的创建过程

  [创建web]: https://blog.csdn.net/myarrow/article/details/50824793

- > 运行过程解决问题：

  > - 端口被占用问题，解决方法，用了换端口的方法
  > - 运行中出现无tomcat，是因为漏了在IDEA配置tomcat
  > - 打包成war及复制到webapps方法：界面右侧的maven>lifecycle>clean>package右键>run maven build
---

- 2020.10.23
  - MySQL的安装配置以及连到idea。
  - 今天主要就是导入单模块的ssm小项目，并运行起来。
  - 遇到问题
  > - 解决未与 -source 1.7 一起设置引导类路径问题，通过修改settings.xml 文件配置解决。
  > - 通过MySQL配置解决时区问题。
---

- 2020.10.24
- 再梳理一遍ssm单模块的运行过程
- 跑ssm多模块
- 跑成功了，但是感觉不甚理解！！！
---

- 2020.10.25
- - [导入该项目](https://github.com/liyifeng1994/ssm)，这个项目是eclipse的，上网找了idea导入eclipse项目方法，但是暂时还没跑成功。
- - [看了](https://blog.csdn.net/qq598535550/article/details/51703190)，也就是上述项目搭建过程，但是还没上手搭，打算先把这个项目跑起来。
---

- 2020.10.26

- > 今天一天都在一步一步跟着搭建，出现一堆问题，有些就算搜索解决了，但是也不知道原因是什么，可能性太多，是时候去看https://www.cnblogs.com/xdp-gacl/tag/JavaWeb%E5%AD%A6%E4%B9%A0%E6%80%BB%E7%BB%93/default.html?page=3
---
- 2020.10.27~28
1. 去详细了解了控制反转和依赖对象。
2. 整理了几种改端口的方法，几种tomcat虚拟目录映射方法。
3. 了解了tomcat配置虚拟主机和浏览器与服务器交互过程。
4. tomcat加密连接互联网 https://www.cnblogs.com/xdp-gacl/p/3744053.html （加密方式，生成数字证书，配置HTTPS连接器，增删CA数字证书）

---
- 2020.10.29
- 学习了mybatis一些相关内容。


