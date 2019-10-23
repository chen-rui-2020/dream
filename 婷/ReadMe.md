# Spring Boot Study-Plan
Fighting!

### 计划 
1. 安装好IDEA,MySQL,配置好环境。初步了解IDEA。
2. 跟着教程导入项目，运行起来。
3. 多跑几个项目，总结步骤，细化每一个步骤。
4. 扎实基础，学习Spring Boot 
5. 学习Maven 多模块项目。
6. https://accp.site/categories/%E7%BC%96%E7%A8%8B/Java/SpringBoot/ 学习Spring Boot基础
---

## 进度
---
#### The first day(10.12)
1. 注册并学会使用GitHub，了解markdown语法。
2. 下载安装配置IntelliJ IDEA

---
#### The second day(10.13)
- [x] 学习markdown语法
- [x] maven本地配置，配置镜像加速maven加载速度。
- [x] 安装tomcat，配置环境变量，IDEA配置tomcat
- [x] 在IDEA创建简单Web项目并运行。
- [x] 学习GitHub协同合作，Fork后进行自己的修改，pull request进行更新和提交自己的修改到源项目，参与项目和让项目得到更好的发展。
- [ ] 学习比较齐全的IDEA介绍，包括新建项目等。 https://github.com/judasn/IntelliJ-IDEA-Tutorial
- [ ] 导入了项目 ssm-demo,还没有跑起来。

---
#### The third day(10.14)
- [x] 安装MySQL
- [x] 学习IDEA介绍：基础设置（包括UI界面），索引和编译方式，了解但未背诵快捷键
- [x] Maven单模块 Spring MVC + Spring + Mybatis 的demo尝试
> 数据库连接
> 数据库初始化
> 单元测试出错，未解决问题 

---
#### The fourth day(10.15)
- [x] 运行起<https://github.com/ZHENFENG13/ssm-demo>的ssm_maven项目
![ssm_maven](https://github.com/Yths0814/picture/blob/master/images/ssm_maven.png)
````
今天运行 ssm_maven 时以 tomcat build 项目，一开始一直不成功，
后来是因为项目得配置要求Tomcat7.0，而我的IDEA用的时Tomcat9.0，
后来重新配了一下就运行起来了。版本得出错也要注意。
````
---
#### The fifth day(10.16)
- [X] 上课间隙看了一些 spring boot 的基本概念知识。了解项目目录结构，主要是java,resources和test

- [X] 《SpringBoot学习目录》<http://blog.csdn.net/xuforeverlove/article/details/89635888> 详细基础，容易入门。

````
IDEA跑项目我的步骤：
> 导入项目
> maven(w我是手动配置)
> Database, new 一个schema, 然后给自己的数据库命名
> 运行数据库脚本，记得勾选上一步新建的数据库命，把表建在自己新建的数据库里
> 测试，会出错
> 以tomcat build 项目，web项目会自动弹出页面
````
---
#### The sixth day(10.17)
- [x] <https://github.com/judasn/Basic-Single-Module-SSM> 运行起 Maven单模块 Spring MVC + Spring + Mybatis 项目
![Basic-Single-Module-SSM](https://github.com/Yths0814/picture/blob/master/images/Basic-Single-Module-SSM.png)
 
  解决之前单元测试不通过问题，是因为MySQL版本问题。
- [x] 项目设置：JDK设置；Facet 加入 Spring（还不是很理解）
- [x] 代码相关
> 简单了解pom.xml文件
> 用InteliJ IDEA 的 Database 初始化数据库
> 单元测试（数据库版本问题导致第三天单元测试不通过，更改后成功连接数据库，单元测试通过）
> 启动 Tomcat 加上 Make Project 事件
> 访问 Controller 了解 Debug
> 静态资源映射，比如做图片上传等，如没有映射好可能遇到404
- [ ] MyBatis插件的使用

---
#### 10.21
- [x] 添加Banner文件
- [x] 创建Controller类，不同的注解方式

   ````
   1. @RestController:处理http请求：等同于@Controller +  @ResponseBody
   2. @RequestMapping:value = “访问的路由”method = 请求方法
   3. @GetMapping:以GET方式请求 相当于对@RequestMapping配置的缩写
   ````
- [x] URL的其他形式
     1.  窄化请求：类和方法都有value (http://localhost:8080/user/hello)
       ![](https://github.com/Yths0814/picture/blob/master/images/url.png)
     2. 配置多url对1映射 http://localhost:8080/hello 或 http://localhost:8080/hi
     
- [x] 其他项目创建方式
    1. > SPRING INITIALIZR：通过IDEA或者STS工具创建INITIALIZR项目
    
    2. >创建Maven项目手动添加依赖
        ````
        <parent>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-parent</artifactId>
            <version>1.5.9.RELEASE</version>
        </parent>
        <dependencies>
            <dependency>
                <groupId>org.springframework.boot</groupId>
                <artifactId>spring-boot-starter-web</artifactId>
            </dependency>
        </dependencies>
        ````
     3. >通过https://start.spring.io/  生成定制项目
 
- [x] 运行方式
    * 在IDEA中直接运行
    * 发布jar包运行
        ````
        <!-- 这个插件，可以将应用打包成一个可执行的jar包；-->
           <build>
               <plugins>
                   <plugin>
                       <groupId>org.springframework.boot</groupId>
                       <artifactId>spring-boot-maven-plugin</artifactId>
                   </plugin>
               </plugins>
           </build>
        ````
        导入这个maven插件，利用idea打包，生成的jar包，可以使用java -jar xxx.jar启动
        
        Spring Boot 使用嵌入式的Tomcat无需再配置Tomcat
- [ ] Basic-Multi-Module-SSM项目运行成功，简单了解多模块项目构建方式。
---
#### 10.22
- [x] 参数传递
    ````
    1、get方式Url传参
    @PathVariable  http://localhost:8080/hello/Yt
    @RequestParam  http://localhost:8080/hello?name=Yt
    @RequestParam+默认参数 @RequestParam(value = "name",defaultValue = "admin")
    @RequestParam(value = "name",required=false)非必须参数

    ````
    
    ````
    2、post方式传递数据
    ````
 ---
#### 10.23
- [x] Getter and Setter方法太方便了，快捷键alt+insert
- [x] 学习配置文件：application.properties 和 application.yml
- [x] YMAL语法：基本语法和值的写法
- [x] 配置文件值注入
   1.  配置文件处理器
   
         ![](https://github.com/Yths0814/picture/blob/master/images/%E9%85%8D%E7%BD%AE%E6%96%87%E4%BB%B6%E7%BB%91%E5%AE%9A.png)
    
   2.  @Value获取值和@ConfigurationPropeties获取值比较
    ````
    注：properties配置文件在IDEA中默认utf-8可能会乱码
    ````


    

      
