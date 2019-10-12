## Spring Boot 学习计划

### 原则
> 先确立几个原则，每天开始学习前大声读三遍！三遍！三遍！
- 莫得完美，完成第一
- 每天结束时根据当天学习的内容调整、补充计划

### 说明
Spring Boot 包含 SSM ？？？
暂时还不能区分出 Spring Boot 和 SSM 的之间的关系，现阶段我比较认同的 Spring Boot 的定义如下
> Spring Boot 是为了让你快速搭建一个 Spring 的项目，把Spring的所有 Project 整合在一起
Spring Boot 解决的是搭建项目快慢的问题，那项目实际是怎么做的就应该不是 Spring Boot 的任务了，因此在此之前还是要学会 Java Web 的常用框架 SSM (对 Servlet + JSP 的模式有一定的了解)

[知乎-spring boot和SSM开发中有什么区别？-陈龙 回答](https://www.zhihu.com/question/284488830/answer/618290880)

### 计划
- 第一阶段：尝个甜头
    - 以能正常运行 [ZHENFENG13/ssm-demo](https://github.com/ZHENFENG13/ssm-demo) 为最终目标了解 SSM 使用到的工具（IDEA, Maven, MyBatis 等）
    - 跟随项目作者的教程走一篇，从0开始搭建，代码可复制/粘贴。注重开发的流程以及工具的深入了解。
- 第二阶段：扎实基础
    - 以 [纯洁的微笑](http://www.ityouknow.com/spring-boot.html) 的 Spring Boot 教程为主线了解 Spring Boot
- 第三阶段：实战演练
    - 将自己的项目 [通讯录](https://github.com/Tindoc/AddressBook) 重构为 SSM 架构，记录其中的问题
    - 根据问题回顾/补充第二阶段的知识

### 进度记录
- 2019.10.12 第一阶段-第 1 日
    - [x] 安装 IDEA （装了旗舰版的，还没激活，试用期用着先）
    - [x] 在 IDEA 中新建 Maven 的 Web-App 项目顺利运行显示"Hello World!"（不求理解跟着步骤走很迷）
    - [x] 修改了 IDEA 的 MAVEN 的 jar 源为阿里云的镜像，加快 build 速度（上个项目 build 了3分钟）
    - [x] 导入了项目 ssm-demo（build 加快了很多；运行失败，没装 MySql）
    - [x] 在 IDEA 设置 Github 账户（重点：File-Settings-Github, VCS）
    - [x] 使用 Github 组织成员的工作流程（以前只用过个人的工作流程）
- 2019.10.13 第一阶段-第 2 日
    - [ ] 安装 MySql
    - [ ] 运行起 ssm-demo