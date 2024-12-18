---
layout: post
title:  "netstat命令的使用"
date:   2024-12-17 20:35:00 +0800
categories: linux shell
---

在开发部署服务器或者docker中，经常会发现所使用的端口被占用。若要查看哪些端口被哪些程序所占用，这个使用就需要使用`netstat`命令。

#### 1.常用参数

```shell
netstat -tunlp |grep "4001"
```

比如我要查看centos中4001端口被哪个程序所占用，就可以使用上面的命令来显示。

<img src="..\assets\img\PixPin_netstat_20241218.png" style="zoom:200%;" />

- t ：显示TCP连接
- u：显示UDP连接
- n：显示数字地址
- l：列出状态是LISTEN的统计信息
- p：显示程序的pid和程序名称

#### 2.查看docker中占用的端口信息

```shell
netstat -tunlp|grep 
```

<img src="D:\simplepxy.github.io\assets\img\PixPin_netstat_2024121802.png" style="zoom:200%;" />





