# 学习笔记

## 登陆登出
```
-- 登录MySQL
mysql -u root -p12345612

-- 退出MySQL数据库服务器
exit;
```
## 创建数据库
create database test;

## 切换数据库
use test;

## 显示数据库中所有的表
show tables;

## 创建数据表
create table pet(
  name varchar(20),
  owner varchar(20),
  species varchar(20),
  sex char(1),
  birth date,
  death date
);

## 查看数据表结构
describe pet;
desc pet;

## 查询表
select * from pet;

## 插入数据
insert into pet values('petname', 'ownername', 'species', 'f', 'date', 'date');

## 修改数据
update pet set name = 'squirrel' where owner = 'diane';

## 删除表
drop table pet;





