date: 2020-9-2 09:34:45

## 简介

前端采用Vue、Element UI

后端采用Spring Boot、Spring Security、Redis & Jwt

高效率开发，使用代码生成器可以一键生成前后端代码

## 接口文档

[http://ip:port/swagger-ui.html](http://ip:port/swagger-ui.html)

## 模块组成

1、**`ruoyi-admin`** 后台服务模块，后台控制的Controller在这里

2、**`ruoyi-common`** 工具类模块，包含公用的工具类和类库

3、**`ruoyi-framework`** 框架核心模块，包括config系统配置、过滤器

4、**`ruoyi-generator`** 代码生成器模块，对代码生成内容格式的控制

5、**`ruoyi-quartz`** 定时任务模块，作业调度的地方，定时执行任务

6、**`ruoyi-system`** 系统代码模块，包含系统Controller所用到的业务和实体


## 主要扩展

* `flyway` 数据库版本控制

* `mybatis-plus` 数据库插件

## 快速开始

1、idea 克隆项目

```bash
https://github.com/liuxs123/ruoyi-vue-gl.git
```

2、配置项目maven地址 (可省略)

```E:\Maven\apache-maven-3.6.3\你的maven地址```
![](http://m.qpic.cn/psc?/V12PDn0m3Qk5yx/ruAMsa53pVQWN7FLK88i5hh2614R5R5xUltXu3Oy8*zM*qj64mOsT.X1h3aMUEwoDJp5CUue8YTWiojqcsmwH7nfgnfx*uVEuqMyhd8pyXs!/mnull&bo=7QKlAO0CpQADCSw!&rf=photolist&t=5)
3、创建数据库名 `修改对应yml文件`，数据库版本 5.7
![](http://m.qpic.cn/psc?/V12PDn0m3Qk5yx/ruAMsa53pVQWN7FLK88i5myG8lToRA0rLBdKfoRQjR2HkJMDdzJEytxadn7vbVX*TZDEO2kgp3d95f.9ruQjFvOcTCjPG32PysakLLxvE1o!/mnull&bo=bAMnAQAAAAADB2s!&rf=photolist&t=5)

4、运行后端项目（如果没有成功，则需要修改pom文件如下）
```xml
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>
    <parent>
        <groupId>com.ruoyi</groupId>
        <artifactId>ruoyi-vue-gl</artifactId>
        <version>3.1.0</version>
    </parent>

    <artifactId>liuxs</artifactId>

    <groupId>com.ruoyi</groupId>
    <version>1.0.0</version>

    <properties>
        <ruoyi.version>3.1.0</ruoyi.version>
    </properties>

    <dependencies>
        <dependency>
            <groupId>com.ruoyi</groupId>
            <artifactId>ruoyi-admin</artifactId>
            <version>${ruoyi.version}</version>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-websocket</artifactId>
        </dependency>
        <dependency>
            <groupId>com.vividsolutions</groupId>
            <artifactId>jts</artifactId>
            <version>1.13</version>
        </dependency>
        <dependency>
            <groupId>net.sf.ehcache</groupId>
            <artifactId>ehcache</artifactId>
        </dependency>
        <dependency>
            <groupId>org.gavaghan</groupId>
            <artifactId>geodesy</artifactId>
            <version>1.1.3</version>
        </dependency>
    </dependencies>
</project>

``` 
`如果还没有成功的，来找我吃两枣子`

5、运行前端项目，在项目`/ruoyi-ui`文件夹下

```bash
npm install #安装依赖
npm run dev	#运行
```

## 项目部署
ruoyi-vue-gl 模块引用了多模块中所有模块
所以以上都测试还没有成功的就是依赖的问题。
![](http://m.qpic.cn/psc?/V12PDn0m3Qk5yx/ruAMsa53pVQWN7FLK88i5gSdb.QJWtM94Mj96n50bHBTt0kDkrtFef6v2o4p0KJnbhfT6h3ARqsFB63Cjhc2WlsCgUq0WWSsDjGm98dQ660!/mnull&bo=PAF7ADwBewADCSw!&rf=photolist&t=5)

###idea清理安装
```bash
maven clean		#清理
maven install	#打包
```



