---
layout: web
title: JavaWeb
date: 2021-05-20 17:57:06
tags:
---
创建数据表
```mysql
create table user
(
	id int,
	name varchar(255),
	password varchar(255),
	email varchar(255),
	birthday date
);
```
连接远程数据库吧http://localhost:3306 换成ip地址
数据库是真的难