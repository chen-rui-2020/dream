# Spring Boot项目开发

你只管努力 其它的交给天意

## Step 1 初步了解SpringBoot

（了解springboot是什么，代码如何实现）

1. 环境搭建（下载安装Java开发工具）。
2. 新建Web项目
3. 导入一个完整的Web项目
4. 从零开始搭建SSM项目

## Step 2 开始学习SSM的核心部分

（Spring Boot项目开发代码实现使用spring+springMVC+mybatis等）

1. 学习Spring 概述，了解Spring核心机制及在项目中的应用
2. 了解SpingMVC它在项目开发中充当什么角色发挥什么作用
3. Mybatis的增删改查

## Step3 深入学习SSM





# 每日学习记录



# 2020/10/22

## 学习内容：

- [x] 学习[用idea+maven创建web项目](http://blog.csdn.net/myarrow/article/details/50824793)


## 学习过程：

### 一、根据这个网址先去了解了IDEA、maven是什么

> 1. IDEA 全称 IntelliJ IDEA，是java编程语言开发的集成环境。
>
> 2. Maven项目对象模型(POM)，可以通过一小段描述信息来管理项目的构建，报告和文档的项目管理工具软件。

我的理解就是，IDEA类似于学校学的visual studio这些软件，之前是用visual studio进行.net开发，现在是用IDEA进行java开发。并稍微了解了一些目前比较流行的java IDE (eclipse,myeclipse,IDEA). maven就是管理和构建项目框架的工具，相当于.net中的nuget，是一个**包管理工具**。

### 二、 安装IDEA

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

### 三、配置maven和tomcat

发现自己安装的版本没有tomcat server，网上查阅了一些资料知道要**下载旗舰版**，因为免费版本少了许多功能。并去网上了解了tomcat是什么。

> Tomcat 服务器是一个免费的开放源代码的Web 应用服务器，属于轻量级应用[服务器](https://baike.baidu.com/item/服务器)，在中小型系统和并发访问用户不是很多的场合下被普遍使用，是开发和调试JSP 程序的首选。

个人理解就是用来部署web项目的，类似于IIS。

### 四、下载ultimate版本的IDEA并完成相关配置

成功创建web项目

### 五、JAVA环境配置总结

1. 下载java jdk, 建议是1.8版本以上，并配置jdk环境变量

2.  下载tomcat，并配置tomcat环境变量

   [为什么安装Java时需要配置环境变量？](https://mp.weixin.qq.com/s?src=11&timestamp=1603360015&ver=2660&signature=f74KKcur*J1FsKv*mRIJ-cqxFqButTkCjEleQGeLgvH5kdq2LpooMO73O3hcAVu63o8y36zDKe9OidAxzr07G30snTD0iCymt1lEQ-PYErFcXoZxpKrhgCYQ4hLXlEdr&new=1)

3. 官网下载IDEA**旗舰版**，需破解。

4. 配置maven，tomcat。

   

------

# 2020/10/23

## 学习内容：

- [x] 学习[用maven创建第一个spring boot web 程序](https://www.cnblogs.com/jiekzou/p/9202247.html)

## 学习过程：

### 一、先去网上简要了解了一下什么是spring boot，spring，mybatis

> 1. Spring Boot是由Pivotal团队提供的全新框架，其设计目的是用来**简化新Spring应用的初始搭建以及开发**过程。该框架使用了特定的方式来进行配置，从而使开发人员不再需要定义样板化的配置。另外SpringBoot通过集成大量的框架使得依赖包的版本冲突，以及引用的不稳定性等问题得到了很好的解决。
>
>    SpringBoot所具备的特征有：
>
>    * 可以创建独立的Spring应用程序，并且基于其Maven或Gradle插件
>    * **内嵌Tomcat**或Jetty等Servlet容器
>    * 提供自动配置的“starter”项目对象模型（POMS）以简化Maven配置
>    * 尽可能自动配置Spring容器
>    * 提供准备好的特性，如指标、健康检查和外部化配置
>    * 绝对没有代码生成，不需要XML配置。 
>
> 2. Spring框架是Java平台上的一种开源应用框架
>
>    * Spring框架具有控制反转（IOC）特性，IOC旨在方便项目维护和测试
>
>    * Spring框架利用容器管理对象的生命周期,开发者可以通过依赖查找或依赖注入来获得对象。
>    * Spring框架具有面向切面编程（AOP）框架,AOP框架主要针对模块之间的交叉关注点进行模块化
>
> 3. MyBatis 是一款优秀的持久层框架，它支持定制化 SQL、存储过程以及高级映射。

我的理解是，Spring Boot项目开发代码的实现依然是使用spring+springMVC+mybatis等，只是利用了spring boot启动程序和自动配置简化Spring应用的初始搭建以及开发过程，提高开发效率。对spring框架的理解有待进一步加深，目前的简要理解就是有些像vue项目的通过下载依赖，配置依赖，然后再代码中通过import关键字引用，在代码中就可以使用依赖中的对象。关于MyBatis目前不理解它是怎么在项目中使用的。

- [ ] 遗留问题：Mybatis在项目中的应用

### 二、创建spring boot web 框架

> File->New Project->Spring Initializr->不联网下载，使用maven创建->web->创建成功。

------



# 2020/10/24

## 学习内容：

- [ ] 导入EasyEE项目

## 学习过程：

- [x] 安装MySQL5.7

- [x] 安装 `Maven local artifact install/` 下的 Maven 本地库

- [x] 创建数据库

  执行相应 SQL 脚本 `database\DATABASE_easyee_LANGUAGE[_COUNTRY].sql`

  - MySQL

    ```
    mysql> source MySQL_easyee_LANGUAGE[_COUNTRY].sql
    ```

  ------

  

# 2020/10/25

## 学习内容：

- [ ] 导入EasyEE项目

## 学习过程：

- [x] 编辑 JDBC 数据库连接配置参数

  * Spring Boot: `src/main/resources/application.properties`

    ![image-20201025231321116](F:\git仓库\2020.10.24\dream\2017级\zhangtingting\img\image-20201025231321116.png)

- [ ] 启动

  - Spring Boot: `mvn compile spring-boot:run`

    导入出了一些问题，正在解决。



# 2020/10/26

## 学习内容：

- [ ] 导入EasyEE项目

## 学习过程：

- [ ] 启动

  - 找出错原因

    ![image-20201026204019077](F:\git仓库\2020.10.25\dream\2017级\zhangtingting\img\image-20201026204019077.png)

  ​       

- [x] 了解了[jar包和war包的区别](https://www.cnblogs.com/wenzheshen/articles/6307696.html)

- [x] SringBoot的简化部署

  导入SpringBoot的maven插件，可以把应用打成jar包，直接使用java -jar命令运行

- [x] 学习Spring常见注解类

  **@RequestMapping**

  > ```
  > @RequestMapping是Spring Web应用中最常见的注解之一，它主要将Http的请求映射到我们的控制器和处理方法上。
  > ```

  **@RestController**注解，相当于**@Controller+@ResponseBody**两个注解的结合，返回json数据不需要在方法前面加@ResponseBody注解了，但使用@RestController这个注解，就不能返回jsp,html页面，视图解析器无法解析jsp,html页面

  

# 2020/10/27

## 学习内容：

- [ ] 导入EasyEE项目

## 学习过程：

- [x] 与研发小队成员一起讨论解决**:Error:(55,71)java:程序包 com.ckfinder connector不存在**的方法

  ![image-20201026204019077](F:\git仓库\2020.10.25\dream\2017级\zhangtingting\img\image-20201026204019077.png)

  ​       

- [x] 了解项目每个目录的作用

  > | 文件名            |                             作用                             |
  > | ----------------- | :----------------------------------------------------------: |
  > | src               |                  根目录，下面有main和test。                  |
  > | - main            |           主要目录，可以放java代码和一些资源文件。           |
  > | - - java          | 存放我们的java代码，这个文件夹要使用Build Path -> Use as Source Folder，这样看包结构会方便很多，新建的包就相当于在这里新建文件夹咯。 |
  > | - - resources     |    存放资源文件，譬如各种的spring，mybatis，log配置文件。    |
  > | - - - mapper      |   存放dao中每个方法对应的sql，在这里配置，无需写daoImpl。    |
  > | - - - spring      | 这里当然是存放spring相关的配置文件，有dao service web三层。  |
  > | - - - sql         |       其实这个可以没有，但是为了项目完整性还是加上吧。       |
  > | - - - webapp      | 这个貌似是最熟悉的目录了，用来存放我们前端的静态资源，如jsp js css。 |
  > | - - - - resources |      这里的资源是指项目的静态资源，如js css images等。       |
  > | - - - - WEB-INF   | 很重要的一个目录，外部浏览器无法访问，只有内部才能访问，可以把jsp放在这里，另外就是web.xml了。部署时候基本上只有webapp里的会直接输出到根目录，其他都会放入WEB-INF里面，项目内部依然可以使用classpath:XXX来访问 |
  > | - test            |                       这里是测试分支。                       |
  > | - - java          | 测试java代码，应遵循包名相同的原则，这个文件夹同样要使用Build Path -> Use as Source Folder，这样看包结构会方便很多。 |
  > | - - resources     |                很少用到，但这个是maven的规范                 |

  

# 2020/10/28

## 学习内容：

- [ ] Spring

## 学习收获：

- [x] Spring的核心容器，可以认为IOC

  1.Beans:产生Bean，某个对象

  2.Core：核心

  3.Content：上下文

  4.SpEL：Spring表达式语言

- [x] webjars：以jar包的方式引入静态资源

- [x] alter+insert：有参无参构造，getter and setter /直接引入

- [x] @ConfigurationProperties（prefix=“ ”）作用

  通过把yml配置文件中配置的每个属性的值，映射到这个组件（Bean）中，一一对应

  只有通过@Componant注解，将Bean注册为Spring容器中的组件以后，才能使用Spring提供的@ConfigurationProperties功能
  
  

# 2020/10/29

## 学习内容：

- [x] Spring的核心机制Bean和依赖注入

## 学习收获：

- [x] 理解了什么是Bean以及Spring容器如何通过Bean来创建对象

- [x] Bean的作用域以及创建时机

- [x] 理解了什么是Bean的依赖注入，以及常见的两种依赖注入的方法

- [x] 学习了Spring通过组件扫描注解的方式创建java对象以及依赖注入，以及注解如何使用

  

# 2020/10/30

## 学习内容：

- [x] Spring配置数据源

## 学习收获：

- [x] 明白了druid，C3P0，DBCP,BoneCP是什么

- [x] 如何通过Spring配置文件配置数据源连接信息，实现代码解耦

- [x] 如何在Spring配置文件中加载外部的.properties文件。

- [x] 明白了"${}"即Spring的SpEL

  

# 2020/10/31

## 学习内容：

- [x] Spring新注解和集成Junit

## 学习收获：

- [x] 知道了什么是全注解类，@configuration指定当前类是Spring的核心配置类，当创建容器时会从该类上加 吧 载注解

  （用全注解类代替XML文件，用注解代替标签）

  @componentscan用于指定Spring容器在初始化容器时要扫描的包，扫描哪些包有注解，然后创建对象

  @Bean使用在**方法**上，将该方法的返回值存储到Spring容器中（针对**非自定义**的Bean的配置）

  （@component用于实例化**自定义**的类，）

  @PropertySource加载.properties文件中的配置

  @import 导入其它配置类

- [x] Spring集成junit步骤

  1. 导入spring集成junit的坐标 （spring-test）
  
  2. 使用@runwith注解替换原来的运行期
  
  3. 使用@contextconfiguration指定配置文件或配置类

  4. 使用@autowired注入需要测试的对象
  
  5. 创建测试方法进行测试
  
     

# 2020/11/1

## 学习内容：

- [x] Spring jdbc template基本使用
- [x] Spring集成web环境
- [x] Spring MVC入门

## 学习收获：

- [x]  会使用jdbc template对象进行数据库的CRUD
- [x] 会使用Spring提供的WebApplicationContextUtils获取应用上下文对象。
- [x] Spring MVC开发步骤:
  1. 导入 SpringMVC相关坐标
  2. 配罩SpringMVC核心控制器 DispathcerServlet
  3. 创建 Controllers类和视图页面
  4. 使用注解配置 Controller类中业务方法的映射地址
  5. 配置 SpringMVC核心文件 spring-mvc.xml
  6. 客户端发起请求测试

## 学习困难：

servlet的知识不了解

------



# 2020/11/2

## 学习内容：

- [x] servlet简要学习
- [ ] Spring  MVC数据响应-页面跳转

## 学习收获：

- [x] 知道了servlet在web项目中的作用

- [x] 通过学习servlet接口实现类的开发步骤了解到了抽象类的作用、子类实现接口的规则、this指向和继承规则

- [x] 通过学习servlet后再学习spring MVC知道Spring MVC在web项目中起到什么作用

  

------

# 2020/11/3

## 学习内容：

- [x] Spring  MVC数据响应-回写数据
- [ ] Spring MVC获得请求数据

## 学习收获：

- [x] 通过配置MappingHandlerAdapter，SpringMVC自动将对象转换成json格式的数据返回
- [x] 通过`<mvc：annotation-driven`>注解驱动替代MappingHandlerAdapte的配置。
- [x] 理解@responsebody这个注解的作用
- [x] 明白了SpringMVC如何将获得的POJO参数类型封装成实体（参数名和属性名一致，将参数值进行注入）   

------



# 2020/11/4

## 学习内容：

- [x] Spring  MVC拦截器
- [x] Spring AOP

## 学习收获

- [x] 明白Spring MVC拦截器的作用 
- [x] 拦截器链执行顺序
- [x] 了解了动态代理的思想和作用

------



# 2020/11/5

## 学习内容：

- [x] xml和注解方式实现aop入门

- [x] Mybatis快速入门

## 学习收获

- [x] 知道了什么是切点（拦截的方法或者说需要进行增强的方法），什么是通知（拦截到切点以后对它进行的增强操作，有前置增强后置增强等），什么是切面（切点+通知）
- [x] My Batis开发步骤:

> 1. 添加 My Batis的坐标
> 2. 创建user数据表
> 3. 编写Use实体类
> 4. 写映射文件 UserMapper.xml
> 5. 编写核心文件 SqlMapConfig xml
> 6. 编写测试类

- [x] 通过编写mybatis的增删改查体会到了Mybatis框架比原生的jdbc的优势（sql语句的解耦以及能直接将查询的结果映射为java对象，不需要手动封装到实体中。）
- [x] mybatis默认事务不提交，需要显示的提交事务



# 2020/11/8

## 学习内容：

- [x] Spring的事务控制

## 学习收获

- [x] 通过编写基于xml的Spring事务控制，了解了Spring声明式事务控制底层就是AOP

# 2020/11/10

## 学习内容：

- [x] ssm整合

## 学习过程

- [x] 原始整合方式环境搭建
- [x] 原始整合方式mybatis配置文件内容填充

# 2020/11/12

## 学习内容：

- [x] ssm整合

## 学习过程

- [x] 原始整合方式spring和mvc配置文件内容填充
- [x] 原始整合方式web.xml配置文件内容填充
- [x] 逻辑代码编写
- [x] 测试







