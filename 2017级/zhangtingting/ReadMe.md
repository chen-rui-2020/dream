# SSM入门计划
好好努力  好好生活

## Step 1

1. 环境搭建（Java开发环境，Spring-boot开发环境，MySQL环境）。
2. 新建Web项目
3. 导入一个完整的Web项目
4. 从零开始搭建SSM项目

## Step 2

 根据Step 1实施情况后续再做调整



# Learning situation every day

2020/10/22

#### 学习内容：

学习[用idea+maven创建web项目](http://blog.csdn.net/myarrow/article/details/50824793)

#### 学习过程：

##### 一、根据这个网址先去了解了IDEA、maven是什么

> 1. IDEA 全称 IntelliJ IDEA，是java编程语言开发的集成环境。
>
> 2. Maven项目对象模型(POM)，可以通过一小段描述信息来管理项目的构建，报告和Maven项目对象模型(POM)，可以通过一小段描述信息来管理项目的构建，报告和文档的项目管理工具软件。的Maven项目对象模型(POM)，可以通过一小段描述信息来管理项目的构建，报告和文档的项目管理工具软件。软件。

我的理解就是，IDEA类似于学校学的visual studio这些软件，之前是用visual studio进行.net开发，现在是用IDEA进行java开发。并稍微了解了一些目前比较流行的java IDE (eclipse,myeclipse,IDEA). maven就是管理和构建项目框架的工具，有些类似vue-cli

##### 二、 安装IDEA

安装的过程中，官网提供了社区免费版本，以及旗舰版本。一开始下载的是社区免费版本。

下载完成后提示需要下载**SDK**，然后又先去了解了一下什么是SDK，在查询的过程中也知道了JavaEE说的是什么。

> 1. **JDK** (Java Development Kit) 是 Java 语言的软件开发工具包([SDK](https://baike.baidu.com/item/SDK))
>
> 2. **SE(JavaSE)**，standard edition，标准版，是我们通常用的一个版本，从JDK 5.0开始，改名为Java SE。
> 3. **EE(JavaEE)**，enterprise edition，企业版，使用这种JDK开发J2EE应用程序，从JDK 5.0开始，改名为Java EE。从2018年2月26日开始，J2EE改名为Jakarta EE [1] 。
>
> 4. 常用的基本工具有:
>
> * Javac：Java源程序编译器，将Java源代码转换成字节码。
> * Java： Java解释器，直接从字节码文件，又称为类文件。执行Java应用程序的字节代码。
> * appletviewer.exe Java applet浏览器：appletviewer命令可在脱离万维网浏览器环境的情况下运applet
> * jar：java应用程序打包工具，可将多个类文件合并为单个JAR归档文件。
> * Javadoc：Java API文档生成器从Java源程序代码注释中提取文档，生成API文档HTML页。
> * jdb：Java调试器(debugger),可以逐行执行程序.设置断点和检查变Md
> * jps：查看Java虚拟机进程列表 

##### 三、配置maven和tomcat

发现自己安装的版本没有tomcat server，网上查阅了一些资料知道要**下载旗舰版**，因为免费版本少了许多功能。并去网上了解了tomcat是什么。

> Tomcat 服务器是一个免费的开放源代码的Web 应用服务器，属于轻量级应用[服务器](https://baike.baidu.com/item/服务器)，在中小型系统和并发访问用户不是很多的场合下被普遍使用，是开发和调试JSP 程序的首选。

个人理解就是用来部署web项目的，类似于IIS。

##### 四、下载ultimate版本的IDEA并完成相关配置

成功创建web项目

##### 五、JAVA环境配置总结

1. 下载java jdk, 建议是1.8版本以上，并配置jdk环境变量

2.  下载tomcat，并配置tomcat环境变量

   [为什么安装Java时需要配置环境变量？](https://mp.weixin.qq.com/s?src=11&timestamp=1603360015&ver=2660&signature=f74KKcur*J1FsKv*mRIJ-cqxFqButTkCjEleQGeLgvH5kdq2LpooMO73O3hcAVu63o8y36zDKe9OidAxzr07G30snTD0iCymt1lEQ-PYErFcXoZxpKrhgCYQ4hLXlEdr&new=1)

3. 官网下载IDEA**旗舰版**，需破解。

4. 配置maven，tomcat。

   

