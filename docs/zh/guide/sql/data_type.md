---
title: 数据类型
icon: config
order: 1
---

## 数据类型

| 类型            | 描述              | 大小  |
| --------------- | ----------------- | ----- |
| BIGINT          | 整型              | 8字节 |
| BIGINT UNSIGNED | 无符号整型        | 8字节 |
| BOOLEAN         | 布尔类型          | 1字节 |
| TIMESTAMP       | 时间戳            | 8字节 |
| STRING          | UTF-8编码的字符串 | ----- |
| DOUBLE          | 双精度浮点型      | 8字节 |

- TIMESTAMP
- BIGINT
- BIGINT UNSIGNED
- DOUBLE
- STRING
- BOOLEAN

## 常量

| 类型              | 语法                            | 说明                                                                                 |
|-----------------| ------------------------------- |------------------------------------------------------------------------------------|
| BIGINT          | [{+\| -}]123                                                                             |      数值类型                |
| BIGINT UNSIGNED | [+]123                          | 数值类型                                                                               |
| DOUBLE          | 123.45                          | 数值类型，目前暂不支持科学记数法                                                          |
| BOOLEAN         | {true &#124; false&#124; t &#124; f} |                                                       |
| STRING          | 'abc'                           | 不支持双引号格式，引号中连续两个''转义成‘                                               |
| TIMESTAMP       | TIMESTAMP '1900-01-01 12:00:00' | 时间戳，TIMESTAMP 关键字表示后面的字符串字面量需要被解释为 TIMESTAMP 类型。字符串需要满足 YYYY-MM-DD HH:mm:ss.MS 格式。 |
| --              | NULL                            | 空值                                                                                 |
