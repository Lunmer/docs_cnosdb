---
title: 路线图
order: 3
---
# CnosDB 2.0 Roadmap 

![RoadMap](/_static/img/RoadMap.png)

## CnosDB 2.0 总体设计目标
设计并开发一个高性能、高压缩比、高可用的分布式云原生时间序列数据库，满足以下目标：
### 时序数据库
1. 扩展性，理论上支持的时间序列无上限，彻底解决时间序列膨胀问题，支持横/纵向扩展。
2. 计算存储分离，计算节点和存储节点，可以独立扩缩容，秒级伸缩。
3. 高性能存储和低成本，利用高性能io栈，支持利用云盘和对象存储进行分级存储。
4. 查询引擎支持矢量化查询。
5. 支持多种时序协议写入和查询，提供外部组件导入数据。
### 云原生
1. 支持云原生，支持充分利用云基础设施带来的便捷，融入云原生生态。
2. 高可用性，秒级故障恢复，支持多云，跨区容灾备灾。
3. 原生支持多租户，按量付费。
4. CDC,日志可以提供订阅和分发到其他节点。
5. 为用户提供更多可配置项，来满足公有云用户的多场景复杂需求。
6. 云边端协同，提供边端与公有云融合的能力
7. 融合云上OLAP/CloudAI 数据生态系统。



### CnosDB V 2.4.0 设计目标
CnosDB V 2.4.0 版本将实现：增加时序函数、添加有损压缩算法、支持更新和删除操作和有主复制组，该版本的CnosDB将为能够为用户提供一个更高性能、更易操作、更全面的数据处理能力的开源时序数据库，详细功能描述如下。

#### 时空函数
支持空间类型和时空函数，空间类型将以标准的WKT与WKB的模式进行支持，支持的时空函数包括但不限于位置计算、面积计算、移动速度计算等。
#### 高级函数
常用函数（first、last、max、min）、日期转换类、监控类（gauges计算）。
#### 有损压缩
- Deadband Compression ：一种数据压缩算法，用于降低传感器数据更新的频率，减少数据传输和存储成本。
- Swinging Door Trending (SDT)  Algorithm ：一种实时数据流处理算法，可以用于处理动态数据集合，通过不断调整门的大小来维护数据集中元素的数量。
#### 支持Schema change 
支持 Update、Delete 等操作。
#### 添加有主复制组 
实现处理流数据的 exactly once 语义。
