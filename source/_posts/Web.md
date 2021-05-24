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


### 1、以安全模式启动MySQL

>mysqld --skip-grant-tables

（这个窗口保持现状，不要关闭）
 
### 2、登陆mysql服务（另外新开一个cmd窗口）
mysql -uroot -p
 
提示输入密码时直接回车即可。

### 3、修改密码
>use mysql

>update user set Password=password('123456') where User='root';

>flush privileges;

>quit; 退出

