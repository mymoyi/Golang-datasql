# Golang-datamysql

标签（空格分隔）： 服务计算

---

## 1.框架
**gorm**
概述

- 全功能ORM（几乎）
- 关联（包含一个，包含多个，属于，多对多，多种包含）
- Callbacks（创建/保存/更新/删除/查找之前/之后）
- 预加载（急加载）
- 事务
- 复合主键
- SQL Builder
- 自动迁移
- 日志
- 可扩展，编写基于GORM回调的插件
- 每个功能都有测试
- 开发人员友好

## 2.特性
- 支持 Go 的所有类型存储
- 轻松上手，采用简单的 CRUD 风格
- 自动 Join 关联表
- 跨数据库兼容查询
- 允许直接使用 SQL 查询／映射
- 严格完整的测试保证 ORM 的稳定与健壮

## 3.安装
    go get github.com/astaxie/beego/orm
    
## 4.测试
    moyi@ubuntu:~/Desktop/gocode/hw6$ ab -n 1000 -c 100 http://localhost:8080/service/userinfo?userid=

    This is ApacheBench, Version 2.3 <$Revision: 1757674 $>
    Copyright 1996 Adam Twiss, Zeus Technology Ltd, http://www.zeustech.net/
    Licensed to The Apache Software Foundation, http://www.apache.org/

    Benchmarking localhost (be patient)
    Completed 100 requests
    Completed 200 requests
    Completed 300 requests
    Completed 400 requests
    Completed 500 requests
    Completed 600 requests
    Completed 700 requests
    Completed 800 requests
    Completed 900 requests
    Completed 1000 requests
    Finished 1000 requests


    Server Software:        
    Server Hostname:        localhost
    Server Port:            8080

    Document Path:          /service/userinfo?userid=
    Document Length:        663 bytes

    Concurrency Level:      100
    Time taken for tests:   0.412 seconds
    Complete requests:      1000
    Failed requests:        0
    Total transferred:      683000 bytes
    HTML transferred:       559000 bytes
    Requests per second:    2956.25 [#/sec] (mean)
    Time per request:       37.256 [ms] (mean)
    Time per request:       0.422 [ms] (mean, across all concurrent requests)
    Transfer rate:          1888.89 [Kbytes/sec] received

    Connection Times (ms)
                   min  mean[+/-sd] median   max
    Connect:        0    1   0.9      0       5
    Processing:     1   34  29.5     27     137
    Waiting:        1   33  29.5     27     137
    Total:          1   34  29.7     27     139
    WARNING: The median and mean for the initial connection time are not within a normal deviation
            These results are probably not that reliable.

    Percentage of the requests served within a certain time (ms)
    50%     22
    66%     34
    75%     36
    80%     42
    90%     90
    95%    117
    98%    123
    99%    134
    100%    143 (longest request)




