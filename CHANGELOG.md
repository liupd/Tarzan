# Change Log
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/)
and this project adheres to [Semantic Versioning](http://semver.org/).

## [0.9.1] - 2018-02-01
### Added
- 新增服务端的自动选举master功能
- 新增【数据中心Id】的配置项，用于区分zookeeper
- 客户端新增销毁方法

### Changed
- 消息消费结果记录逻辑修改
- 取消【服务端workId】的配置项，通过zookeeper自动生成

## [0.9.0] - 2017-08-07
### Added
- 消息消费结果记录tag

## [0.8.2] - 2017-07-20
### Changed
- 修复MQ消息不能保存tag的问题

## [0.8.1] - 2017-05-31
### Added
- 新增［汇集计划］清理功能
- 新增事务检查和消息重发功能

## [0.8.0] - 2017-05-03
### Added
- RocketMQ消息支持Tag
- 待发消息支持按产生时间查询
- 客户端bean加载支持属性注入，避免循环依赖
- 客户端和服务端地址新增version字段

## [0.7.1] - 2017-03-08
### Added
- 新增接入CAT监控

### Changed
- 服务端基于Spring改造

## [0.7.0] - 2017-01-12
### Added
- 新增消息消费结果的记录
- 新增负载均衡算法

### Changed
- 优化客户端心跳发送（多个生产者group合并成一个心跳）
- 调整RocketMQ参数字段
- TbjMQ客户端整合到mq-client
- tarzan-admin拆分为独立工程
- 权重基准值调整为10

## [0.6.0] - 2017-01-10
### Added
- 新增部署说明文档

### Changed
- 修复消息重发未记录msgId的问题
- 文档目录调整
- 表结构调整，增加id字段

## [0.5.0] - 2016-12-12
### Added
- 新增Redis锁，避免定时任务并发
- 新增事务消息查询功能

### Changed
- 项目更名为Tarzan
- 事务检查和消息重发查询性能优化
- 分表数调整：256张虚表（实际存储16张表）

## [0.3.1] - 2016-12-05
### Added
- 新增从消息分表汇总到待处理表，超时的消息汇总到［待事务检查表］，
发送失败的消息汇总到［待发送表］
- 新增消息重发定时任务，对发送失败的MQ消息定时重发
- 新增store模块的数据流图

### Changed
- 优化消息事务状态检查定时任务
- 更新TEvent架构图

## [0.3.0] - 2016-11-29
### Added
- 新增admin管理端，支持服务端和ServerId列表查询，
及失效ServerId的删除

## [0.2.0] - 2016-11-16
### Added
- 新增单元测试

### Changed
- 重构Store模块

## [0.1.0] - 2016-11-03
### Added
- 新增Server端启动脚本
- 新增tbjmq客户端

### Changed
- 重构Server和Client配置
- 重构Server端MQ消息发送者
- 重构MQ客户端