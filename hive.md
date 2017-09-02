# Hive

Hive是基于Hadoop的一个数据仓库工具，可以将结构化的数据文件映射为一张数据库表，并提供简单的sql查询功能，可以将sql语句转换为MapReduce任务进行运行。 其优点是学习成本低，可以通过类SQL语句快速实现简单的MapReduce统计，不必开发专门的MapReduce应用，十分适合数据仓库的统计分析。

### 1.非交互模式

### 执行脚本
> hive -f script.sql    
####直接执行sql语句

> hive -e 'select * from table_a'

### 2.交互模式常用命令
| 命令                     | 描述              |
| ---------------------- | --------------- |
| quit、exit              | 退出              |
| source FILE <filePath> | 在CLI里执行一个hive脚本 |

### 3.hive sql
####展示所有数据库

> hive> show databases;

####显示的展示当前数据库

> hive> set hive.cli.print.current.db = true;

####切换数据库

> hive> use test;

####创建数据库

> hive> create database db_test;

####删除数据库

删除有数据的数据库时，会报错，加CASCADE忽略报错信息
> hive> drop database test_db [cascade];    
> hive> drop database if exists db_name cascade;

####展示所有表

> show talbes [in db_name];

