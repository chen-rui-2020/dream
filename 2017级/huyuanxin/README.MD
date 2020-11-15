#  Spring Boot学习计划

## 1.计划

### （1）第一阶段

* 搭建项目环境和安装IDEA  [CSDN笔记](https://blog.csdn.net/m0_51683714/article/details/109156046)
* 创建项目并成功运行  [CSDN笔记](https://blog.csdn.net/m0_51683714/article/details/109185265)
* IDEA的快捷键  无CSDN笔记
* 学习更多的模块 无CSDN笔记
* Maven打包 无CSDN笔记
* 项目分层和配置
* Mybatis的配置

* Mybatis增删改查的实现

* 写一个小demo，http的形式完成对数据库的增删改查


### （2）第二阶段

* 学习前端，将demo改为界面操作

* 写一个更多功能的项目练手
* 尝试了解Spring原理
* 待增加

## 2.进度

### 2020.10.20

#### （1）整理第一阶段的资料，并写成CSDN笔记上传[1/9]

- - [x] 搭建项目环境和安装IDEA

#### （2）与队伍成员合作解决Git冲突的解决方法。

### 2020.10.21

#### （1）整理第一阶段的资料，并写成CSDN笔记上传[2/9]

- - [x] 搭建项目环境和安装IDEA

- - [x] 创建项目并成功运行

#### （2） CURD的demo

- - [x] 已完成

### 2020.10.22

#### （1） 完善CURD的demo

- - [x] 已完成
    * * [x] 单个对象的CURD
  - [x] 上传至GitHub  [GitHub链接](https://github.com/huyuanxin1999/LearnSSM)

#### （2）学习Git冲突的解决方法。

* * [x] 学会合并分支
* * [x] 学会解决合并分支时出现冲突



### 2020.10.23

#### （1）学习用新的方式获得请求参数

* * [x] 学习@RequestParam代替HttpServletRequest

    ```java
        @RequestMapping(value = "/deleteUserByUid", method = RequestMethod.DELETE)
        public int delete(
                @RequestParam("id") int uid) {
            return userService.deleteOneByUid(uid);
        }
    
    	// 等同于
        @RequestMapping(value = "/deleteUserByUid", method = RequestMethod.DELETE)
        public int delete(HttpServletRequest request){
            int uid= Integer.parseInt(request.getParameter("id"));
            return userService.deleteOneByUid(uid);
        }
    ```

  * [x] 学习获取http发送的Json请求

    ```java
       	// RequestBody接收
    	@RequestMapping(value = "/getUserList", method = RequestMethod.GET)
        public List<User> getUserList(
                @RequestBody List<User> list) {
            return list;
        }
    ```

### 2020.10.24

#### （1）Json字段自定义

* * [x] 解决返回Json开头小写和发送接收的问题

    ```java
    //  以这个为例子返回为["Uid":value]，若没有 @JsonProperty("Uid"),则返回字段为["uid":value]
    public class User {
        private long Uid;
        
    @JsonProperty("Uid")
        public long getUid() {
            return Uid;
        }
    }
    ```

#### （2）完善CURD的demo

* * [x] 已完成
    * * [x] 单个对象的CURD
    * * [x] 完成多个对象的CURD
    * * [x] 完善代码
    * * [x] 更新至GitHub   [GitHub链接](https://github.com/huyuanxin1999/LearnSSM)

### 2020.10.25-2020.10.27

#### (1）掌握SpringBoot多模块的创建

* * [x] 掌握创建多模块
* * [x]  掌握各模块的依赖关系
* * [x] 上传快速创建项目到GitHub[GitHub链接](https://github.com/huyuanxin1999/SpringBootMultiMoudle)

#### （2）改单模块CURD为多模块

* * [x] 修改完成
* * [x] 完善
* * [x] 上传GitHub[GitHub链接](https://github.com/huyuanxin1999/SpringBootMultiMoudleDemo)

### 2020.10.27-2020.11.1

#### 这段时间踩了一堆的坑

* * [x] Spring Boot+EasyUI demo运行
* * [x] 学会thymeleaf配置静态文件
* * [x] 写一写简单的页面
* * [x] 学习了dto层
* * [x] 为原来单模块的项目加入dto层(完善后上传GitHub)

### 2020.11.2

* * [x] Spring Boot+EasyUI项目的编写

### 2020.11.3

* * [x] 解决dto格式化json后，获取出现的问题
* * [x] EasyUI DataGrid分页的问题
* * [x] 更新到GitHub [GitHub链接 LearnSSM](https://github.com/huyuanxin1999/LearnSSM)

### 2020.11.4

* * [x] 学习ajax请求
* * [x] 学习JavaScript部分语法
* * [x] EasyUI 批量生成按钮
* * [x] EasyUI DataGrid删除操作
* * [x] 更新到GitHub [GitHub链接 LearnSSM](https://github.com/huyuanxin1999/LearnSSM)

### 2020.11.5-2020.11.16

* * [x] 学习阿里Java开发规范

* * [x] 将已有代码重构为符合阿里开发规范的代码

* * [x] 上传重构后代码到GitHub

* * [x] Spring测试

    ```java
    package com.example.demo;
    
    import org.junit.jupiter.api.Test;
    import org.springframework.boot.test.context.SpringBootTest;
    
    @SpringBootTest
    class DemoApplicationTests {
    
        @Test
        void contextLoads() {
            // 测试代码
        }
    
    }
    ```

* * [x] Spring多个类测试

    ```java
    package com.example.demo;
    
    import org.junit.runner.RunWith;
    import org.junit.runners.Suite;
    
    // 这个是批量测试
    @RunWith(Suite.class)
    @Suite.SuiteClasses({
            Test1.class,
            Test2.class,
            UserMapperTest.class
            // 把要测试的写在这里
    })
    public class DemoApplicationTests {
    	// Some Code
    }
    ```

    ```java
    package com.example.demo;
    
    import com.example.demo.domain.mapper.UserMapper;
    import org.junit.Test;
    import org.junit.jupiter.api.DisplayName;
    import org.junit.runner.RunWith;
    import org.springframework.beans.factory.annotation.Autowired;
    import org.springframework.boot.test.context.SpringBootTest;
    import org.springframework.test.context.junit4.SpringRunner;
    
    @RunWith(SpringRunner.class)
    
    //不加上会无法创建bean
    @SpringBootTest 
    
    // 测试的名字
    @DisplayName("测试UserMapper")
    public class UserMapperTest{
        @Autowired
        UserMapper mapper;
    
        @Test
        @DisplayName("测试findAll接口")
        public void findAll(){
            mapper.findAll();
        }
    }
    
    ```

* * [x] 进一步学习Mybatis的写法以及@Param的作用

* * [x] 解决Mybatis全部爆红的问题

  需要添加数据源，且数据库名称要写进xml里面，如下：

  ```xml
  <?xml version="1.0" encoding="UTF-8" ?>
  <!DOCTYPE mapper PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN" "http://mybatis.org/dtd/mybatis-3-mapper.dtd" >
  <mapper namespace="com.example.demo.domain.mapper.UserMapper">
      <!--Sql串-->
      <sql id="select">
          Select * From spring.user
      </sql>
      <!--以下会报无数据库和无法查到数据库下的属性-->
       <sql id="select">
          Select * From spring.user
      </sql>
  </mapper>
  ```

  