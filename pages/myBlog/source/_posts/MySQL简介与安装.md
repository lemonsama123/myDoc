---
title: MySQL简介与安装
author: Lemon
coverImg: 
top: false
cover: false
toc: true
mathjax: false
summary: MySQL数据库的介绍、安装、使用和基本命令
tags:
  - 数据库
  - MySQL
categories:
  - MySQL
abbrlink: 97104bc6
reprintPolicy: cc_by
date: 2022-01-25 17:04:50
img:
password:
---
## 一、数据库和 SQL 概述

### 1.1 数据库的好处

1. 持久化数据到本地。
2. 可以实现结构化查询，方便管理。

### 1.2 数据库相关概念

1. **DB**（Database）：数据库，保存一组有组织的数据的容器。
2. **DBMS**（Database Management System）：数据库管理系统，即数据库软件（产品），用于管理 DB 中的数据。

![DBMS和DB](https://s2.loli.net/2022/01/25/I8YV4TfAUMtCvSw.png)

3. **SQL**（Structure Query Language）：结构化查询语言，用于和 DBMS 通信。

### 1.3 数据库存储数据的特点

1. 将数据放到表中，再将表放到库中。
2. 一个数据库中可以有多个表，每个表都有一个名字，用来标识自己。表名具有唯一性。
3. 表具有唯一性，这些特性定义了数据在表中如何存储，类似于 `Java` 中的“类”。
4. 表由**列**组成，我们也称之为**字段**。所以表都是由一个或多个列组成，每一列类似于 `Java` 中的属性。
5. 表中的数据是按行存储的，每一行相当于 `Java` 的对象。

### 1.4 常见的 DBMS

- **MySQL**
- **Oracle**
- **DB2**
- **SQLServer**

## 二、MySQL 的介绍，安装和使用

![图解MySQL程序结构](https://s2.loli.net/2022/01/25/Z6WIJXgtSGbNBYU.png)

### 2.1 MySQL 数据库产品的介绍

- **MySQL** 数据库隶属于 **MySQL AB**公司，总部位于瑞典，后被 **Oracle** 收购。
- 优点：
  - 成本低：开放源代码，一般可以免费试用。
  - 性能高：执行很快。
  - 简单：很容易安装和使用



### 2.2 MySQL 数据库的安装（以 5.5 为例）

- **DBMD** 分为两类：
  - 基于共享文件系统的 **DBMS**：**Access**.
  - 基于客户机——服务器的 **DBMS**：**MySQL**、**Oracle**、**SQLServer**.

[MySQL 国内镜像](http://mirrors.ustc.edu.cn/mysql-ftp/Downloads/)

[其他版本的MySQL的安装方法](/posts/84e07c0b.html)

#### 2.2.1 安装

![安装（图1）](https://s2.loli.net/2022/01/25/QRH1S9AveTuBWyO.png)

![安装（图2）](https://s2.loli.net/2022/01/25/vlSdfFyiUPc562t.png)

![安装（图3）](https://s2.loli.net/2022/01/25/eyphMDYVIO6JsiQ.png)

![安装（图4）](https://s2.loli.net/2022/01/25/S1du94oXAf53Pxs.png)

![安装（图5）](https://s2.loli.net/2022/01/25/FLXo4BlbdnkDhMR.png)

![安装（图6）](https://s2.loli.net/2022/01/25/54MYDsi8wBPfqgA.png)

![安装（图7）](https://s2.loli.net/2022/01/25/EwRMcmeSXlbFh5t.png)

#### 2.2.2 配置

安装完毕后，会看到如下界面：

![配置（图1）](https://s2.loli.net/2022/01/25/UuXoawc6xBhYPWI.png)

如果不小心关闭了这个界面，可进入 **MySQL** 安装目录下的 **bin** 目录，找到 **MySQLInstanceConfig.exe**，双击打开。

![配置（图2）](https://s2.loli.net/2022/01/25/rdIslE7ozcneDHU.png)

开始配置

![配置（图3）](https://s2.loli.net/2022/01/25/8UiCYFuqIDhtrms.png)

![配置（图4）](https://s2.loli.net/2022/01/25/U8QH5cpBCbaoL3F.png)

![配置（图5）](https://gitee.com/lemonsama123/image/raw/master/image/20211012111958.png)

![配置（图6）](https://s2.loli.net/2022/01/25/Jr8TgHwcVk63nbz.png)

![配置（图7）](https://s2.loli.net/2022/01/25/WLbywHoCa1T6vSj.png)

![配置（图8）](https://s2.loli.net/2022/01/25/2oMwrdKHEsCgG78.png)

![配置（图9）](https://s2.loli.net/2022/01/25/vZ3faWtS4ho1VJU.png)

![配置（图10）](https://s2.loli.net/2022/01/25/izkl6uGQEmRCX3A.png)

![配置（图11）](https://s2.loli.net/2022/01/25/8HQmBgMeuTUSscP.png)

![配置（图12）](https://s2.loli.net/2022/01/25/V7RKvQOWJDMpt4A.png)

xxxxxxxxxx <div style="width: 100%;text-align: center; height: 120px; position: relative; bottom: 0px;" ><span class="particletext sunbeams" style="font-size:48px; position: relative;">This is sunbeams</span></div>html

![配置（图14）](https://s2.loli.net/2022/01/25/Pb5ZconQwkj6YsS.png)

至此，配置完毕。

### 2.3 配置文件介绍

![配置文件目录](https://s2.loli.net/2022/01/25/pIeXfh18Jb9ZLnr.png)

![配置文件](https://s2.loli.net/2022/01/25/Zw5Fjvy6cMmoXT8.png)

可直接修改配置文件来设置相关的功能。



## 三、MySQL 的使用

### 3.1 MySQL 服务的启动和停止

#### 3.1.1 方式一

![启动方式一（图1）](https://s2.loli.net/2022/01/25/9esXKpBQVDfYh8r.png)

![启动方式一（图2）](https://s2.loli.net/2022/01/25/9esXKpBQVDfYh8r.png)

![启动方式一（图3）](https://s2.loli.net/2022/01/25/usjpPWlETHomVtM.png)

![启动方式一（图4）](https://s2.loli.net/2022/01/25/8IBoidE3fWDPFqn.png)

右击可启动、停止和查看属性

![启动方式一（图5）](https://s2.loli.net/2022/01/25/tsaefkyhB1FmAnC.png)

在属性界面可以把启动类型改成手动

![启动方式一（图6）](https://s2.loli.net/2022/01/25/BnUV81ePAksKZIE.png)

#### 3.1.2 方式二

![启动方式二（图1）](https://s2.loli.net/2022/01/25/F9CTO4qg13LXtbf.png)tg

通过 `net start mysql服务名` 启动 **MySQL** 服务：

![启动方式二（图2）](https://s2.loli.net/2022/01/25/sgzE8KDFcbCUAhM.png)

通过 `net stop mysql服务名` 停止 **MySQL** 服务：

![启动方式二（图3）](https://s2.loli.net/2022/01/25/H5S6kYfZFXpqTcM.png)



### 3.2 MySQL 的登陆和退出

#### 3.2.1 方式一：通过 MySQL 自带客户端登陆（不建议使用）

![登陆方式一（图1）](https://s2.loli.net/2022/01/25/lqjmDxs3oSZ9KJY.png)

![登陆方式一（图2）](https://s2.loli.net/2022/01/25/UijYA7vCnV1pHxh.png)

这种方式貌似只能登陆到 **root** 用户，故不建议使用。

`exit` 或 <kbd>ctrl</kbd> + <kbd>c</kbd> 退出

![退出](https://s2.loli.net/2022/01/25/raTYo4i27lxpbyq.png)

#### 3.2.2 方式二：通过命令行登陆

使用 `mysql -h 主机名 端口号 -u 用户名 -p[密码]` 登陆。

如果要登陆到本机端口号为 3306 的 MySQL 数据库可简写为：`mysql -u 用户名 -p密码`.

![登陆方式二（图1）](https://s2.loli.net/2022/01/25/XhARG8ilc5vUFI9.png)

退出：`exit` 或 <kbd>ctrl</kbd> + <kbd>c</kbd> 

## 四、MySQL 常用命令

### 4.1 查看当前所有的数据库——`SHOW DATABASES;`

![SHOW DATABASES](https://s2.loli.net/2022/01/25/Jd9TDzMeSGLPw5y.png)

### 4.2 打开某个库——`USE 库名;`

![USE 库名](https://s2.loli.net/2022/01/25/3YXI5yKH2kebzQd.png)

### 4.3 查看当前库中所有表——`SHOW TABLES;`

![SHOW TABLES](https://s2.loli.net/2022/01/25/sCTKGOp5U9PldDn.png)

### 4.4 查看指定库的所有表——`SHOW TABLES FROM 库名;`

![SHOW TABLES FROM 库名](https://s2.loli.net/2022/01/25/HFZatm8xlXSnA1p.png)

### 4.5 创建数据库——`CREATE DATABASE [if not exists] 数据库名;`

![create database](https://s2.loli.net/2022/01/27/3kGtUlem4NVQMF9.png)

### 4.6 删除数据库——`drop database [if exists] 数据库名;`

![drop database](https://s2.loli.net/2022/01/27/omzClBLK6gq8k1E.png)

### 4.7 创建表

语法：

```mysql
create table 表名(  
	列名 列类型, 
	列名 列类型，
	...
);
```

![创建表](https://s2.loli.net/2022/01/25/yARO9VgkifoqH2r.png)

 ### 4.8 查看表结构——`DESC 表名;`

![DESC 表名](https://s2.loli.net/2022/01/25/Kjtcx1V7sEkprCR.png)

### 4.9  查看当前所在库——`SELECT DATABASE();`

![SELECT DATABASE()](https://s2.loli.net/2022/01/25/ZoOXAlqsh95iGNI.png)

### 4.10 查看 MySQL 版本

#### 4.10.1 方式一：登陆到 MySQL 服务端

`select version();`

![select version()](https://s2.loli.net/2022/01/25/QUyPZr923GjEVwM.png)

#### 4.10.2 方式二：没有登陆到 MySQL 服务器

` mysql --version`

![mysql --version](https://s2.loli.net/2022/01/25/vsFhH71cSxQ5942.png)

### 4.11 修改指定用户密码

语法：

```mysql
update user set password=password('新密码')where user='用户名';
```

![image-20220127112520553](https://s2.loli.net/2022/01/27/k8sVWpTjlrF96Lo.png)

> 这条命令实际上是修改 `mysql` 库中的 `user` 表的 `password` 字段。

## 五、MySQL 的语法规范

1. 不区分大小写，但建议关键字大写，表名、列明小写。
2. 每条最好用分号结尾。
3. 每条命令根据需要，可以进行缩进或换行。
4. 注释：
   1. 单行注释：`#注释文字`
   2. 单行注释：`-- 注释文字`
   3. 多行注释：`/* 注释文字 */`

