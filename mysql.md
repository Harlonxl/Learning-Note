目录
=================

* [1、SQL语言主要分为三类：](#1sql%E8%AF%AD%E8%A8%80%E4%B8%BB%E8%A6%81%E5%88%86%E4%B8%BA%E4%B8%89%E7%B1%BB)
* [2、库操作](#2%E5%BA%93%E6%93%8D%E4%BD%9C)
  * [2\.1 新增数据库](#21-%E6%96%B0%E5%A2%9E%E6%95%B0%E6%8D%AE%E5%BA%93)
  * [2\.2 查询数据库](#22-%E6%9F%A5%E8%AF%A2%E6%95%B0%E6%8D%AE%E5%BA%93)
  * [2\.3 更新数据库](#23-%E6%9B%B4%E6%96%B0%E6%95%B0%E6%8D%AE%E5%BA%93)
  * [2\.4 删除数据库](#24-%E5%88%A0%E9%99%A4%E6%95%B0%E6%8D%AE%E5%BA%93)
* [3、表操作](#3%E8%A1%A8%E6%93%8D%E4%BD%9C)
  * [3\.1 新增表](#31-%E6%96%B0%E5%A2%9E%E8%A1%A8)
  * [3\.2 查询表](#32-%E6%9F%A5%E8%AF%A2%E8%A1%A8)
  * [3\.3 更新表](#33-%E6%9B%B4%E6%96%B0%E8%A1%A8)
  * [3\.4 删除表](#34-%E5%88%A0%E9%99%A4%E8%A1%A8)
* [4、数据操作](#4%E6%95%B0%E6%8D%AE%E6%93%8D%E4%BD%9C)
  * [4\.1 新增数据](#41-%E6%96%B0%E5%A2%9E%E6%95%B0%E6%8D%AE)
  * [4\.2 查询数据](#42-%E6%9F%A5%E8%AF%A2%E6%95%B0%E6%8D%AE)
  * [4\.3 更新数据](#43-%E6%9B%B4%E6%96%B0%E6%95%B0%E6%8D%AE)
  * [4\.3 删除数据](#43-%E5%88%A0%E9%99%A4%E6%95%B0%E6%8D%AE)
* [5、字符集问题](#5%E5%AD%97%E7%AC%A6%E9%9B%86%E9%97%AE%E9%A2%98)
* [6、校对集问题](#6%E6%A0%A1%E5%AF%B9%E9%9B%86%E9%97%AE%E9%A2%98)
* [7、数值型](#7%E6%95%B0%E5%80%BC%E5%9E%8B)
  * [7\.1 整数型](#71-%E6%95%B4%E6%95%B0%E5%9E%8B)
  * [7\.2 小数型](#72-%E5%B0%8F%E6%95%B0%E5%9E%8B)
* [8、日期时间类型](#8%E6%97%A5%E6%9C%9F%E6%97%B6%E9%97%B4%E7%B1%BB%E5%9E%8B)
* [9、字符类型](#9%E5%AD%97%E7%AC%A6%E7%B1%BB%E5%9E%8B)
* [10、记录长度](#10%E8%AE%B0%E5%BD%95%E9%95%BF%E5%BA%A6)
* [11、列属性](#11%E5%88%97%E5%B1%9E%E6%80%A7)
  * [11\.1 空属性](#111-%E7%A9%BA%E5%B1%9E%E6%80%A7)
  * [11\.2 列描述](#112-%E5%88%97%E6%8F%8F%E8%BF%B0)
  * [11\.3 默认值](#113-%E9%BB%98%E8%AE%A4%E5%80%BC)
  * [11\.4 主键](#114-%E4%B8%BB%E9%94%AE)
  * [11\.5 自动增长](#115-%E8%87%AA%E5%8A%A8%E5%A2%9E%E9%95%BF)
  * [11\.6 唯一键](#116-%E5%94%AF%E4%B8%80%E9%94%AE)
* [12、索引](#12%E7%B4%A2%E5%BC%95)
* [13、关系](#13%E5%85%B3%E7%B3%BB)
  * [13\.1 一对一](#131-%E4%B8%80%E5%AF%B9%E4%B8%80)
  * [13\.2  一对多](#132--%E4%B8%80%E5%AF%B9%E5%A4%9A)
  * [13\.3 多对多](#133-%E5%A4%9A%E5%AF%B9%E5%A4%9A)
* [14、范式](#14%E8%8C%83%E5%BC%8F)
  * [14\.1 1NF](#141-1nf)
  * [14\.2 2NF](#142-2nf)
  * [14\.3 3NF](#143-3nf)
  * [14\.4 逆规范化](#144-%E9%80%86%E8%A7%84%E8%8C%83%E5%8C%96)
* [15、主键冲突](#15%E4%B8%BB%E9%94%AE%E5%86%B2%E7%AA%81)
* [16、蠕虫复制](#16%E8%A0%95%E8%99%AB%E5%A4%8D%E5%88%B6)
* [17、数据库高级操作](#17%E6%95%B0%E6%8D%AE%E5%BA%93%E9%AB%98%E7%BA%A7%E6%93%8D%E4%BD%9C)
  * [17\.1 更新数据](#171-%E6%9B%B4%E6%96%B0%E6%95%B0%E6%8D%AE)
  * [17\.2 删除数据](#172-%E5%88%A0%E9%99%A4%E6%95%B0%E6%8D%AE)
* [18、查询高级操作](#18%E6%9F%A5%E8%AF%A2%E9%AB%98%E7%BA%A7%E6%93%8D%E4%BD%9C)
  * [18\.1 select 选项](#181-select-%E9%80%89%E9%A1%B9)
  * [18\.2 字段别名](#182-%E5%AD%97%E6%AE%B5%E5%88%AB%E5%90%8D)
  * [18\.3 数据源](#183-%E6%95%B0%E6%8D%AE%E6%BA%90)
  * [18\.4 where子句](#184-where%E5%AD%90%E5%8F%A5)
  * [18\.5 group by 子句](#185-group-by-%E5%AD%90%E5%8F%A5)
  * [18\.6 having 子句](#186-having-%E5%AD%90%E5%8F%A5)
  * [18\.7 order by子句](#187-order-by%E5%AD%90%E5%8F%A5)
* [19、连接查询](#19%E8%BF%9E%E6%8E%A5%E6%9F%A5%E8%AF%A2)
  * [19\.1 交叉连接](#191-%E4%BA%A4%E5%8F%89%E8%BF%9E%E6%8E%A5)
  * [19\.2 内连接](#192-%E5%86%85%E8%BF%9E%E6%8E%A5)
  * [19\.3 外链接](#193-%E5%A4%96%E9%93%BE%E6%8E%A5)
  * [19\.4 自然连接](#194-%E8%87%AA%E7%84%B6%E8%BF%9E%E6%8E%A5)
* [20、外键](#20%E5%A4%96%E9%94%AE)
  * [20\.1 外键操作](#201-%E5%A4%96%E9%94%AE%E6%93%8D%E4%BD%9C)
  * [20\.2 外键作用](#202-%E5%A4%96%E9%94%AE%E4%BD%9C%E7%94%A8)
  * [20\.3 外键条件](#203-%E5%A4%96%E9%94%AE%E6%9D%A1%E4%BB%B6)
  * [20\.4 外键约束](#204-%E5%A4%96%E9%94%AE%E7%BA%A6%E6%9D%9F)
* [21、联合查询](#21%E8%81%94%E5%90%88%E6%9F%A5%E8%AF%A2)
* [22、子查询](#22%E5%AD%90%E6%9F%A5%E8%AF%A2)
  * [22\.1 标量子查询](#221-%E6%A0%87%E9%87%8F%E5%AD%90%E6%9F%A5%E8%AF%A2)
  * [22\.2 列子查询](#222-%E5%88%97%E5%AD%90%E6%9F%A5%E8%AF%A2)
  * [22\.3 行子查询](#223-%E8%A1%8C%E5%AD%90%E6%9F%A5%E8%AF%A2)
  * [22\.4 表子查询](#224-%E8%A1%A8%E5%AD%90%E6%9F%A5%E8%AF%A2)
  * [22\.5 exists子查询](#225-exists%E5%AD%90%E6%9F%A5%E8%AF%A2)
* [23、视图](#23%E8%A7%86%E5%9B%BE)
  * [23\.1 创建视图](#231-%E5%88%9B%E5%BB%BA%E8%A7%86%E5%9B%BE)
  * [23\.2 查询视图](#232-%E6%9F%A5%E8%AF%A2%E8%A7%86%E5%9B%BE)
  * [23\.3 使用视图](#233-%E4%BD%BF%E7%94%A8%E8%A7%86%E5%9B%BE)
  * [23\.4 修改视图](#234-%E4%BF%AE%E6%94%B9%E8%A7%86%E5%9B%BE)
  * [23\.5 删除视图](#235-%E5%88%A0%E9%99%A4%E8%A7%86%E5%9B%BE)
  * [23\.6 视图意义](#236-%E8%A7%86%E5%9B%BE%E6%84%8F%E4%B9%89)
* [24、视图数据操作](#24%E8%A7%86%E5%9B%BE%E6%95%B0%E6%8D%AE%E6%93%8D%E4%BD%9C)
  * [24\.1 新增数据](#241-%E6%96%B0%E5%A2%9E%E6%95%B0%E6%8D%AE)
  * [24\.2 删除数据](#242-%E5%88%A0%E9%99%A4%E6%95%B0%E6%8D%AE)
  * [24\.3 更新数据](#243-%E6%9B%B4%E6%96%B0%E6%95%B0%E6%8D%AE)
  * [24\.4 视图算法](#244-%E8%A7%86%E5%9B%BE%E7%AE%97%E6%B3%95)
* [25、数据备份与还原](#25%E6%95%B0%E6%8D%AE%E5%A4%87%E4%BB%BD%E4%B8%8E%E8%BF%98%E5%8E%9F)
  * [25\.1 数据表备份](#251-%E6%95%B0%E6%8D%AE%E8%A1%A8%E5%A4%87%E4%BB%BD)
  * [25\.2 单数据表备份](#252-%E5%8D%95%E6%95%B0%E6%8D%AE%E8%A1%A8%E5%A4%87%E4%BB%BD)
  * [25\.3 SQL备份](#253-sql%E5%A4%87%E4%BB%BD)
  * [25\.4 增量备份](#254-%E5%A2%9E%E9%87%8F%E5%A4%87%E4%BB%BD)
* [26、事务](#26%E4%BA%8B%E5%8A%A1)
  * [26\.1 事务操作](#261-%E4%BA%8B%E5%8A%A1%E6%93%8D%E4%BD%9C)
  * [26\.2 事务原理](#262-%E4%BA%8B%E5%8A%A1%E5%8E%9F%E7%90%86)
  * [26\.3 回滚点](#263-%E5%9B%9E%E6%BB%9A%E7%82%B9)
  * [26\.4 自动事务](#264-%E8%87%AA%E5%8A%A8%E4%BA%8B%E5%8A%A1)
  * [26\.5 事务特性](#265-%E4%BA%8B%E5%8A%A1%E7%89%B9%E6%80%A7)
* [27、数据库变量](#27%E6%95%B0%E6%8D%AE%E5%BA%93%E5%8F%98%E9%87%8F)
  * [27\.1 系统变量](#271-%E7%B3%BB%E7%BB%9F%E5%8F%98%E9%87%8F)
  * [27\.2 自定义变量](#272-%E8%87%AA%E5%AE%9A%E4%B9%89%E5%8F%98%E9%87%8F)
* [28、触发器](#28%E8%A7%A6%E5%8F%91%E5%99%A8)
  * [28\.1 创建触发器](#281-%E5%88%9B%E5%BB%BA%E8%A7%A6%E5%8F%91%E5%99%A8)
  * [28\.2 查询触发器](#282-%E6%9F%A5%E8%AF%A2%E8%A7%A6%E5%8F%91%E5%99%A8)
  * [28\.3 使用触发器](#283-%E4%BD%BF%E7%94%A8%E8%A7%A6%E5%8F%91%E5%99%A8)
  * [28\.4 修改触发器 &amp; 删除触发器](#284-%E4%BF%AE%E6%94%B9%E8%A7%A6%E5%8F%91%E5%99%A8--%E5%88%A0%E9%99%A4%E8%A7%A6%E5%8F%91%E5%99%A8)
  * [28\.5 触发器记录](#285-%E8%A7%A6%E5%8F%91%E5%99%A8%E8%AE%B0%E5%BD%95)
* [29、代码执行结构](#29%E4%BB%A3%E7%A0%81%E6%89%A7%E8%A1%8C%E7%BB%93%E6%9E%84)
  * [29\.1 分支结构](#291-%E5%88%86%E6%94%AF%E7%BB%93%E6%9E%84)
  * [29\.2 循环结构](#292-%E5%BE%AA%E7%8E%AF%E7%BB%93%E6%9E%84)
* [30、函数](#30%E5%87%BD%E6%95%B0)
  * [30\.1 系统函数](#301-%E7%B3%BB%E7%BB%9F%E5%87%BD%E6%95%B0)
  * [30\.2 自定义函数](#302-%E8%87%AA%E5%AE%9A%E4%B9%89%E5%87%BD%E6%95%B0)
  * [30\.3 创建函数](#303-%E5%88%9B%E5%BB%BA%E5%87%BD%E6%95%B0)
  * [30\.4 查看函数](#304-%E6%9F%A5%E7%9C%8B%E5%87%BD%E6%95%B0)
  * [30\.5 修改函数 &amp; 删除函数](#305-%E4%BF%AE%E6%94%B9%E5%87%BD%E6%95%B0--%E5%88%A0%E9%99%A4%E5%87%BD%E6%95%B0)
  * [30\.6 函数参数](#306-%E5%87%BD%E6%95%B0%E5%8F%82%E6%95%B0)
  * [30\.7 变量作用域](#307-%E5%8F%98%E9%87%8F%E4%BD%9C%E7%94%A8%E5%9F%9F)
* [31、存储过程](#31%E5%AD%98%E5%82%A8%E8%BF%87%E7%A8%8B)
  * [31\.1 创建过程](#311-%E5%88%9B%E5%BB%BA%E8%BF%87%E7%A8%8B)
  * [32\.2 查看过程](#322-%E6%9F%A5%E7%9C%8B%E8%BF%87%E7%A8%8B)
  * [32\.3 调用过程](#323-%E8%B0%83%E7%94%A8%E8%BF%87%E7%A8%8B)
  * [33\.3 修改过程 &amp; 删除过程](#333-%E4%BF%AE%E6%94%B9%E8%BF%87%E7%A8%8B--%E5%88%A0%E9%99%A4%E8%BF%87%E7%A8%8B)
  * [33\.4 过程参数](#334-%E8%BF%87%E7%A8%8B%E5%8F%82%E6%95%B0)

# 1、SQL语言主要分为三类：
- DDL：Data Defination Language，数据定义语言，用来维护存储数据的结构（数据库、表），例如create、drop和alter操作
- DML：Data  Manipulation Language，数据操作语言，用来对数据进行操作，例如delete、update、insert，又可细分为DQL（Data Query Language），数据查询语言，例如select
- DCL：Data Control Language，数据控制语言，用于负责用户权限管理，例如grant、revoke等
- - - - -
# 2、库操作
## 2.1 新增数据库

基本语法：
``` SQL
create database 数据库名称 数据库选项;
```
数据库选项：
- 字符集设定：charset + 字符集，用来表示数据存储的编码格式，常用的字符集包括GBK和UTF8等
- 校对集设定：collate + 具体校对集，表示数据比较的规则，其依赖字符集
实例：
``` SQL
create database mydatabase charset utf8;
```
注意：
- 数据库名称最好别不要使用中文
- 数据库名称不要用关键字和保留字
- 如果要使用关键字和保留字，用反引号括起来

- - - - -
## 2.2 查询数据库
基本语法：
``` SQL
show databases;
```
模糊查询语法：
``` SQL
show databases like 'pattern';
```
其中，pattern是匹配模式，有两种，分别是：
- %：表示匹配多个字符
- _：表示匹配单个字符

如果库名中有_时，要用\_进行转义。
- - - - -
## 2.3 更新数据库
基本语法：
``` SQL
alter dabase 数据库名称 数据选项
```
实例：
``` SQL
alter database mydatabase charset gdk;
```
注意：
- 数据库名称不可更改
- - - - -
## 2.4 删除数据库
基本语法：
``` SQL
drop database 数据库名称;
```
注意：
- 删除是不可逆操作，删除之前要先备份数据库
- - - - -
# 3、表操作
## 3.1 新增表

基本语法：
``` SQL
create table [if not exists] 表名(
    字段名称 数据类型;
    ...
    字段名称 数据类型
)[表选项];
```
其中，if not exists 表示：
- 如果表名不存在，就执行创建代码；如果表名存在，则不执行创建代码。

表选项则是用来控制表的表现形式的，共有三种，分别为：
- 字符集设定：charset 具体字符集，用来指定存储的数据的编码格式，常用的有GBK和UTF8
- 校对集设定：collate 具体校对集，表示数据比较的规则，其依赖字符集
- 存储引擎：engine 具体存储引擎，默认为InnoDB，常用的还有MyISAM

实例一：实现的指定表所属的数据库
``` SQL
create table if not exists test.Student(
    name varchar(10),
    age int,
    grade varchar(10)
) engine InnoDB charset utf8;
```
实例二：隐式的指定表所属的数据库
``` SQL
use test;
create table if not exists Student(
    name varchar(10),
    age int,
    grade varchar(10)
) engine InnoDB charset utf8;
```
- - - - -
## 3.2 查询表
基本语法：
``` SQL
show tables;
```
模糊查询语法：
``` SQL
show tables like 'pattern';
```
其中，pattern是匹配模式，有两种，分别是：
- %：表示匹配多个字符
- _：表示匹配单个字符

查看表中的字段信息：
``` c++
desc/describe/show columns from 表名;
```
- - - - -
## 3.3 更新表
表的修改，分为修改表本身和修改表中的字段。  
第1类：修改表本身
- 修改表名，基本语法：
``` SQL
rename table 旧表名 to 新表名;
```
- 修改表选项，基本语法：
``` SQL
alter table 表名 表选项[=] 值;
```
第2类：修改表中的字段，新增、修改、重命名和删除
- 新增字段，基本语法：
``` SQL
alter table 表名 add [column] 字段名 数据类型 [列属性][位置];
```
其中，位置表示此字段存储的位置，分为first（第一个位置）和after + 字段名（指定的字段后，默认为最后一个位置）。
实例：
``` SQL
alter table Student add column id int first;
```
- 修改字段，基本语法：
``` SQL
alter table 表名 modify 字段名 数据类型 [列属性][位置];
```
实例：
``` SQL
alter table Student modify name char(10) after id;
```
- 重命名字段，基本语法：
``` SQL
alter table 表名 change 旧字段名 新字段名 数据类型 [列属性][位置];
```
实例：
``` SQL
alter table Student change grage class varchar(10);
```
- - - - -
- 删除字段，基本语法：
``` SQL
alter table 表名 drop 字段名;
```
实例：
``` SQL
alter table Student drop age;
```
注意：
- 如果表中已经存在数据，那么删除该字段会清空该字段所有的数据，且不可逆，慎用。
- - - - -
## 3.4 删除表
基本语法：
``` SQL
drop table 表1, 表2;
```
 注意：
- 删除表为不可逆操作，慎用。
- - - - -
# 4、数据操作
SQL的基本操作CURD，即增删改查
## 4.1 新增数据
对于数据的新增操作，有两种方法。  
第1种：给全表字段插入数据，不需要指定字段列表，但要求数据的值出现的顺序与表中的字段出现的顺序一致，而且凡是非数值数据，都需要用引号括起来。
基本语法：
``` SQL
insert into 表名 values(值列表[,(值列表)]);
```
实例：
``` SQL
insert into Student values(1, 'Harlon', 'class-1');
```
第2种：给部分字段插入数据，需要选定字段列表，字段列表中字段出现的顺序与表中字段的顺序无关，但值列表的顺序必须与字段列表的保持一致。  
基本语法：
``` SQL
insert into 表名(字段列表) values(值列表[,(值列表)]);
```
实例：
``` SQL
insert into Student(name, class) values('Juice', 'class-2');
```
- - - - -
## 4.2 查询数据
基本语法：
``` SQL
select * from 表名 [where 条件];
```
查看部分，基本语法：
``` SQL
select 字段名称[,字段名称] from 表名 [where 条件];
```
实例：
``` SQL
select name, class from Student;
```
- - - - -
## 4.3 更新数据
基础语法：
``` SQL
update 表名 字段 = 值 [where 条件];
```
在这里，尽量加上where条件，否则的话，操作就是全表数据。  
实例：
``` SQL
update Student set class = 'class-2' where id=1;
```
- - - - -
## 4.3 删除数据
基本语法：
``` SQL
delete from 表名 [where 条件];
```
实例：
``` SQL
delete from Strudent where name='Juice';
```
我们也可以用drop实现删除操作，不过与delete相比，drop威力更强，其在执行删除操作的时候，不仅会删除数据，还会删除定义并释放存储空间；而delete删除的时候，仅会删除数据，并不会删除定义和释放存储空间。
- - - - -
# 5、字符集问题
查看服务器识别的字符集
``` SQL
show character set;
```
查看服务器默认的对外处理的字符集
``` SQL
show variables like 'character_set%';
```
修改字符传输方式：
``` SQL
set names utf8;
```
- - - - -
# 6、校对集问题
校对集有三种：
- _bin：binary，二进制比较，区分大小写
- _cs：case sensitive，大小写敏感，区分大小写
- _ci：case insensitive，大小写不敏感，不区分大小写

查看全部校对集：
``` SQL
show collation;
```
注意：
- 如果在没有数据之前没有声明校对集，在有了数据之后，再对校对集进行修改，则修改无效

- - - - -
# 7、数值型
在SQL中，将数据类型分为三大类，分别为：数值型、字符串型和日期时间型
![](https://img-blog.csdn.net/20170505201016682)
## 7.1 整数型
在SQL中，由于要考虑节省磁盘空间的问题，因此系统又将整型分配五类，分别为：
- tinyint：迷你整型，使用1个字节存储数据（常用）
- smallint：小整型，使用2个字节存储数据
- mediumint：中整型，使用3个字节存储数据
- int：标准整型，使用4个字节存储数据（常用）
- bigint：大整型，使用8个字节存储数据

实例：
``` SQL
create table my_int( 
    int_1 tinyint, 
    int_2 smallint, 
    int_3 int, 
    int_4 bigint 
) engine InnoDB charset utf8;
```
``` SQL
mysql> desc my_int;
+-------+-------------+------+-----+---------+-------+
| Field | Type        | Null | Key | Default | Extra |
+-------+-------------+------+-----+---------+-------+
| int_1 | tinyint(4)  | YES  |     | NULL    |       |
| int_2 | smallint(6) | YES  |     | NULL    |       |
| int_3 | int(11)     | YES  |     | NULL    |       |
| int_4 | bigint(20)  | YES  |     | NULL    |       |
+-------+-------------+------+-----+---------+-------+
```
每个字段的数据后面都会跟一堆括号，并且里面含有数字，这表示数据的显示宽度。
``` SQL
mysql> alter table my_int add int_5 tinyint zerofill;
Query OK, 0 rows affected (0.05 sec)
Records: 0  Duplicates: 0  Warnings: 0
mysql> desc my_int;
+-------+------------------------------+------+-----+---------+-------+
| Field | Type                         | Null | Key | Default | Extra |
+-------+------------------------------+------+-----+---------+-------+
| int_1 | tinyint(4)                   | YES  |     | NULL    |       |
| int_2 | smallint(6)                  | YES  |     | NULL    |       |
| int_3 | int(11)                      | YES  |     | NULL    |       |
| int_4 | bigint(20)                   | YES  |     | NULL    |       |
| int_5 | tinyint(3) unsigned zerofill | YES  |     | NULL    |       |
+-------+------------------------------+------+-----+---------+-------+
5 rows in set (0.00 sec)
```
- - - - -
## 7.2 小数型
在SQL中，将小数型分为浮点型和顶点型两种，其中：
- 浮点型：小数点浮动，精度有限，容易丢失精度
- 定点型：小数点固定，精度固定，不会丢失精度

第1种：浮点型
浮点型数据是一种精度型数据，因为超出指定范围之后，其会丢失精度，自动进行四舍五入操作，分为两种精度：
- float：单精度，占用4个字节存储数据，精度范围大概7位左右
- double：双精度，占用8个字节存储数据，精度范围15位左右

浮点型使用方式：如果直接使用float，则表示没有小数部分；如果用float(M, D)，其中M代表总长度，D代表小数部分长度，M-D则为证书部分长度。  
实例：
``` SQL
create table my_float(
    f1 float,
    f2 float(10, 2),
    f3 float(6, 2)
) engine InnoDB charset utf8;
```
插入浮点数时，可以直接插入小数，也可以插入科学计数法表示的数据，此外，插入浮点型数据时，整数部分不能超出长度范围，但小数部分可以超出长度范围的，系统会自动进行四舍五入操作。
``` SQL
mysql> insert into my_float values(2.15e4, 20.15, 9999.99);
Query OK, 1 row affected (0.00 sec)

mysql> insert into my_float values(20180710, 33.338888, 9999.99);
Query OK, 1 row affected (0.00 sec)

mysql> select * from my_float;
+----------+-------+---------+
| f1       | f2    | f3      |
+----------+-------+---------+
|    21500 | 20.15 | 9999.99 |
| 20180700 | 33.34 | 9999.99 |
+----------+-------+---------+
2 rows in set (0.00 sec)
```
第2种：定点型
定点型数据，绝对的保证整数部分不会被四舍五入，也就是说不会丢失精度，但小数部分有可能会丢失精度，虽然理论上小数部分也不会丢失精度。  
实例：
``` SQL
create table my_decimal (
    f1 float(10, 2),
    d1 decimal(10, 2)
) engine InnoDB charset utf8;
```
``` SQL
mysql> insert into my_decimal values(99999999.99, 99999999.99);
Query OK, 1 row affected (0.01 sec)

mysql> insert into my_decimal values(123456.99, 2018.1364);
Query OK, 1 row affected, 1 warning (0.00 sec)

mysql> select * from my_decimal;
+--------------+-------------+
| f1           | d1          |
+--------------+-------------+
| 100000000.00 | 99999999.99 |
|    123456.99 |     2018.14 |
+--------------+-------------+
2 rows in set (0.00 sec)
```
- - - - -
# 8、日期时间类型
日期时间类型共有物种类型，分别为：
- datetime：日期时间，其格式为yyyy-MM-dd HH:mm:ss，表示的范围是1000年到9999年，有零值，即0000-00-00 00:00:00
- date：日期，就是datetime的date部分
- time：时间，或者说是时间段，为指定的某个时间区间之间，包含正负时间；
- timestamp：时间戳，但并不是真正意义上的时间戳，其是从1970年开始计算的，格式和datetime一致
- year：年份，有两种格式，分别为year(2)和year(4)

实例：
``` SQL
create table my_date(
    d1 datetime,
    d2 date,
    d3 time,
    d4 timestamp,
    d5 year
) engine InnoDB charset utf8;
```
日期时间型中的time，可以为负数，甚至可以是很大的负数；year，可以使用 2 位数据插入，也可以使用 4 位数据插入；timestamp，只要当前所在的记录被更新，该字段就会自动更新为当前时间，且时间戳类型默认为非空的。
``` SQL
mysql> insert into my_date values('2018-07-10 13:15:00', '2017-07-10', '18:49:00', '2018-07-10 13:15:00', 2018);
Query OK, 1 row affected (0.00 sec)

mysql> insert into my_date values('2018-07-10 13:15:00', '2017-07-10', '-135:49:00', '2018-07-10 13:15:00', 69);
Query OK, 1 row affected (0.01 sec)

mysql> insert into my_date values('2018-07-10 13:15:00', '2017-07-10', '-2 35:49:00', '2018-07-10 13:15:00', 70);
Query OK, 1 row affected (0.04 sec)

mysql> select * from my_date;
+---------------------+------------+------------+---------------------+------+
| d1                  | d2         | d3         | d4                  | d5   |
+---------------------+------------+------------+---------------------+------+
| 2018-07-10 13:15:00 | 2017-07-10 | 18:49:00   | 2018-07-10 13:15:00 | 2018 |
| 2018-07-10 13:15:00 | 2017-07-10 | -135:49:00 | 2018-07-10 13:15:00 | 2069 |
| 2018-07-10 13:15:00 | 2017-07-10 | -83:49:00  | 2018-07-10 13:15:00 | 1970 |
+---------------------+------------+------------+---------------------+------+
3 rows in set (0.00 sec)
```
``` SQL
mysql> update my_date set d1 = '2017-07-10 18:54:00' where d5 = 1970;
Query OK, 1 row affected (0.00 sec)
Rows matched: 1  Changed: 1  Warnings: 0

mysql> select * from my_date;
+---------------------+------------+------------+---------------------+------+
| d1                  | d2         | d3         | d4                  | d5   |
+---------------------+------------+------------+---------------------+------+
| 2018-07-10 13:15:00 | 2017-07-10 | 18:49:00   | 2018-07-10 13:15:00 | 2018 |
| 2018-07-10 13:15:00 | 2017-07-10 | -135:49:00 | 2018-07-10 13:15:00 | 2069 |
| 2017-07-10 18:54:00 | 2017-07-10 | -83:49:00  | 2018-07-10 18:54:50 | 1970 |
+---------------------+------------+------------+---------------------+------+
3 rows in set (0.00 sec)
```
- - - - -
# 9、字符类型
在SQL中，将字符串分为6类，分别为：char、varchar、text、blob、enum和set  
第1类：定长字符串
定长字符串：char，即磁盘在定义结构的时候就确定了最终数据的长度。
- char(L)：L表示length，即存储的长度，最大长度为255
- char(4)：表示在utf8情况下，需要4*3 = 12字节

第2类：变长字符串
变长字符串：varchar，即在分配空间的时候，按照最大的空间进行分配，但是实际用了多少，则是根据具体的数据来确定。
- varchar(L)：L表示length，理论长度是65536，但是会多出来1到2个字节来确定存储的实际长度
- varchar(10)：例如存储10个汉字，在UTF8环境下，需要10*3+1 = 31个字节
实际上，如果超过255个字符，用text。
如何选择定长字符串或者变长字符串呢？
- 定长字符串对磁盘空间比较浪费，但是效率高；如果数据基本上确定长度都一样，就使用定长字符串，例如身份证、电话号码等
- 变长字符串对磁盘空间比较节省，但是效率低；如果数据不能确定长度（不同的数据有变化），就使用变长字符串，例如地址、姓名等

第3类：文本字符串
如果数据量非常大，通常说超过255个字符就会使用文本字符串。  
文本字符串根据存储的格式分类，可以分为：
- text：存储文字
- blob：存储二进制数据（其实际上都是存储路径），通常不用

第4类：枚举字符串
枚举字符串：enum，需要事先将可能出现的结果都设计好，实际上存储的数据必须是规定好的数据中的一个。  
枚举字符串的使用方式：
- 定义：enum('元素1', '元素2', '元素3', ...)
- 使用：存储的数据，只能是事先定义好的数据

实例：
``` SQL
create table my_enum(
    gender enum('男', '女', '保密')
) engine InnoDB charset utf8;
```
``` SQL
mysql> insert into my_enum values('男'), ('女'), ('保密');
Query OK, 3 rows affected (0.00 sec)
Records: 3  Duplicates: 0  Warnings: 0

mysql> insert into my_enum values('male');
ERROR 1265 (01000): Data truncated for column 'gender' at row 1
mysql> select * from my_enum;
+--------+
| gender |
+--------+
| 男     |
| 女     |
| 保密   |
+--------+
3 rows in set (0.00 sec)
```
枚举除了规范数据格式外，还能节省空间，因为枚举存储的是一个数值，而不是字符串本身。枚举的效率不高。

第5类：集合字符串
集合字符串：set，跟枚举类似，实际存储的是数值而不是字符串。
集合字符串的使用方式：
- 定义：set，元素列表；
- 使用：可以使用元素列表中的多个元素，用逗号分隔

实例：
``` SQL
create table my_set(
    hobby set('音乐', '电影', '旅行', '美食', '摄影', '运动', '宠物')
) engine InnoDB charset utf8;
```
``` SQL
mysql> insert into my_set values('电影,旅行,摄影');
Query OK, 1 row affected (0.00 sec)

mysql> insert into my_set values(3);
Query OK, 1 row affected (0.01 sec)

mysql> select * from my_set;
+----------------------+
| hobby                |
+----------------------+
| 电影,旅行,摄影       |
| 音乐,电影            |
+----------------------+
2 rows in set (0.00 sec)
```
同样，使用集合的效率并不高，但能规范数据和节省空间。
- - - - -
# 10、记录长度
MySQL规定：任何一条记录最长不超过65535个字节，这意味着varchar永远达不到理论最大值。
- - - - -
# 11、列属性
列属性：实际上，真正约束字段的数据类型，但是数据类型的约束比较单一，因此就需要额外的一些约束来保证数据的有效性，这就是列属性。  
列属性有很多：例如：null、not null、default、primary key、unique key、auto_increment和comment等。

## 11.1 空属性
空属性有两个值，分别为：null和not null  
虽然默认数据库的字段基本都为空，但是实际上真正开发的时候，要尽可能的保证数据不为空，因为空数据没有意义，也没办法参与运算。

实例：
``` SQL
create table my_class (
    grade varchar(20) not null,
    room varchar(20) null -- 显示声明为空，实际上，默认就为空
) engine InnoDB charset utf8;
```
``` SQL
mysql> desc my_class;
+-------+-------------+------+-----+---------+-------+
| Field | Type        | Null | Key | Default | Extra |
+-------+-------------+------+-----+---------+-------+
| grade | varchar(20) | NO   |     | NULL    |       |
| room  | varchar(20) | YES  |     | NULL    |       |
+-------+-------------+------+-----+---------+-------+
2 rows in set (0.00 sec)
```
- - - - -
## 11.2 列描述
列描述：comment，表示描述，没有实际含义，是专门用来存储描述字段的，其会随着创建语句自动保存，用来给程序员（数据库管理员）了解数据库使用。  

实例：
``` SQL
create table my_friend(
    name varchar(20) not null comment '姓名',
    age tinyint not null comment '年龄'
) engine InnoDB charset utf8;
```

``` SQL
mysql> desc my_friend;
+-------+-------------+------+-----+---------+-------+
| Field | Type        | Null | Key | Default | Extra |
+-------+-------------+------+-----+---------+-------+
| name  | varchar(20) | NO   |     | NULL    |       |
| age   | tinyint(4)  | NO   |     | NULL    |       |
+-------+-------------+------+-----+---------+-------+
2 rows in set (0.00 sec)

mysql> show create table my_friend;
+-----------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Table     | Create Table                                                                                                                                                 |
+-----------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| my_friend | CREATE TABLE `my_friend` (
  `name` varchar(20) NOT NULL COMMENT '姓名',
  `age` tinyint(4) NOT NULL COMMENT '年龄'
) ENGINE=InnoDB DEFAULT CHARSET=utf8     |
+-----------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
1 row in set (0.00 sec)
```
- - - - -

## 11.3 默认值
默认值：default，某一数据会经常性出现某个具体的值，因此可以在开始的时候就制定好，而在需要真实数据的时候，用户可以选择性的使用默认值。  

实例：
``` SQL
create table my_default(
    name varchar(20) not null,
    age tinyint unsigned default 0,
    gender enum('男', '女') default '男'
) engine InnoDB charset utf8;
```

``` SQL
mysql> insert into my_default(name) values('Harlon');
Query OK, 1 row affected (0.00 sec)

mysql> insert into my_default values('Juice', 18, default);
Query OK, 1 row affected (0.00 sec)

mysql> select * from my_default;
+--------+------+--------+
| name   | age  | gender |
+--------+------+--------+
| Harlon |    0 | 男     |
| Juice  |   18 | 男     |
+--------+------+--------+
2 rows in set (0.00 sec)
```
- - - - -
## 11.4 主键
主键：primary key，表中主要的键，每张表只能有一个字段（复合主键，可以是多个字段）使用此属性，用来唯一的约束该字段里面的数据，不能重复。  
增加主键：  
在SQL操作中，有3种方法可以给表增加主键，分别为：  
第1种：在创建表的时候，直接在字段之后，添加primary key关键字。  

实例：
``` SQL
 create table my_pri (
    name varchar(20) not null comment '姓名',
    number char(10) primary key comment '学号'
) engine InnoDB charset utf8;
```
这种方法清晰明了，缺点是只能使用一个字段作为主键。  

第2种：在创建表的时候，在所有的字段之后，使用primary key（主键字段列表）来创建主键（如果有多个字段作为主键，则称之为符合主键）  

实例：
``` SQL
create table my_pri2(
    number char(10) not null comment '学号',
    course char(10) not null comment '课程编号',
    score tinyint unsigned default 60,
    primary key(number, course)
) engine InnoDB charset utf8;
```

第3种：当表创建之后，额外追加主键，可以直接追加主键，也可以通过修改字段的属性追回主键。  

实例：
``` SQL
create table my_pri3 (
    course char(10) not null comment '课程编号',
    name varchar(10) not null comment '课程名称'
) engine InnoDB charset utf8;
```
追加主键的方式有两种：
- alter table my_pri3 modify course char(10) primary key comment '课程' -- 不建议使用
- alter table my_pri3 add primary key(course) -- 推荐使用

使用此方法的前提是表中的数据是不重复的，即保证唯一性。  

更新主键 & 删除主键  
对于主键，没有办法直接更新，主键必须先删除，然后才能更新  
基本语法：  
``` SQL
alter table 表名 drop primary key;
```

主键分类：  
根据主键的字段类型，我们可以将主键分类两类，分别为：
- 业务主键：即使用真实的业务数据作为主键，例如学号、课程编号等等，很少使用
- 逻辑主键：即使用逻辑性的字段作为主键，字段没有业务含义，值有没有都没有关系，经常使用
- - - - -
## 11.5 自动增长
自动增长：auto_increment，当对应的字段，不给值，或者是默认值，或者是null的时候，就会自动的被系统触发，系统会从当前字段中取得已有的最大值再进行+1操作，得到新的字段值。  
自增长通过跟主键进行搭配使用，其特点是：
- 任何字段要做自增长，前提其本身必须是一个索引，即key栏有值
- 自增必须是数字（整型）
- 每张表最多有一个自增长类型

实例：
``` SQL
create table my_auto (
    id int primary key auto_increment,
    name varchar(20) not null
) engine InnoDB charset utf8;
```
``` SQL
mysql> insert into my_auto values('Harlon');
ERROR 1136 (21S01): Column count doesn't match value count at row 1
mysql> insert into my_auto(name) values('Harlon');      
Query OK, 1 row affected (0.00 sec)

mysql> insert into my_auto values(null, 'Juice');
Query OK, 1 row affected (0.30 sec)

mysql> insert into my_auto values(default, 'Ellie'); 
Query OK, 1 row affected (0.01 sec)

mysql> select * from my_auto;
+----+--------+
| id | name   |
+----+--------+
|  1 | Harlon |
|  2 | Juice  |
|  3 | Ellie  |
+----+--------+
3 rows in set (0.00 sec)

mysql> show create table my_auto;
+---------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Table   | Create Table                                                                                                                                                               |
+---------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| my_auto | CREATE TABLE `my_auto` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `name` varchar(20) NOT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=4 DEFAULT CHARSET=utf8 |
+---------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
1 row in set (0.00 sec)
```
修改自增长  
自增长如果涉及到字段变化，必须先删除自增长，然后再增加增长，因为一个表只有有一个自增长字段。  
如果修改当前自增长已经存在的值，则只能修改比当前已有自增长字段中的最大值更大，不能更小，因为更小不生效。  
基本语法：
``` SQL
alter table 表名 auto_increment = 值;
```
``` SQL
mysql> show variables like 'auto_increment%';
+--------------------------+-------+
| Variable_name            | Value |
+--------------------------+-------+
| auto_increment_increment | 1     |
| auto_increment_offset    | 1     |
+--------------------------+-------+
2 rows in set (0.00 sec)
```
其中auto_increment_increment表示自增长步长，auto_increment_offset表示自增长的初值。  

删除自增长：  
基本语法：
``` SQL
alter table 表名 modify 字段 类型
```

实例：
``` SQL
alter table my_auto modify id int;
```
- - - - -
## 11.6 唯一键
唯一键：每张表往往有多个字段需要具有唯一性，数据不能重复，但是在每个表中，只能有一个主键，因此唯一键就是用来解决表中多个字段具有唯一性的问题。  
唯一键的本质与主键差不多，唯一键默认的允许字段为空，而且可以多个字段为空，因此空字段不参与唯一性的比较。  

增加唯一性：  
增加唯一性的方法与主键类型，有三种方法，分别为：  
第一种：在创建表的时候，字段后面之间添加unique或者unique key关键字  

实例：
``` SQL
create table my_unique (
    number char(10) unique comment '学号',
    name varchar(20) not null
) engine InnoDB charset utf8;
```

第二种：在所有字段之后，添加unique key(字段列表)，可以设置复合唯一键。  

实例：
``` SQL
create table my_unique2 (
    number char(10) not null,
    name varchar(10) not null,
    unique key(number)
) engine InnoDB charset utf8;
```
当唯一键又非空时，就和主键的性质一样了。  

第3种：在创建表之后，添加唯一键。  

实例：
``` SQL
create table my_unique3 (
    id int primary key auto_increment,
    number char(10) not null,
    name varchar(10) not null    
) engine InnoDB charset utf8;
```
``` SQL
alter table my_unique3 add unique key(number);
```

唯一性约束：唯一键与主键本质上相同，区别在于：唯一键允许字段值为空，并且允许多个字段空值存在。  

更新唯一键 & 删除唯一键  
在表中，更新唯一键的时候，可以不用先删除唯一键，因为表的唯一键允许有多个。  
删除唯一键的基本语法：  
``` SQL
alter table 表名 drop index 索引名字
```

实例：
``` SQL
alter table my_unique3 drop index number;
```
- - - - -
# 12、索引
索引：系统根据某种算法，单独建立一个文件，根据这个文件能够快速的匹配数据，加快数据搜索。  
索引的意义：
- 提高查询数据的效率
- 约束数据的有效性

MySQL中提供了多种索引，包括：
- 主键索引（primary key）
- 唯一键索引（unique key）
- 全文索引（fulltext index）
- 普通索引（index）

主键索引和唯一键索引，顾名思义就是在主键和唯一键字段上建立的索引，普通索引没有什么特色，就是为了加快数据查找。  
全文索引，即根据文章内部的关键字进行索引，其最大的难度就是在于如何确定关键字。对于英文来说，全文索引的建立相对容易，因为英文的两个单词之间有空格；但是对于中文来说，全文索引的建立就比较难啦，因为中文两个字之间不仅没有空格，而是还可以随意组合。  
- - - - -
# 13、关系
在数据库中，将实体与实体的关系反应到表的设计上来，可以分为三种，分别为：一对一（1：1），一对多（1：N）（或多对一（N：1））和多对多（N：N）。  
在此，所有的关系都是指表与表之间的关系。  

## 13.1 一对一
一对一，即一张表的一条记录只能与另一张表的一条记录想对应，反之亦然。  

实例：  
设计一张「个人信息表」，其字段包括：姓名、性别、年龄、身高、体重、籍贯、居住地等。  

| ID | 姓名 | 性别 | 年龄 | 身高 | 体重 | 籍贯 | 居住地 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | Juice | 男 | 18 | 182 | 72 | 中国 | 北京 | 
| 2 | Alice | 女 | 18 | 170 | 52 | 美国 | 西雅图 | 

如上表所示，但是有些数据是我们经常使用的，有些不经常使用，每次查询的时候都要查询所有数据，影响效率，可以将常用的数据和不常用的数据分为两个表，例如：  

表1：常用数据

| ID | 姓名 | 性别 | 年龄 | 
| --- | --- | --- | --- | 
| 1 | Juice | 男 | 18 | 
| 2 | Alice | 女 | 18 | 

表2：不常用数据

| ID | 身高 | 体重 | 籍贯 | 居住地 |
| --- | --- | --- | --- | --- |
| 1 | 182 | 72 | 中国 | 北京 | 
| 2 | 170 | 52 | 美国 | 西雅图 | 

如上面表2和表1所示，通过字段ID，表1中的一条记录只能匹配表2种的一条记录，反之亦然，这就是一对一的关系。  
- - - - -
## 13.2  一对多
一对多，即一张表中的记录可以对用另一张表中的多条记录，但是反过来，另一张表中的一条记录只能对应第一张表中的一条记录。  

实例：  
例如，设计「国家城市表」，其中包含两个实体，即国家和城市。  

表3：国家表

| COUNTRY_ID | 国家 | 位置 |
| --- | --- | --- |
| 1 | 中国 | 亚洲 |
| 2 | 美国 | 北美洲 |

表4：城市表
| CITY_ID | 城市 | 国家 |
| --- | --- | --- |
| 1 | 北京 | 中国 |
| 2 | 上海 | 中国 |
| 3 | 纽约 | 美国 |
| 4 | 华盛顿 | 美国 |

如上面表3和表4的关系，是一种典型的一对多的关系。

- - - - -
## 13.3 多对多
多对多，即一张表中的记录可以对应另一张表中的多条记录，反过来，另外一张表中的记录也可以对应第一张表中的多条记录。  

实例：  
例如，设计「教师学生表」，其中包含两个实体，即学生和老师。  

表5：教师表

| TEA_ID | 姓名 | 性别 |
| --- | --- | --- |
| 1 | 刘涛 | 女 |
| 2 | 胡歌 | 男 |
| 3 | 周杰伦 | 男 |

表6：学生表

| STU_ID | 姓名 | 性别 |
| --- | --- | --- |
| 1 | 张三 | 男 |
| 2 | 刘丽 | 女 |

表7：中间表

| ID | TEA_ID | STU_ID |
| --- | --- | --- |
| 1 | 1 | 1 |
| 2 | 1 | 2 |
| 3 | 2 | 1 |
| 3 | 3 | 2 |

表5和表6之间是多对多的关系，他们的关系是通过表7来维护的。
- - - - -
# 14、范式
范式：Normal Farmat，是为了解决数据存储和优化的问题。  
在数据存储之后，凡是能通过关系寻找出来的数据，坚决不再重复存储，范式的终极目标是减少数据冗余。  

范式是一种分层结果的规范，共6层，分别为1NF、2NF、3NF、4NF、5NF和6NF，每一层都比上一层严格，若要满足下一层范式，其前提条件是满足上一层范式。其中，1NF是最底层的范式，6NF为最高层的范式，也最为严格。  

MySQL数据库属于关系型数据库，其存储数据的时候有些浪费空间，但也致力于节省空间，这就与范式想解决的问题不谋而合，因此在设计数据库的时候，大多利用范式来指导设计。但是数据库不单要解决存储空间的问题，还要保证效率的问题，而范式只为解决存储空间的问题，所以数据库的设计又不能完全按照范式的要求来实现，因此在一般情况下，只需要满足前三种范式即可。  

此外，咱们需要知道：范式在数据库的设计中是有指导意义的，但不是强制规范。  

## 14.1 1NF
第一范式：在设计数据库的时候，如果表中设计的字段存储的数据，在取出来使用之前还需要额外的处理（拆分），那么表的设计就不满足第一范式，第一范式要求字段的数据具有原子性，不可再分。  

实例：  
例如，设计一个「学校假期表」，如下所示：  
表1：学校假期时间表  

| ID | 学校 | 起始时间，结束时间 |
| --- | --- | --- |
| 1 | 清华大学 | 20180711, 20180901 |
| 2 | 华中科技大学 | 20180804, 20180820 |

观察上表，咱们会发现表1的设计并没有什么问题，但是如果需求是查询各学校开始放假的日期呢？那显然上表的设计并不满足1NF，数据不具有原子性。对于此类问题，解决的方案就是将表1进行拆分：  

表2：拆分后的表1  

| ID | 学校 | 起始时间 | 结束时间 |
| --- | --- | --- | --- |
| 1 | 清华大学 | 20180711 | 20180901 |
| 2 | 华中科技大学 | 20180804 | 20180820 |

- - - - -
## 14.2 2NF
第二范式：在数据表的设计过程中，如果有复合主键（多字段主键），且表中字段并不是由主键来确定，而是依赖复合主键的某个字段（主键的部分），也就是说存在依赖主键的部分依赖，第二范式就是解决表设计中不存在出现部分依赖。  

实例：  
例如，设计一个「教室授课表」，如下所示：  

表3：教室授课表

| 教师| 性别 | 课程 | 地点 |
| --- | --- | --- | --- |
| 王伟 | 男 | 《如何追到心爱的女孩》 | 西12 |
| 李白 | 男 | 《唐诗三百首》 | 东9 |

观察上表，我们发现：教室不能作为主键，需要与授课地点相结合才能成作为主键，其中性别依赖于具体的老师，而课程依赖于授课地点，这就出现了表的字段依赖于部分主键的问题，从而导致不能满足第二范式。
- 解决方案1：将教师和性别，课程和授课地点，分成两张单独的表
- 解决方案2：取消复合主键，使用逻辑主键

这里我们选择方案2。  

| ID | 教师| 性别 | 课程 | 地点 |
| --- | --- | --- | --- | --- |
| 1 | 王伟 | 男 | 《如何追到心爱的女孩》 | 西12 |
| 2 | 李白 | 男 | 《唐诗三百首》 | 东9 |

- - - - -
## 14.3 3NF
第三范式：需要满足第一范式和第二范式，理论上讲，每张表中的所有字段都应该直接依赖主键（逻辑主键，代表是业务主键），如果表设计中存在一个字段，并不直接依赖主键，而是通过某个非主键字段依赖，最终实现主键依赖（把这种不是直接依赖主键，而是依赖非主键字段的依赖关系，称之为传递依赖），第三范式就是要解决表设计中出现传递依赖的问题。  

以上的添加逻辑主键的表3为例：  

| ID | 教师| 性别 | 课程 | 地点 |
| --- | --- | --- | --- | --- |
| 1 | 王伟 | 男 | 《如何追到心爱的女孩》 | 西12 |
| 2 | 李白 | 男 | 《唐诗三百首》 | 东9 |

在以上表的设计中，性别依赖教师，教师依赖主键；课程依赖授课地点，授课地点依赖主键，因此性别和课程都存在传递依赖的问题。  
- 解决方案：将存在传递依赖的字段，以及依赖的字段本身单独取出来，形成一个单独的表，然后在需要使用对应的信息的时候，把对应的实体表的主键添加进来。

表4：教室表

| TEA_ID | 教师| 性别 |
| --- | --- | --- |
| 1 | 王伟 | 男 | 
| 2 | 李白 | 男 | 

表5：授课地点表

| ADDRESS_ID | 课程 | 地点 |
| --- | --- | --- |
| 1 | 《如何追到心爱的女孩》 | 西12 |
| 2 | 《唐诗三百首》 | 东9 |

表6：进行处理后的表

| ID | TEA_ID | ADDRESS_ID |
| --- | --- | --- |
| 1 | 1 | 1 |
| 2 | 2 | 2 |
| 3 | 3 | 3 |

- - - - -
## 14.4 逆规范化
在某些特定的环境中（例如淘宝数据库），在设计表的时候，如果一张表中有几个字段是需要从另外的表中去获取数据，理论上讲，的确可以获得想要的数据，但是相对来说，其效率低会一点。此时为了提高查询效率，咱们会刻意的在某些表中，不去保存另外一张表的主键（逻辑主键），而是直接保存想要存储的数据信息，这样的话，在查询数据的时候，这张表就可以直接提供咱们想要的数据，而不需要多表查询，但是这样做会导致数据冗余。  

实际上，逆规范化是磁盘利用率和效率之间的对抗。
- - - - -
# 15、主键冲突
数据的操作，无外乎就是增删改查。  
在插入数据的时候，假设主键对用的值已经存在，则插入失败，这就是主键冲突。  

第一种情况：主键冲突，进行更新操作  
基本语法：
``` SQL
insert into 表名[(字段列表：包含主键)]  values(值列表) on duplicate  key update 字段 = 新值;
```

实例：
``` SQL
insert into my_class values('PM', 'B313') on duplicate key update room = 'B313'
```

第二种情况：主键冲突，选择替换操作  
基本语法：  
``` SQL
replace insert into 表名[(字段列表：包含主键)]  values(值列表);
```
实例：
``` SQL
insert into my_class values('PM', 'B313');
replace into my_class values('PM', 'B313');
```
- - - - -
# 16、蠕虫复制
蠕虫复制：从已有的表中获取数据，然后将数据进行新增操作，数据成倍（以指数形式）的增加。  
根据已有表创建表，即复制表结构，其基本语法为：  
``` SQL
create table 表名 like [数据库名.]表名;
```

实例：
``` SQL

mysql> create table my_copy like my_auto;
Query OK, 0 rows affected (0.01 sec)

mysql> desc my_copy;
+-------+-------------+------+-----+---------+----------------+
| Field | Type        | Null | Key | Default | Extra          |
+-------+-------------+------+-----+---------+----------------+
| id    | int(11)     | NO   | PRI | NULL    | auto_increment |
| name  | varchar(20) | NO   |     | NULL    |                |
+-------+-------------+------+-----+---------+----------------+
2 rows in set (0.00 sec)
```

蠕虫复制的步骤为：先查出数据，然后将查出的数据新增一遍。  
基本语法：
``` SQL
insert into 表名 select 字段列表/* from 表名;
```

实例：
``` SQL
mysql> insert into my_copy select * from my_auto;
Query OK, 3 rows affected (0.00 sec)
Records: 3  Duplicates: 0  Warnings: 0

mysql> select * from my_copy;
+----+--------+
| id | name   |
+----+--------+
|  1 | Harlon |
|  2 | Juice  |
|  3 | Ellie  |
+----+--------+
3 rows in set (0.00 sec)
```

蠕虫复制的效果：
``` SQL
mysql> insert into my_copy(name) select name from my_copy;
Query OK, 3 rows affected (0.01 sec)
Records: 3  Duplicates: 0  Warnings: 0

mysql> insert into my_copy(name) select name from my_copy;
Query OK, 6 rows affected (0.00 sec)
Records: 6  Duplicates: 0  Warnings: 0

mysql> insert into my_copy(name) select name from my_copy;
Query OK, 12 rows affected (0.00 sec)
Records: 12  Duplicates: 0  Warnings: 0

mysql> insert into my_copy(name) select name from my_copy;
Query OK, 24 rows affected (0.01 sec)
Records: 24  Duplicates: 0  Warnings: 0
```

蠕虫复制的意义：
- 从已有的数据表中拷贝数据到新的数据表
- 可以迅速的让表中的数据膨胀到一定的数量级，多用于测试表的压力及效率

- - - - -
# 17、数据库高级操作
## 17.1 更新数据
基本语法：
``` SQL
update 表名 set 字段 = 值 [where 条件]
```
高级语法：
``` SQL
update 表名 set 字段 = 值 [where 条件] [limit 更新数量]
```

实例：
``` SQL
mysql> update my_copy set name = 'Harlon2' where name = 'harlon' limit 3;
Query OK, 3 rows affected (0.00 sec)
Rows matched: 3  Changed: 3  Warnings: 0

mysql> select * from my_copy;
+----+---------+
| id | name    |
+----+---------+
|  1 | Harlon2 |
|  2 | Juice   |
|  3 | Ellie   |
|  4 | Harlon2 |
|  5 | Juice   |
|  6 | Ellie   |
|  7 | Harlon2 |
...
```
- - - - -
## 17.2 删除数据
``` SQL
delete from 表名 [where 条件]
```
高级语法：
``` SQL
delete from 表名 [where 条件] [limit 更新数量]
```

实例：
``` SQL
mysql> delete from my_copy where name = 'Harlon2' limit 2;
Query OK, 2 rows affected (0.00 sec)

mysql> select * from my_copy;
+----+---------+
| id | name    |
+----+---------+
|  2 | Juice   |
|  3 | Ellie   |
|  5 | Juice   |
|  6 | Ellie   |
|  7 | Harlon2 |
|  8 | Juice   |
...
```

删除表的数据，自增长不会还原，如果想要还原自增长属性，思路是：先删除表，然后重新建表。  
基本语法：
``` SQL
truncate 表名;
```
- - - - -
# 18、查询高级操作
基本语法：
``` SQL
select 字段列表/* from 表名 [where 条件]
```
完整语法：
``` SQL
select [select 选项] 字段列表[字段别名]/* from 数据源 [where条件]
[1] [2] [3]
```
- [1] = [group by 子句]
- [2] = [order by 子句]
- [3] = [limit 子句]
- - - - -
## 18.1 select 选项
select选项，即select对查出来的结果的处理方式。
- all：默认，保留所有的查询结果
- distinct：去重，将查出来的结果中所有字段相同的记录去除

实例：
``` SQL
select * from my_copy;
select all * from my_copy;
select distinct * from my_copy;
```
- - - - -
## 18.2 字段别名
字段别名，即当数据进行查询的时候，有时候字段的名字不一定满足需求（特别地，在多表查询的时候，很有可能会有同名字段），这就需要对字段进行重命名、取别名。  
基本语法：
``` SQL
字段名 as 别名;
```

实例：
``` SQL
select id name as n age as a grade as g from student;
```
- - - - -
## 18.3 数据源
数据源，即数据的来源，关系型数据库的数据源都是数据表，本质上只要保证数据类型二维表，最终就可以做为数据源。  
数据源分为3种，分别为：单表数据源，多表数据源和查询语句。  
第1种：单数据源  
基本语法：
``` SQL
select * from 表名;
```

第2种：多数据源  
基本语法：
``` SQL
select * from 表名1, 表名2
```

第3种：查询语句（子查询）  
基本语法：
``` SQL
select * from (select * from 表名) [as] 别名;
```
- - - - -
## 18.4 where子句
where子句：用来判断数据和筛选数据，返回的结果为0或者1，其中0代表false，1代表true，where是唯一一个直接从磁盘获取数据的时候就开始判断的条件，从磁盘中读取一条数据，就开始where判断，如果判断的结果为真，则保持，反之，不保存。  
判断条件：
- 比较运算符：>、<、>=、<=、<>、=、like、between and、in和not in
- 逻辑运算符：&&、||、和!

实例：
``` SQL
select * from student where id = 2 || id = 3 || id = 5;
select * from student where id in (2,3,5);
select * from student where if between 2 and 5;
```
- - - - -
## 18.5 group by 子句
group by 子句：根据表中的某个字段进行分组，即将含有相同字段值的记录放在一组，不同的放在不同组。  
基本语法：
``` SQL
group by 字段名;
```

实例：
``` SQL
select * from student group by sex;
```
分组的目标是为了（按分组字段）统计数据，并不是为了单纯为了方便统计数据，SQL提供了一些列的统计函数，例如：
- count()：统计分组后，每组的记录数；
- max()：统计每组中的最大值；
- min()：统计每组中的最小值；
- avg()：统计每组中的平均值；
- sum()：统计每组中的数据总和；

实例：
``` SQL
select sex,count(*),max(age),min(age),avg(age),sum(age) from student group by sex;
```
其中，count()函数可以使用两种参数，分为为：*表示统计组内全部记录的数量；字段名表示统计对应字段的非null（如果某条记录中该字段的值为null，则不统计）记录的总数。此外，使用group by进行分组之后，展示的记录会根据分组的字段值进行排序，默认为升序。当然，也可以人为的设置升序和降序。  
基本语法：
``` SQL
group by 字段名 [asc/desc]
```

实例：
``` SQL
select sex, count(*) from student group by sex;
select sex, count(*) from student group by sex asc;
select sex, count(*) from student group by sex desc;
```

多字段分组：
``` SQL
select *, count(*) from student group by grage, sex;
```
group_concat(字段名)可以对分组的结果中的某个字段值进行字符串链接，即保留该组某个字段的所有值，例如：
``` SQL
select sex, age, count(*), group_concat(name) from student group by sex;
```
回溯统计：利用with rollup关键字，可以在每次分组之后，根据当前分组的字段进行统计，并向上一级分组进行汇报，例如：
``` SQL
select sex, count(*) from student group by sex with rollup;
```
- - - - -
## 18.6 having 子句
having子句：与where子句一样，都是进行条件判断的，但是where是针对磁盘数据进入内存之后，会进行分组操作，分组结果就需要having来操作。思考可以，having能做where能做的几乎所有事情，但是where却不能做having能做的很多事情。  
第1点：分组统计的结果或者说统计函数只有having能够使用

实例：
``` SQL
select grage, count(*) from student group by grade having count(*) >= 2;
```

第2点：having能够使用字段别名，where则不能

实例：
``` SQL
select grage, count(*) as total from student group by grade having total >= 2;
```
- - - - -
## 18.7 order by子句
order by子句：根据某个字段进行升序或者降序排序，依赖校对集。  
基本语法：
``` SQL
order by 字段 asc/desc
```
其中，asc为升序，desc为降序。

实例：
``` SQL
select * from student order by age;
```
多字段排序，即先根据某个字段进行排序，然后在排序后的结果中，再根据某个字段进行排序。  

实例：
``` SQL
select * from student order by age, grade desc;
```
- - - - -
18.8 limit子句
limit子句：是一种限制结果的语句，通常来限制结果的数量。  
基本语法：
``` SQL
limit [offset] length;
```
其中，offset为起始值，length为长度。  
第1种，只用来限制长度（数据量）  
实例：
``` SQL
select * from student;
select * from student limit 3;
```
第2种：限制起始值，限制长度（数据量）  
实例：
``` SQL
select * from student limit 0,2
select * from student limit 2,2
```
第3种：主要用来实现数据的分页，目的是为了节省时间，提高服务器的响应效率，减少资源的浪费。  
- - - - -
# 19、连接查询
连接查询：将多张表（大于等于2张表）按照某个指定的条件进行数据的拼接，其最终结果记录数可能有变化，但字段一定会增加。  
连接查询的意义：在用户查询的时候，需要显示的数据来自多张表。  
连接查询为join，使用方式为：左表 join 右表  
- 左表：join 左表的表
- 右表：join 右边的表

连接查询分类：在SQL中将连接查询分为四类：分别为内连接、外链接、自然连接和交叉连接。  
## 19.1 交叉连接
交叉连接：cross join，从一张表中循环取出每条记录，每条记录都去另外一张表进行匹配，匹配的结果都保留（没有条件匹配），而连接本身的字段会增加，最终形成的结果为笛卡尔积形式。  
基本语法：
``` SQL
左表 cross join 右表;
```
其结果与多表查询相同。
实例：
``` SQL
select * from student cross join class;
select * from student, class;
```
实际上，笛卡尔积形式（交叉连接和多表查询）的结果并没有什么实际意义，应该尽量避免，其存在的价值就是保证连接这种结构的完整性。
- - - - -
## 19.2 内连接
内连接：inner join，从左表中取出每一条记录，和右表中的所有记录进行匹配，仅当某个条件在左表和右表的值相同时，结果才会保留，否则不保留。  
基本语法：
``` SQL
左表 [inner] join 右表 on 左表.字段 = 右表.字段;
```
其中，关键字on表示连接条件，两表中的条件字段有着相同的业务含义。  
实例：
``` SQL
select * from student inner join class on student.grade = class.grade;
select * from student  join class on student.grade = class.grade;
```
注意：
如果两表中有某个表的条件字段名唯一，那么在书写连接条件的时候，可以省略表名，直接书写字段名，MySQL 会自动识别唯一字段名，但不建议这么做。此外，咱们会发现，在上面的结果中有同名字段，这会给咱们理解数据的意义造成一定的困扰，这时就需要使用字段别名和表别名做区别啦！  
实例：
``` SQL
select s.*, c.id as c_id, c.grade as c_grade, room from student as s inner join class as c on s.grade = c.grade;
```
最后，内连接可以可以没有连接条件，即可以没有on及之后的内容，这时内连接的结果全部保留，与交叉连接的结果完全相同。而且在内连接的时候可以使用where关键字代替on，但不建议这么做，因为where没有on的效率高。
- - - - -
## 19.3 外链接
外链接：`left\right join`，以某张表为主表，取出里面的所有记录，然后让主表中的每条记录都与另外一张表进行连接，不管是否匹配成功，其最终结果都会保留，匹配成功，则正确保留；匹配失败，则将另一张表的字段都置为`NULL`。  
基本语法：
``` SQL
左表 left\right join 右表 on 左表.字段 = 右表.字段
```
其中，`on`表示连接条件，两表的字段有着相同的含义。在这里，以主表为依据，外连接分为两种，分别为：
- `left join`：左外连接（左连接），以左表为主表；
- `right join`：右外连接（右连接），以右表为主表；

实例：
``` SQL
select s.*, c.id as c_id, c.grade as c_grade, room from student as s left join class as c on s.grade = c.grade;
select s.*, c.id sd c_id, c.grade as c_grade, room from student as s right join class as c on s.grade = c.grade;
```
实际上，无论以那张表为主表，其外连接的结果（记录数量）都不会少于主表的记录总数。此外，虽然左连接与右连接有主表差异，但显示的结果都是：左表的数据在左边，右表的数据在右边。
- - - - -
## 19.4 自然连接
自然连接：`nature join`，自然连接其实就是自动匹配连接条件，系统以两表中同名字段作为匹配条件，如果两表有多个同名字段，那就都作为匹配条件。在这里，自然连接可以分为自然内连接和自然外连接。  

自然内连接：  
基本语法：  
``` SQL
左表 + natural + join + 右表;
```

实例：
``` SQL
select * from student natural join class;
```
自然连接自动使用同名字段作为连接条件，而且在连接完成之后合并同名字段。  

自然外连接：
基本语法：
``` SQL
左表 natural left/right join 右表
```

实例：
``` SQL
select * from student natural left join class;
select * from student natural right join class;
```
实际上，自然连接并不常用。而且，咱们可以用内连接和外连接来模拟自然连接，模拟的关键就在于使用同名字段作为连接条件及合并同名字段。  
基本语法：
``` SQL
左表 inner/left/right join 右表 using(字段名);
```

实例：
``` SQL
select * from student natural left join class;
select * from student left join class using(id, grade);
```
- - - - -
# 20、外键
外键：`foreign key`，外面的键，即不在自己表中的键。如果一张表中的有一个非主键的字段指向另外一张表的主键，那么该字段称之为主键。每张表中，可有有多个主键。  

## 20.1 外键操作
新增主键：  
主键即可以再创建表的时候增加，也可以在创建之后增加（但是要考虑数据的问题）。  
第1种：在创建表的时候，增加外键。  
基本语法：  
``` SQL
foreign key(外键字段) references 外部表名(主键字段);
```

实例：
``` SQL
create table my_foreign1(
    id int primary key auto_increment,
    name varchar(20) not null comment '学生姓名',
    c_id int comment '班级表ID',
    foreign key(c_id) references my_class(id)
) engine InnoDB charset utf8;
```
``` SQL
mysql> desc my_foreign1;
+-------+-------------+------+-----+---------+----------------+
| Field | Type        | Null | Key | Default | Extra          |
+-------+-------------+------+-----+---------+----------------+
| id    | int(11)     | NO   | PRI | NULL    | auto_increment |
| name  | varchar(20) | NO   |     | NULL    |                |
| c_id  | int(11)     | YES  | MUL | NULL    |                |
+-------+-------------+------+-----+---------+----------------+
3 rows in set (0.00 sec)

```
`c_id`的`key`显示为`MUL`，表示多个键的意思。这是因为外键要求字段本身是一个索引（普通索引）如果字段本身没有索引，外键就会先创建一个索引，然后才创建外键本身。  

第2中：在创建表之后，增加外键  
基本语法：  
``` SQL
alter table 表名 add[constraint 外键名字] foreign key(外键字段) + references 外键表名(主键字段);
```

实例：
``` SQL
create table my_foreign2 (
    id int primary key auto_increment,
    name varchar(20) not null comment '学生姓名',
    c_id int comment '班级表ID'
) engine InnoDB charset utf8;

alter table my_foreign add constraint test_foreign foreign key(c_id) references my_class(id);
```

修改外键 & 删除外键  
外键不能修改，只能先删除后增加。  
基本语法：
``` SQL
alter table 表名 drop foreign key 外键名字;
```

实例：
``` SQL
alter table my_foreign2 drop foreign key test_foreign;
```
- - - - -
## 20.2 外键作用
首先，给出父表和子表的定义：
- 父表：指外键所指向的表；
- 子表：指相对于父表，拥有外键的表；
外键默认的作用有两个，分别对子表和父表进行约束。  
第1种：约束子表  
在子表进行数据的写操作（增和改）的时候，如果对应的外键字段在父表中找不到对用的匹配，那么操作会失败。

实例：
``` SQL
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'ls' at line 1
mysql> insert into my_foreign1 values(null, 'Harlon', 1);
ERROR 1452 (23000): Cannot add or update a child row: a foreign key constraint fails (`test`.`my_foreign1`, CONSTRAINT `test_foreign` FOREIGN KEY (`c_id`) REFERENCES `my_class` (`id`))
mysql> insert into my_class values(null, 'class-1', 'A301');
Query OK, 1 row affected (0.00 sec)

mysql> insert into my_foreign1 values(null, 'Harlon', 1);
Query OK, 1 row affected (0.01 sec)
```

第2中：约束父表
在父表进行数据的写操作（删和改，且涉及主键）的时候，如果对应的主键在子表中已经被数据引用，那么操作就会失败。  

实例：
``` SQL
update my_class set id = 5 where id = 1;
```
- - - - -
## 20.3 外键条件
在我们使用外键的时候，应该遵循如下条件：
- 外键要存在，首先必须保证表的引擎是InnoDB（默认的存储引擎），如果不是InnoDB存储引擎，那么主键可以创建成功，但没有约束作用；
- 外键的字段的字段类型（列类型），必须与父表的主键类型完全一致；
- 每张表中的外键名称不能重复；
- 增加外键的字段，如果数据已经存在，那么要要求数据与父表中的主键对应；

- - - - -
## 20.4 外键约束
所谓的外键约束，就是指外键的作用。之前所讲的外键的作用都是默认的作用，实际上，可以通过对外键的需求，进行定制操作。  
外键约束有三种模式，分别为：
- `distrinct`：严格模式（默认），父表不能删除或更新一个已经被子表数据所引用的记录
- `cascade`：级联模式，父表的操作，对应父表关联的数据也跟着删除
- `set null`：置空模式，父表的操作之后，子表对用的数据（外键字段）被置空

基本语法：
``` SQL
foreign key(外键字段) references 父表(主键字段) [on delete 模式 on update 模式];
```
通常一个合理的做法（约束模式）是：删除的时候，子表被置空；更新的时候，子表进行级联操作。

实例：
``` SQL
create table my_foreign4 (
    id int primary key auto_increment,
    name varchar(20) not null,
    c_id int,
    foreign key(c_id) references my_class(id) on delete set null on update cascade
) engine InnoDB charset utf8;
```
外键的功能十分强大，但是在开发过程中，由于外键的存在，使得开发变得困难不可控，所以一般都不使用外键。
- - - - -
# 21、联合查询
联合查询：`union`，将多次查询（多条select语句）的结果，在字段数相同的情况下，在记录的层次上进行拼接。  
基本语法：  
联合查询由多条`select`语句构成，每条`select`语句获取的字段数相同，但与字段类型无关。    
基本语法：  
``` SQL
select 语句1 union [union选项] select 语句2;
```

实例：
``` SQL
mysql> select * from my_class union distinct select * from my_class;
+----+---------+------+
| id | grade   | room |
+----+---------+------+
|  1 | class-1 | A301 |
+----+---------+------+
1 row in set (0.00 sec)

mysql> select * from my_class union all select * from my_class;
+----+---------+------+
| id | grade   | room |
+----+---------+------+
|  1 | class-1 | A301 |
|  1 | class-1 | A301 |
+----+---------+------+

```

联合查询只要求字段数相同，而跟类型无关。执行如下`SQL`语句，实例：  
``` SQL
select id, grade, room from my_class union distinct select name, grade, id from Student;
```

意义：  
- 查询同一张表，例如查询学生信息，要求男孩按年龄升序排序，女生按年龄降序排序
- 多表查询，多张表的结构是完全一样的，保持的数据结构也是一样的

此外，如果数据量非常的大，就要进行分表（垂直分表和水平分表），而分表的依据无外乎数据多不多和常不常用。  

- - - - -
# 22、子查询
子查询：`sub query `，查询时在某个查询结果上进行的，一条select语句内部包含了另外一条select语句。  

分类：  
子查询有两种分类方式，分别为：按结果分类和位置分类。  
按结果分类，即根据子查询得到的数据进行分类（理论上，任何一个查询结果都可以理解为一个二维表），分别为：
- 标量子查询：子查询得到的结果是一行一列，出现的位置在`where`之后
- 列子查询：子查询得到的结果是一行多列，出现的位置在`where`之后
- 行子查询：子查询得到的结果是多行一列（多行多列），出现的位置在`where`之后
- 表子查询：子查询得到的结果是多行多列，出现的位置在`from`之后。

按位置分类，即根据子查询（`select`语句）在外部查询（`select`语句）中出现的位置进行分类，分别为：
- `from`子查询：子查询出现在`from`之后
- `where`子查询：子查询出现在`where`条件之后
- `exists`子查询：子查询出现在`exists`里面

## 22.1 标量子查询
需求：知道班级号，想要获取该班的全部学生。  
思路：  
- 先确定数据源，学生表
``` SQL
select * from student where c_id = ?;
```
- 然后获取班级ID，通过班级表来确定
``` SQL
select id from class where grade = "class-1";
```
- 合并
``` SQL
select * from student where c_id = (select id from class where grade = 'class-1');
```

## 22.2 列子查询
需求：查询所有在读班级（学生表存在的班级）的学生。  
思路：  
- 先确定数据源，学生表
``` SQL
select * from student where c_id in ?;
```
- 然后确定全部有效的班级ID
``` SQL
select id from class;
```
- 合并：
``` SQL
select * from student where c_id in (select id from class);
```

在列子查询的结果为一行多列时，我们需要使用`in`作为条件来进行匹配；此外，在MySQL中还有三个类似的条件，分别为：`all`、`some`和`any`。
- `any`等价于`in`，表示其中一个；
- `any`等价于`some`，而`any`和`some`用于否定时却有些区别
- `all`表示等于全部

值得注意的是，在我们使用上面三个关键字中任何一个的时候，都需要搭配`=`使用，例如：
``` SQL
select * from student where c_id = any (select id from class);
select * from student where c_id = some (select id from class);
select * from student where c_id = all (select id from class);
```
否定用法：
``` SQL
select * from student where c_id != any (select id from class);
select * from student where c_id != some (select id from class);
select * from student where c_id != all (select id from class);
```
- - - - -
## 22.3 行子查询
行子查询，返回的结果可以是一行多列或者多列多行。  
需求：查询学生表中，年龄最大且身高最高的学生。  
思路：  
- 先确定数据源，学生表
``` SQL
select * from student where age = ? and height = ?;
```
- 然后确定最大年龄和最大身高
``` SQL
select max(age), max(height) from student;
```
- 合并
``` SQL
select * from student where (age, height) = (select max(age), max(height) from student);
```
- - - - -
## 22.4 表子查询
表子查询，返回的结果是多行多列二维表（将子查询的结果当做二维表来使用），实际上查询的返回结果都可以称之为二维表。  
需求：找出每个班身高最高的学生。  
思路：  
- 先确定数据源，将学生按身高进行降序排序
``` SQL
select * from student order by height desc;
```
- 从每个班级选出第一个学生
``` SQL
select * from student group by c_id;
```
- 合并
``` SQL
select * from (select * from student order by height desc) as student group by c_id;
```
- - - - -
## 22.5 exists子查询
`exists`：表示是否存在的意思，因此`exists`子查询就是用来判断某些条件是否满足（跨表），`exists`是接在`where`之后，其返回的结果为`1`或`0`，满足条件为`1`，反之为`0`。  
需求：在班级存在的前提下，查询所有的学生。  
思路：  
- 先确定数据源：
``` SQL
select * from student where ?;
```
- 然后确定条件是否满足
``` SQL
exists(select * from class);
```
- 合并：
``` SQL
select * from student where exists(select * from class);

select * from student where exists(select * from class where id  = 3);

select * from student where exists(select * from class where id = 100);
```

- - - - -
# 23、视图
视图：view，是一种有结构（有行有列），但没有结果（结构中不真实存在数据）的虚拟表，虚拟表的结构来源不是自己定义的，而是从对应的基表（视图的数据来源）中产生的。
## 23.1 创建视图
首先，给出创建视图的基本语法：  
基本语法：  
``` SQL
create view 视图名 as select 语句;
```
其中，select语句可以使普通查询，也可以是连接查询、联合查询、子查询等。  
此外，视图根据数据的来源，可以分为单表视图和多表视图：  
- 单表视图：基表只有一个
- 多表视图：基表至少两个

实例：
``` SQL
-- 单表视图
create view my_v1 as select * from student;
create view my_v2 as select * from my_class;

-- 多表视图
create view my_v3 as select s.*, c.grade, c.room from student as s left join my_class c on s._cid = c.id;
```
- - - - -
## 23.2 查询视图
这里的查询视图是指查看视图的结构，而不是查看视图的结果。  
由于视图是一张虚拟表，因此标的所有查询语句，都使用于视图，例如：  
``` SQL
desc 视图名;
show create table 视图名;
show create view 视图名;
```
此外，视图一旦创建，系统就会在视图对用的数据库文件夹下创建一个对应的frm结构文件，以保证结构的完整性。
- - - - -
## 23.3 使用视图
在操作数据库表的过程中，使用视图，主要就是为了查询，因此将视图当做表一样查询即可。  
在这里需要注意的是，虽然我们说视图是一个虚拟表，它不保存数据，但是它却可以获取数据。  

实例：
``` SQL
select * from my_v1;
select * from my_v2;
select * from my_v3;
```
我们查询视图的结果和查询创建视图时as后面连接的select语句的结果完全相同。
因此，我们也可以认为：创建视图，就是给一条select语句起别名，或者说是封装select语句。
- - - - -
## 23.4 修改视图
视图本身不可修改，但是视图的来源（select）语句是可以修改的。因此，修改视图，就是修改视图的来源（select）语句。  
基本语法：
``` SQL
alter view 视图名 as 新的select语句;
```

实例：
``` SQL
alter view my_v1 as select id, name, gender, age, c_id from student;
```
- - - - -
## 23.5 删除视图
基本语法：  
``` SQL
drop view 视图名;
```
- - - - -
## 23.6 视图意义
- 视图可以节省SQL语句，将一条负责的查询语句来进行分装，以后可以直接对视图进行操作
- 数据安全，视图操作主要是针对查询的，如果对视图结构进行处理，例如删除，并不会影响基表的数据
- 视图往往在大项目中使用，而且是多系统使用，可以对外提供有用的数据，但是隐藏关键（或无用）的数据
- 视图是对外提供友好型的，不同的视图提供不同额数据，就如专门对外设计的一样
- 视图可以更好（或者说，容易）进行权限控制
- - - - -
# 24、视图数据操作
视图数据操作：虽然我们说视图可以称之为select语句的别名，实际上，它和别名不一样，因为视图是可以进行数据写操作的，只不多有很多限制而已。
- - - - -
## 24.1 新增数据
在这里，新增数据就是指通过视图直接对基表进行数据的新增操作。  
- 限制1：多表视图不能进行新增操作
- 限制2：可以向单表视图新增数据，但视图中包含的字段必须有基表中所有不能为空的字段
- - - - -
## 24.2 删除数据
与新增数据类似：
- 多表不能删除数据
- 单表数据可以删除数据
- - - - -
## 24.3 更新数据
理论上，无论多表视图还是单表视图，都可以进行数据的更新。  
此外，更新数据并不总是成功的，这是因为有更新限制的存在。  
更新限制：with check option，如果创建视图的时候，设置了某个字段的限制，那么对视图进行更新操作的时候，系统就会进行验证，要保证更新之后，数据依然可以被查出来，否则不让更新。

实例：
``` SQL
create view my_v4 as select * from student where height > 170 with check option;
update my_v4 set height = 165 where id = 6;
```
- - - - -
## 24.4 视图算法
视图算发，即系统对视图以及外部查询视图的select语句的一种解析方式，视图算法有三种，分别为：  
- underfined：未定义（默认的），这不是一种实际使用的算法，而是一个“推卸责任”的算法。在未定义的情况下，告诉系统，视图没有定义算法，请自己选择
- template：临时表算法，系统先执行视图的select语句，后执行外部查询语句
- merger：合并算法，系统先将视图对用的select语句与外部查询视图的select语句进行合并，然后再执行。此算法比较高效，且在未定义算法的时候，经常会默认选择此算法。
指定视图算法，基本语法：
``` SQL
create [algorithm = template/merge/underfined] view 视图名 as select 语句;
```
- - - - -
# 25、数据备份与还原
基础概念：
- 备份：将当前已有的数据或记录存一份
- 还原：将数据恢复到备份时的状态
为什么要进行数据备份与还原：  
- 防止数据丢失
- 保护数据记录
数据备份与还原的方式有很多，具体可以分为：数据表备份、单表数据备份，SQL备份和增量备份。
## 25.1 数据表备份
数据表备份，不需要通过 SQL 来备份，我们可以直接进入到数据库文件夹复制对应的表结构以及数据；在需要还原数据的时候，直接将备份（复制）的内容放回去即可。  
不过想要进行数据表备份是有前提条件的，因为不同的存储引擎之间是有区别的。  
对于存储引擎，MySQL 主要使用两种，分别为：InnoDB 和 Myisam，两者均免费。  

| 特点 | MyISAM | InnoDB | BDB | Memory | Archive |
| --- | --- | --- | --- | --- | --- |
| 批量插入的速度 | 搞 | 低 | 高 | 高 | 非常高 |
| 事务安全 | —— | 支持 | 支持 | —— | —— |
| 全文索引 | 支持 | 5.5版本支持 | —— | —— | —— |
| 锁机制 | 表锁 | 行锁 | 页锁 | 表锁 | 行锁 |
| 存储限制 | 没有 | 64TB | 没有 | 有 | 没有 |
| B树索引 | 支持 | 支持 | 支持 | 支持 | —— |
| 哈希索引 | —— | 支持 | —— | 支持 | —— |
| 集群索引 | —— | 支持 | —— | —— | —— |
| 数据索引 | —— | 支持 | —— | 支持 | —— |
| 索引缓存 | 支持 | 支持 | —— | 支持 | —— |
| 数据可压缩 | 支持 | —— | —— | —— | 支持 |
| 空间使用 | 低 | 高 | 低 | N/A | 非常低 |
| 内存使用 | 低 | 高 | 低 | 中等 | 低 |
| 外键支持 | —— | 支持 | —— | —— | —— |

其中，MyISAM和InnoDB的数据存储方式也有所区别：
- MyISAM：表、索引和数据全部分开存储
- InnoDB：只有表结构，数据全部存储在ibd文件中

在linux上，MySQL文件默认存储在/var/lib/mysql中，例如：  
``` shell
[root@bigdata4 test]# ls
db.opt        my_class.ibd  my_date.ibd     my_default.ibd  my_float.ibd     my_foreign2.ibd  my_foreign4.frm  my_int.frm   my_pri3.frm  my_set.frm      my_unique3.frm  my_v1.frm
my_auto.frm   my_copy.frm   my_decimal.frm  my_enum.frm     my_foreign1.frm  my_foreign3.frm  my_foreign4.ibd  my_int.ibd   my_pri3.ibd  my_set.ibd      my_unique3.ibd  my_v2.frm
my_auto.ibd   my_copy.ibd   my_decimal.ibd  my_enum.ibd     my_foreign1.ibd  my_foreign3.MYD  my_friend.frm    my_pri2.frm  my_pri.frm   my_unique2.frm  my_unique.frm   Student.frm
my_class.frm  my_date.frm   my_default.frm  my_float.frm    my_foreign2.frm  my_foreign3.MYI  my_friend.ibd    my_pri2.ibd  my_pri.ibd   my_unique2.ibd  my_unique.ibd   Student.ibd
```
其中：
- \*.frm：存储表的结构
- \*.MYD：存储表的数据
- \*.MYI：存储表的索引

在这里，有一点需要我们注意，那就是：我们可以将通过 InnoDB 存储引擎产生的.frm和.idb文件复制到另一个数据库，也可以通过show tables命令查看复制过来的表名称，但是却无法获得数据。  
- - - - -
## 25.2 单数据表备份
单数据表备份，每次只能备份一张表，而且只能备份数据，不能备份表结构。  
通常的使用场景：将表中的数据导出到文件。  
备份方法：  
``` SQL
select */字段列表 into outfile '文件存储路径' from 数据源;
select */字段列表 from 数据源 into outfile '文件存储路径';
```
在这里，使用单表数据备份有一个前提，那就是：导出的外部文件不存在，即文件存储路径下的文件不存在。  

实例：
``` SQL
select * into outfile '/home/class.txt' from my_class;
```

单表数据备份的高级操作，即自己指定字段和行的处理方式。  
基本语法：  
``` SQL
select */字段列表 into outfile  '文件存储路径' fields 字段处理 lines 行处理 from 数据源;
```
字段处理：
- enclosed by：指定字段用什么内容包括，模式是空字符串
- terminated by：指定字段以什么技术，默认是\t
- escaped by：指定特殊符号用什么方式处理，默认是\\

行处理：
- starting by：指定每行以什么开始，默认是空字符串
- terminated by：指定每行以什么结束，默认是\r\n

实例：
``` SQL
select * into outfile '/home/class.txt' fields enclosed by '"' terminated by ' | ' lines starting by 'START: ' from my_class; 
```
恢复数据，基本语法：
``` SQL
load data infile '文件路径' into table 表名 字段列表 fields 字段处理 lines 行处理;
```
- - - - -
## 25.3 SQL备份
SQL备份，备份的是SQL语句，进行SQL备份的时候，系统会对表结构以及数据进行处理，变成相应的SQL语句，然后执行备份，在还原的时候，只要执行备份的SQL语句即可，此种备份方式主要是针对表结构。  
不过，MySQL并没有提供SQL备份的指令，如果我们想要进行SQL备份，则需要利用MySQL提供的软件mysqldump。  
基本语法：  
``` shell
mysqldump -hPup 数据库名字 [表名1, [表名2] > 备份文件目录
```
其中，-hPup分别为：
- h：IP或者localhost
- P：端口号
- u：用户名
- p：密码

实例：
``` shell
mysqldump -uroot -p123456 test class > class.sql
```
还原数据，基本语法：  
方法1：使用mysql还原数据
``` shell
mysql -hPup 数据库名称 [表名1 [表名2]] < 备份目录
```

实例：
``` shell
mysql -uroot -p123456 test < class.sql
```

方法2：使用SQL命令还原数据  
基本语法：  
``` SQL
source 备份文件目录;
```

实例：
``` SQL
source /home/class.sql
```
SQL备份的优缺点：
- 优点：可以备份表结构
- 缺点：增加额外的SQL命令，会浪费磁盘空间
- - - - -
## 25.4 增量备份
增量备份，不是针对数据或者 SQL 进行备份，而是针对 MySQL 服务器的日志进行备份，其日志内容包括了我们对数据库的各种操作的历史记录，如增删改查等。此外，增量备份是指定时间段进行备份，因此备份的数据一般不会出现重复的情况，常用于大型项目的数据备份。
- - - - -
# 26、事务
事务：一系列将要发生或正在发生的连续操作。  
事务安全：是一种保护连续操作同时实现（完成）的机制，事务安全的意义就是，保证数据操作的完整性。  
创建银行账户并插入数据：
``` SQL
create table bank_account(
    id int primary key auto_increment,
    cardno varchar(16) not null unique comment 'bank card number',
    name varchar(20) not null,
    money decimal(10, 2) default  0.0 comment 'account balance'
) engine InnoDB charset utf8;
insert into bank_account values
(null, '0000000000000001', 'Harlon', 8000),
(null, '0000000000000002', 'Jack', 5000);
```
## 26.1 事务操作
事务操作，分为两种：自动事务，手动事务。  
以银行的余额增减为例： 
第1步，开启事务，告诉系统一下所有操作，不要直接写入数据，先保存到事务日志。  
基本语法：  
``` SQL
start transaction;
```
第2不，减少Harlon账户的余额
``` SQL
update bank_account set money = money - 1000 where id = 1;
select * from bank_account;
```
由于我们开启了事务操作，数据库中真实的数据，并没有同步更新，而是先写入事务日志。  
第3步：增加Jack账户的余额  
``` SQL
update bank_account set money = money + 1000 where id = 2;
select * from bank_account;
```
第4步：提交事务或回滚事务
- 提交事务：commit
- 回滚事务：rollback

如果我们选择提交事务，则将事务日志存储的记录直接更新到数据库，并清除事务日志；如果我们选择回滚事务，则直接将事务日志清除，所有在开启事务至回滚事务之间的操作失效，保持原有的数据库记录不变。在这里，我们以提交事务为例：
``` SQL
commit;
select * from bank_account;
```
目前，只有InnoDB支持事务操作。

- - - - -
## 26.2 事务原理
事务原理：在事务开启之后，所有的操作都会被临时存储到事务日志，事务日志只有在收到commit命令之后，才会将操作同步到数据表，其他任何情况下都会清空事务日志，例如突然断开连接、收到rollback命令等。  
接下来，简单分析一下MySQL的操作过程：  
- Step1：客户端与服务端建立连接，同时开启一个临时的事务日志，此事务日志只作用于当前用户的当次连接；
- Step2：在客户端用 SQL 语句执行写操作，客户端收到 SQL 语句，执行，将结果直接写入到数据表，并将数据表同步到数据库；
- Step3：我们在客户端开启事务，则服务端原来的操作机制被改变，后续所有操作都会被先写入到临时日志文件；
- Step4：在客户端执行 SQL 语句（例如写操作），服务端收到 SQL 语句，执行，将结果写入到临时日志文件，并不将结果同步到数据库；
- Step5：在客户端执行查询操作，服务端直接从临时日志文件中捞取数据，返回给客户端；
- Step6：在客户端执行commit或者rollback命令，清空临时日志文件，如果是commit命令，则将结果同步到数据库；如果是rollback命令，则不同步。

- - - - -
## 26.3 回滚点
回滚点：在某个操作成功完成之后，后续的操作有可能成功也有可能失败，但无论后续操作的结果如何，前一次操作都已经成功，因此我们可以在当前成功的位置，设置一个操作点，其可以供后续操作返回该位置，而不是返回所有操作，这个点称之为回滚点。关于回滚点的基本语法为：
- 设置回滚点：savepoint 回滚点名称
- 返回回滚点：rollback to 回滚点名称

实例：
``` SQL
select * from bank_account;
start transaction;
-- 发工资
update bank_account set money = money + 10000 where id = 1;
savepoint spone;
-- 扣税，错误
update bank_account set money = money - 10000 * 0.05 where id = 2;
select * from bank_account;
rollback to spone;
-- 扣税，成功
update bank_account set money = money - 10000 * 0.05 where id = 1;
select * from bank_account;
commit;
```
- - - - -
## 26.4 自动事务
在 MySQL 中，默认的都是自动事务处理，即用户在操作完成之后，其操作结果会立即被同步到数据库中。  
自动事务是通过autocommit变量控制的，我们可以通过如下SQL语句，进行查看：
``` SQL
show variables like 'autocommit';
```
- 开启自动事务处理：set autocommit = on / 1;
- 关闭自动事务处理：set autocommit = off / 0;

- - - - -
## 26.5 事务特性
事务的特性，可以概括为ACID，具体为：  
- 原子性：Atomic，表示事务的整个操作都是一个整体，不可分割，要么全部成功，要么全部失败
- 一致性：Consistency，表示事务操作的前后，数据表中的数据处于一致状态
- 隔离性：Isolation，表示不同的事务操作之间是互相隔离的，互不影响
- 持久性：Durability，表示事务一旦提交，将不可修改，永久性的改变数据表中的数据

- - - - -
# 27、数据库变量
在MySQL数据库中，变量有两种，分别为：系统变量和自定义变量。  
根据变量的作用范围，又分为：  
- 会话级别变量：仅对当前客户端当次连接有效
- 全局级别变量：对所有客户端的任一次连接有效
## 27.1 系统变量
系统变量，顾名思义，是系统设置好的变量（皆为全局级别变量），也是用来控制服务器表现的，如autocommit、wait_timeout等。  
大多数的时候，我们并不需要使用系统变量，但我们仍然需要了解有这么回事，在必须要的时候，它可以帮助我们完成特殊的需求。  
查看系统变量，语法为：  
``` SQL
show variables;
```
查看具体的系统变量的值，语法为：
``` SQL
select @@变量名 [, @@变量名2];
```
实例：
``` SQL
mysql> select @@autocommit, @@version, @@version_compile_os, @@wait_timeout;
+--------------+-----------+----------------------+----------------+
| @@autocommit | @@version | @@version_compile_os | @@wait_timeout |
+--------------+-----------+----------------------+----------------+
|            1 | 5.6.39    | Linux                |          28800 |
+--------------+-----------+----------------------+----------------+
```
修改会话级别变量，有两种方法，语法分别为：
- 基本语法1：set 变量名 = 值
- 基本语法2：set @@变量名= 值

对于修改全局级别变量，语法为：
- 基本语法：set global 变量名= 值
- - - - -
## 27.2 自定义变量
自定义变量，顾名思义，是用户自定义的变量，并且都是会话级别的变量。  
系统为了区别系统变量与自定义变量，规定用户自定义的变量必须使用一个@符号，设置子定义变量的语法为：
- 基本语法： set @变量名 = 值;

实例：
``` SQL
mysql> set @name = 'harlon';
Query OK, 0 rows affected (0.00 sec)

mysql> select @name;
+--------+
| @name  |
+--------+
| harlon |
+--------+
1 row in set (0.00 sec)
```
注意：在 MySQL 中，很多地方会默认将=处理为比较符号，因此 MySQL 还提供了另外一种赋值符号:=，即冒号与等号拼接而成的符号。  
此外，MySQL允许我们从数据表中获取数据，然后直接赋值给变量，共两种方式：
第1种：边复制，边查看结果。语法为：
``` SQL
select @变量名 := 字段名 from 表名;
```

实例：
``` SQL
select @name = name from student;
select @name;
```

第2种：只赋值，不查看结果。语法为：
``` SQL
select 字段列表 from 表名 into 变量列表;
```

实例：
``` SQL
select name from student where id = 2 into @name;
select @name;
select * from student;
```
注意：自定义变量都是会话级别，只要是当前用户当次连接，都会受到影响，不区分数据库。
- - - - -
# 28、触发器
触发器：trigger，是指实现为某张表绑定一段代码，当表中的某些内容发生变化（增、删、改）的时候，系统会自动触发代码执行。  
触发器包含三个要素，分别为：
- 事件类型：增删改，即insert、delete和update
- 触发时间：事件类型前和后，即before和after
- 触发对象：表中的每一套记录（行），即整张表

每张表只能拥有一种触发时间和一种事件类型的触发器，即每张表最多可以拥有6种触发器。
## 28.1 创建触发器
``` SQL
delimiter 自定义符号  
create trigger 触发器名称 触发器时间 事件类型 on 表名 for each row  
begin  
触发器内容主体，每行用分号结尾  
end  
自定义符号  
delimiter ;
```

  
根据上述案例的需求，我们创建两张表，商品表goods和订单表orders，SQL语句如下：  
``` SQL
create table goods(
    id int primary key auto_increment,
    name varchar(20) not null,
    price decimal(10, 2) default 0.0,
    inventory int comment '商品库存量'
) engine InnoDB charset utf8;

insert into goods values(null, 'iPhoneX', 7488, 1000), (null, 'iPhone8', 5088, 1000);

create table orders(
    id int primary key auto_increment,
    goods_id int not null,
    goods_number int default 1
) engine InnoDB charset utf8;
```
创建触发器：
``` SQL
delimiter $$
create trigger after_order after insert on orders for each row
begin
    update goods set inventory = inventory - 1 where id = 1;
end
$$
delimiter ;
```

- - - - -
## 28.2 查询触发器
查询所有触发器或模糊匹配：  
基本语法：  
``` SQL
show triggers [like 'pattern']
```

实例：
``` SQL
show triggers\G;
```
\G表示旋转

当然，我们可以查询创建触发器的语句。  
基本语法：  
``` SQL
show create trigger 触发器名称;
```
此外，所有的触发器都会被系统保持到information_schema.triggers这张表中，执行如下SQL，进行测试：
``` SQL
select * from information_schema.triggers\G;
```
- - - - -
## 28.3 使用触发器
实际上，触发器不是我们手动触发，而是在某种情况发生的时候自动触发，例如我们上面创建的after_order触发器，当我们insert订单表的时候，该触发器自动执行。执行如下SQL语句，进行测试：
``` SQL
mysql> select * from goods;
+----+---------+---------+-----------+
| id | name    | price   | inventory |
+----+---------+---------+-----------+
|  1 | iPhoneX | 7488.00 |      1000 |
|  2 | iPhone8 | 5088.00 |      1000 |
+----+---------+---------+-----------+
2 rows in set (0.00 sec)

mysql> select * from orders;
Empty set (0.00 sec)

mysql> insert into orders values(null, 2, 10);
Query OK, 1 row affected (0.00 sec)

mysql> select * from goods;
+----+---------+---------+-----------+
| id | name    | price   | inventory |
+----+---------+---------+-----------+
|  1 | iPhoneX | 7488.00 |       999 |
|  2 | iPhone8 | 5088.00 |      1000 |
+----+---------+---------+-----------+
2 rows in set (0.00 sec)

mysql> select * from orders;
+----+----------+--------------+
| id | goods_id | goods_number |
+----+----------+--------------+
|  1 |        2 |           10 |
+----+----------+---------
```
注意：触发器的触发对象和事件类型，决不能同触发器主体的内容相同，防止发生死循环。
- - - - -
## 28.4 修改触发器 & 删除触发器
触发器不能修改，只能删除。因此，当我们需要修改触发器的时候，唯一的办法就是：先删除，后新增。  
基本语法：  
``` SQL
drop trigger 触发器名称;
```

实例：  
``` SQL
drop trigger after_oder;
show triggers; 
```
- - - - -
## 28.5 触发器记录
触发器记录：无论触发器是否触发，只要当某种操作准备执行，系统就会将当前操作的记录的当前状态和即将执行之后的状态分别记录下来，供触发器使用。其中，当前状态被保存到old中，操作之后的状态被保存到new中。其中old和new保存如下字段：
- ACTION_REFERENCE_OLD_ROW：OLD
- ACTION_REFERENCE_NEW_ROW：NEW

其中：  
- OLD：代表是旧记录，也就是当前记录的状态，插入时没有OLD
- NEW：代表新记录，也就是假设操作发生之后记录的状态，删除时没有NEW
无论OLD还是 NEW，都代表记录本身，而且任何一条记录除了有数据，还有字段名。因此，使用OLD和 NEW的方法就是：  
基本语法：  
``` SQL
OLD/NEW + . + 字段名
```

实例：
``` SQL
delimiter $$
create trigger after_order_new after insert on orders for each row
begin
    update goods set inventory = inventory - NEW.goods_number where id = NEW.goods_id;
end
$$
delimiter ;
```

实例：
``` SQL
mysql> select * from goods;
+----+---------+---------+-----------+
| id | name    | price   | inventory |
+----+---------+---------+-----------+
|  1 | iPhoneX | 7488.00 |       999 |
|  2 | iPhone8 | 5088.00 |      1000 |
+----+---------+---------+-----------+
2 rows in set (0.00 sec)

mysql> select * from orders;
+----+----------+--------------+
| id | goods_id | goods_number |
+----+----------+--------------+
|  1 |        2 |           10 |
+----+----------+--------------+
1 row in set (0.00 sec)

mysql> insert into orders values(null, 2, 10);
Query OK, 1 row affected (0.00 sec)

mysql> select * from goods;
+----+---------+---------+-----------+
| id | name    | price   | inventory |
+----+---------+---------+-----------+
|  1 | iPhoneX | 7488.00 |       999 |
|  2 | iPhone8 | 5088.00 |       990 |
+----+---------+---------+-----------+
2 rows in set (0.00 sec)

mysql> select * from orders;
+----+----------+--------------+
| id | goods_id | goods_number |
+----+----------+--------------+
|  1 |        2 |           10 |
|  3 |        2 |           10 |
+----+----------+--------------+
2 rows in set (0.00 sec)
```
- - - - -
# 29、代码执行结构
在MySQL编程中，代码的执行结构有三种，分别为：  
- 顺序结构
- 分支结构
- 循环结构

下面主要说分支结构和循环结构。
- - - - -
## 29.1 分支结构
分支结构：事先准备多个代码代码块，通过判断条件是否满足，执行对应的代码。
在MySQL中，只有if分支结构，其基本语法为：
``` SQL
if 判断条件 then
    -- 满足条件时，要执行的代码
esle
    -- 不满足条件时，要执行的代码
end if;
```

接下来，我们利用触发器和if分支，完成这样的需求：  
在生成订单前，判断商品的库存是否满足，如果满足，则插入订单；否则插入失败。
实例：
``` SQL
delimiter $$
create trigger before_order before insert on orders for each row
begin
    select inventory from goods where id = NEW.goods_id into @inventory;
    if @inventory < NEW.goods_number then
        insert into xxx values(xxx);
    end if;
end
$$
delimiter ;
```
- - - - -
## 29.2 循环结构
在MySQL中，循环有while循环、loop循环和repeat循环，还有非标准的goto循环，这里介绍while循环，其基本语法为：
``` SQL
while 条件判断 do
    -- 满足条件要执行的代码
end while;
```
在使用循环结构的时候，我们经常需要对循环进行控制，即在循环结构内部进行判断和控制。虽然在 MySQL 中没有continue和break，但是有其替代关键字：
- iterate：迭代，类似于continue，表示结束本次循环，不执行后续步骤，直接开始下一次循环
- leave：离开，类似于break，直接结束整个循环

上述两个关键字的使用方法为：  
基本语法：  
``` SQL
iterate/leave 循环名称;
```
- - - - -
# 30、函数
函数，就是将一段代码封装到一个结构中，在需要执行该代码的时候，直接调用该结构（函数）执行即可。此操作，实现了代码的复用。在MySQL中，函数有两种，分别为：系统函数和自定义函数。

## 30.1 系统函数
任何函数都有返回值（对于空函数，我们认为其返回值为空），而且在MySQL中任何返回值的操作都是通过select来操作的，因此MySQL的函数调用就是通过select来实现的。  
下面，我们介绍一些常见的、对字符进行操作的系统函数：首先，执行如下语句，定义一些变量：
``` SQL
set @cn = '你好世界';
set @en = 'hello world';
set @one = 'harlon';
set @two = 'jack';
set @three = 'jack';

select @cn, @en, @one, @two, @three;
```

字符串函数：
- substring，截取字符串，单位为字符。

``` SQL
mysql> select substring(@cn, 1, 1), substring(@en, 1, 2);
+----------------------+----------------------+
| substring(@cn, 1, 1) | substring(@en, 1, 2) |
+----------------------+----------------------+
| 你                   | he                   |
+----------------------+----------------------+
1 row in set (0.00 sec)
```

- instr，判断字符串中某个子串是否存在，若存在返回具体的位置，不存在返回0。

mysql> select instr(@cn, '你好'), instr(@cn, '世'), instr(@en, 'c'); 
+----------------------+-------------------+-----------------+
| instr(@cn, '你好')   | instr(@cn, '世')  | instr(@en, 'c') |
+----------------------+-------------------+-----------------+
|                    1 |                 3 |               0 |
+----------------------+-------------------+-----------------+
1 row in set (0.00 sec)


- lpad：左填充，将字符串按照某个指定的填充方式，填充到指定长度。

``` SQL
mysql> select lpad(@cn, 20, '曾经'), lpad(@cn, 20, 'hello');
+--------------------------------------------------------------+------------------------------+
| lpad(@cn, 20, '曾经')                                        | lpad(@cn, 20, 'hello')       |
+--------------------------------------------------------------+------------------------------+
| 曾经曾经曾经曾经曾经曾经曾经曾经你好世界                     | hellohellohelloh你好世界     |
+--------------------------------------------------------------+------------------------------+
1 row in set (0.00 sec)
```

- insert，找到目标位置，将指定长度的字符串替换为目标字符串。

``` SQL
mysql> select insert(@en, 2, 4, 'i'), @en;
+------------------------+-------------+
| insert(@en, 2, 4, 'i') | @en         |
+------------------------+-------------+
| hi world               | hello world |
+------------------------+-------------+
1 row in set (0.00 sec)
```

- strcmp，比较字符串的大小。

``` SQL

mysql> select strcmp(@one, @two), strcmp(@two, @three), strcmp(@three, @one);
+--------------------+----------------------+----------------------+
| strcmp(@one, @two) | strcmp(@two, @three) | strcmp(@three, @one) |
+--------------------+----------------------+----------------------+
|                 -1 |                    0 |                    1 |
+--------------------+-----------
```
- - - - -
## 30.2 自定义函数
对于任意一个函数，都包含如下要素：
- 函数名
- 参数列表
- 返回值
- 函数体

- - - - -
## 30.3 创建函数
基本语法：
``` SQL
create function 函数名([参数列表]) returns 数据类型
begin
    -- 函数体
end
```

实例：
``` SQL
create function showLove() returns int
return 521;

select showLove();
```
- - - - -
## 30.4 查看函数
查看函数，基本语法为：
``` SQL
show function status + [like 'pattern']
```
查看函数的创建语句，基本语法为：
``` SQL
show create function 函数名;
```
- - - - -
## 30.5 修改函数 & 删除函数
函数只能先删除后新增，不能修改，删除函数的基本语法为：
``` SQL
drop function 函数名;
```
- - - - -
## 30.6 函数参数
对于函数的参数，一共有两种，分别为形参和实参，其中，形参可以理解为定义函数时使用的参数，且形参必须指定数据类型；实参可以理解为在调用函数时传入的值或变量。因此，函数定义的具体形式应该为：
``` SQL
function 函数名(形参名字 形参类型) returns 返回数据类型
```
定义一个函数，求1到指定数值的和。
``` SQL
delimiter $$
create function addAll(num int) returns int
begin
    set @i = 1;
    set @res = 0;
    while @i < num do
        set @res = @res + @i;
        set @i = @i +1;
    end while;
    return @res;
end
$$
delimiter ;

mysql> select addAll(100);
+-------------+
| addAll(100) |
+-------------+
|        4950 |
+-------------+
1 row in set (0.01 sec)

mysql> select @i, @res;
+------+------+
| @i   | @res |
+------+------+
|  100 | 4950 |
+------+------+
1 row in set (0.00 sec)
```
- - - - -
## 30.7 变量作用域
在 MySQL 中，变量的作用域有两种，分别为全局和局部，其中，全局变量可以在任何地方使用；局部变量只能在函数内部使用。
- 全局变量：使用set关键字定义，用@符号标识
- 局部变量：使用declare关键字声明，且所用的局部变量必须在函数体开始之前进行声明

定义一个函数，即求1到指定数值的和，要求10的倍数不加，代码如下：
``` SQL
delimiter $$
create function addAll2(num int) returns int
begin
    declare i int default 1;
    declare res int default 0;
    mywhile:while @i < num do
        if i % 10 = 0 then
            set i = i + 1;
            iterate mywhile;
    end if;
    set res = res + i;
    set i = i + 1;
    end while;
    return @res;
end
$$
delimiter ;

mysql> select addAll(100), addAll(200);
+-------------+-------------+
| addAll(100) | addAll(200) |
+-------------+-------------+
|        4950 |       19900 |
+-------------+-------------+
1 row in set (0.00 sec)
```
- - - - -
# 31、存储过程
存储过程：produce，是一种用来处理数据（增删改）的方式，简单点，我们也可以将其理解为没有返回值的函数。
## 31.1 创建过程
基本语法：
``` SQL
create proceduce 过程名([参数列表])
begin
    -- 过程体
end
```

实例：
``` SQL
create procedure pro()
select * from student;
```
- - - - -
## 32.2 查看过程
查看过程，基本语法为：
``` SQL
show procedure status [like 'pattern'];
```
查看过程的创建语句，基本语法为：
``` SQL
show create procedure 过程名;
```
- - - - -
## 32.3 调用过程
基本语法：
``` SQL
call 过程名;
```
- - - - -
## 33.3 修改过程 & 删除过程
过程只能先删除后新增，不能修改。删除过程的基本语法为：
``` SQL
drop procedure 过程名;
```
- - - - -
## 33.4 过程参数
函数的参数需要指定数据类型，过程比函数更加严格。过程有三种自己的参数类型，分别为：
- in：数据只是从过程外部传入给过程内部使用，可以使数值也可以使变量
- out：参数只能传递变量，且变量指向的数据需要先清空然后才能进入过程内部，该引用供过程内部使用，过程结束后可以将变量的值传递给过程外部使用
- inout：此参数只能传递变量，该变量的值可以给过程内部使用，过程结束后可以变量的值传递给过程外部使用

因此，过程定义的具体形式应该为：
``` SQL
procedure 过程名(in 参数名字 参数类型, out 参数名字 参数类型, inout 参数名字 参数类型)
```

实例：
``` SQL
delimiter $$
create procedure pro2(in var1 int, out var2 int, inout var3 int)
begin
    select var1, var2, var3;
end
$$
delimiter ;
```

测试：
``` SQL
set @var1 = 1;
set @var2 = 2;
set @var3 = 3;
mysql> call pro2(@var1, @var2, @var3);
+------+------+------+
| var1 | var2 | var3 |
+------+------+------+
|    1 | NULL |    3 |
+------+------+------+
1 row in set (0.00 sec)

Query OK, 0 rows affected (0.00 sec)

mysql> select @var1, @var2, @var3;
+-------+-------+-------+
| @var1 | @var2 | @var3 |
+-------+-------+-------+
|     1 |  NULL |     3 |   
+-------+-------+-------+
1 row in set (0.00 sec)
```
