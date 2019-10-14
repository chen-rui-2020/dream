## Spring Boot 学习计划

### 原则
> 先确立几个原则，每天开始学习前大声读三遍！三遍！三遍！
- 莫得完美，~~完成第一~~ 做好记录
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
    - ~~跟随项目作者的教程走一篇，从0开始搭建，代码可复制/粘贴。注重开发的流程以及工具的深入了解。~~（我觉得该项目并不初学者友好）
    - 多找几个 Demo 熟悉 IDEA 各工具以及技术的使用，暂学习 [IntelliJ-IDEA-Tutorial](https://github.com/judasn/IntelliJ-IDEA-Tutorial) 里的 Demo
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
    - [x] 安装 MySql （没有仔细看 ssm-demo 的开发环境介绍，装的是 8.0 的，倒是用 IDEA 的 DB 连接工具执行了脚本，但 demo 就是跑不起来。）
        > 简要分析原因：MuSQL 5.x 和 8.0 有着飞跃的发展，jdbc 的驱动改变了，还有一些配置上的改变。pom.xml 改了依赖，数据库改了时区，建了新用户（root默认不能远程连接），还翻遍了互联网没找到解决的方法，也没能运行起来）
    - [x] 了解到项目的运行/调试是有不同的方式，可以以 JUnit 或者 Tomcat 的方式来运行
    - [x] 运行起 ssm-demo（忧愁）
        ![运行界面图](./img/run.png)
- 2019.10.14 第一阶段-第 3 日（今日总结：一事无成，大项目还是比较难跑起来的，还是走走小 DEMO 吧）
    - [x] 学会 IDEA 一个 window 显示多个项目（原因见 [注意/IDEA 相关](#idea相关)）
        > 勉强实现，不太理想，通过导入多个 module 的方法
    - [ ] 稍微深入了解一下 Github 的多人协作（主要是解决冲突等），实际体验一下
    - [ ] ~~配置项目 [EasyEE](https://github.com/service-java/summer-cli-mybatis/tree/ffa8d5532b73a98de26d29718c5c218450c50f79/__cant-run-now/EasyEE) 环境及运行（尽量流程化一点）~~
    
        真正的项目地址在 [这里](https://github.com/ushelp/EasyEE)，建议使用这个
        > 为什么需要真正的项目地址？
        >
        > 1. 可以直接用 IDEA 的 New -> Project from version control -> Git 来 **直接** 导入项目
        >   > 实际体验不佳，原因？ GitHub 仓库不一定就是该项目的根目录，可能是多项目的集合。难道是创建项目的姿势不是很对？
        > 2. 原项目是某个学习后端技术的人把 GitHub 上面的某些项目集合在一起的，文件夹层次比较深，不是很方便，而且按理来说文件较大
        （趣事：项目文件夹为 `__cant-run-now` 是不是仓库拥有者还不能跑起来这个项目 :joy: ）
- 2019.10.15 第一阶段-第 4 日
        

### 注意
##### MySQL 的安装
1. 到 [官网](https://dev.mysql.com/downloads/) 下载社区版
    > 虽然 MySQL 是开源的，但也提供企业版。下载时默认版本是 8.0 ，下载界面右侧可选其他版本
2. 安装时只需选择安装 'Server only' 即可，因为可以通过 IDEA 来管理，不需要像以前装 sqldevelper(Oracle), SSMS(SQL Server) 这些 GUI 的管理工具
    ![安装时选择设置类型](./img/installSel.png)
3. 安装时请创建一个用户，默认 root 用户是不能远程连接的，但是可以修改，关键词是 “开启远程访问”、“host” 等
    > 如果用不到远程连接可以不用新建，但是正常的项目为了安全不应该使用 root 账户。
    我的习惯：创建一个名为 dev 的账户
4. 如果在 IDEA 中测试连接数据库提示 serverTimeZone 类似错误，可以按照错误提示设置时区为 `GMT-8` (东八区)
    > 这只是途径之一，还可以 [这样](https://blog.csdn.net/cy12306/article/details/97259049) 修改, 但其实一步也能解决问题。
    原因大概在数据库默认安装的时候使用的是时区是 SYSTEM (从链接中可以看出)，而这个值是美国时区，出现了不匹配或 IDEA 不清楚 SYSTEM 的定义
5. IDEA 的 Database 操作可以看 [这里](https://github.com/judasn/IntelliJ-IDEA-Tutorial/blob/master/database-introduce.md)
    > 十分推荐上面这个 IDEA 的教程 
6. 如果之前有装其他版本的可以尝试 [这个](https://zhuanlan.zhihu.com/p/68190605) 
    > 按照里面有的就操作，没有的就不管（我是成功了，但不一定都可以 :no_mouth: ）

#### IDEA相关
1. 单 IDEA 窗口需要显示多个项目的原因（仅个人认为，暂时没找到很好的办法解决）
    - 多个 Project 之间不共享数据库连接这些，每个项目都配置一次麻烦
    - 每次切换多个 IDEA 窗口比较麻烦，单窗口的话可以在标签之间切换
2. IDEA 安装插件的实际意义就是安装对应的软件，以 Maven 举例

    由于旗舰版的 IDEA 安装时默认勾选了 Maven，所以在安装的时候就已经把 Maven 装上了，
    想要在 Windows 的终端中执行 mvn 命令的话只需要设置 PATH 即可，无需手动安装 Maven，
    一般来说，IDEA 的 Maven 安装在 `C:/Program Files/JetBrains/IntelliJ IDEA 2019.2.3/plugins/` 文件夹内
    （取决于安装时的选项，还可以在 IDEA 的 `Settings->Build, Execution, Deployment->Maven->Maven home directory` 中查看到具体的目录），
    只需要在该文件夹里找到 Maven 的 `/bin` 目录，添加到系统变量之后重启电脑使之生效即可（可以注意到这里装了 maven2 和 maven3 两个版本）
3. 