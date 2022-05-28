---
title: DDL
author: Lemon
top: false
cover: false
toc: true
mathjax: false
summary: 数据定义语言
tags:
  - 数据库
  - MySQL
categories:
  - MySQL
abbrlink: 63ad7bb4
reprintPolicy: cc_by
date: 2022-01-27 15:21:31
coverImg:
img:
password:
---

## 一、概述

`Data Definition Language`，简称 `DDL`，[数据定义语言](https://baike.baidu.com/item/DDL/21997?fr=aladdin)，是用于定义和管理数据如数据库、数据表这样的数据对象对象的语言，是 `SQL` 的一个子集。主要作用就是数据库和数据表的创建、修改和删除，用到的关键字分别为：`create`、`alter`、`drop`.

## 二、库的管理

语言：

```sql
#创建数据库
create database [if not exists] 库名 [DEFAULT CHARACTER SET [=] 字符集名];
#修改数据库的名字
rename database 旧表名 to 新表名;
#修改库的字符集
alter database 库名 character set 字符集名;
#删除数据库
drop database [if exists] 数据库名;
```

来个例子：

```mysql
#创建一个
```

