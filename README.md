# neo4j-ex

[![Build Status](https://travis-ci.org/supermy/rule-interceptor.svg?branch=master)](https://github.com/supermy/rule-interceptor)

缘起：用DB 实现一套RBAC 很不爽，寻寻觅觅，找到了Neo4j。

图计算 [flume-rule-interceptor](https://github.com/supermy/rule-interceptor). 图形数据库适合用于社交网络，推荐系统等专注于构建关系图谱的系统。。
在Neo4j里，图遍历执行的速度是常数，跟图的规模大小无关。不象在RDBMS里常见的联结操作那样，这里不涉及降低性能的集合操作。Neo4j以一种延迟风格遍历图 - 节点和关系只有在结果迭代器需要访问它们的时候才会被遍历并返回，对于大规模深度遍历而言，这极大地提高了性能。
写速度跟文件系统的查找时间和硬件有很大关系。Ext3文件系统和SSD磁盘是不错的组合，这会导致每秒大约100,000写事务操作。

Neo4j是一个用Java实现、完全兼容ACID的图形数据库。数据以一种针对图形网络进行过优化的格式保存在磁盘上。Neo4j的内核是一种极快的图形引擎，具有数据库产品期望的所有特性，如恢复、两阶段提交、符合XA等。

Neo4j作为单独的服务器运行，还可以找到REST包装器。这非常适合使用LAMP软件搭建的架构。通过memcached、e-tag和基于Apache的缓存和Web层，REST甚至简化了大规模读负荷的伸缩。

业务场景1：rbac。

业务场景2：关系DB数据导入。大数据量的话，支持批量导入的，在neo4j的安装文件下可以找到这个batch-import-jar-with-dependencies-2.1.8.jar ，执行对应的批处理命令就可以把二维数据库里面抽出的数据快速生成图。

## Install

安装:

    https://neo4j.com/docs/operations-manual/current/installation/

## Usage

使用原生的rest；
提供定制的rest；

### rbac

关系 db csv文件数据导入；
用户角色配置；
角色权限配置；
用户群组配置；
群组角色配置；
用户权限查询；

```

```
