# 基本语法

## 登陆登出
```
-- 登录MySQL
mysql -u root -p12345612

-- 退出MySQL数据库服务器
exit;
```
```
-- 创建数据库
create database test;

-- 切换数据库
use test;
```


## 数据表操作
```
-- 显示数据库中所有的表
show tables;

-- 创建数据表
create table pet(
  name varchar(20),
  owner varchar(20),
  species varchar(20),
  sex char(1),
  birth date,
  death date
);

-- 查看数据表结构
describe pet;
desc pet;

-- 查询表
select * from pet;

-- 删除表
drop table pet;
```

## 数据操作
```
-- 插入数据
insert into pet values('petname', 'ownername', 'species', 'f', 'date', 'date');

-- 修改数据
update pet set name = 'squirrel' where owner = 'diane';

-- 删除数据
delete from pet where name = 'Maxwell';

-- 修改数据
update pet set name = 'wangwangcai' where owner = 'zhouxinchi';
```
# 键表约束

## 主键约束
可以唯一确认一张表中的一条记录
通过给某个字段添加约束，使得该字段不重复且不为空
```
create table user(
  id int primary key,
  name varchar(20) 
);

+-------+-------------+------+-----+---------+-------+
| Field | Type        | Null | Key | Default | Extra |
+-------+-------------+------+-----+---------+-------+
| id    | int         | NO   | PRI | NULL    |       |
| name  | varchar(20) | YES  |     | NULL    |       |
+-------+-------------+------+-----+---------+-------+
PRI代表主键约束

-- 插入数据
insert into user values(1, 'zhangsan');
+----+----------+
| id | name     |
+----+----------+
|  1 | zhangsan |
+----+----------+

-- 联合主键
create table user2(
  id int,
  name varchar(20),
  password varchar(20),
  primary key(id, name)
);
```

## 自增约束

## 外键约束

## 唯一约束

## 非空约束

## 默认约束

```
-- 创建数据表
create table transformer_3(
  NUMBER varchar(20),
  DATE date,
  TIME time,
  I LONGTEXT,
  Q LONGTEXT,
  MALFUCTION char(1),
  MAL_TYPE char(1),
  COMPARISON char(1)
);
```


