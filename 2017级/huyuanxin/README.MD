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