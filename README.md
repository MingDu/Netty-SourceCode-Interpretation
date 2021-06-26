# Netty 源码解读

Netty Version: 4.1.63
Doc Version: 1.0.0

## 作者
| 微信公众号 | 名称 | 贡献 |
|:----------:|:-------------|:------------:|
|[@阿杜看源码](http://weibo.com/jerrylead) <img src="images/weixin.png" alt="二维码" style="zoom:25%;" /> | 阿杜 | 所有的中文版本 |

## 介绍

本文主要讨论Netty的Server主体框架, PipeLine处理流程, ByteBuf空间管理及一些示例的Handler.
从源码细节到大体的流程梳理, 希望通过图示的方式能把Netty的大体运行说清楚, 图意在基于UML 2的规范, 但还是有很多场景没找到对应的示例, 还请多提意见. 
有错误及不足的地方还请多指正, 希望能对大家有帮助. 

## 内容
1. [Overview]() 总体介绍

2. [ServerBootStrap]() 服务端与客户端的启动

3. [Pipeline]() Pipeline 的执行过程.

4. [PooledByteBuf]() PooledByteBuf 的管理过程.

5. [Handler 执行过程]() Handler 的执行过程.

   测试方法的用例: https://github.com/netty/netty/tree/4.1/buffer/src/test/java/io/netty/buffer 
   
   github上不能正常显示公式, 可以下载chrome插件: MathJax Plugin for Github, https://chrome.google.com/webstore/detail/mathjax-plugin-for-github/ioemnmodlmafdkllaclgeombjnmnbima/related

## 参考
1. [Netty案例大全](https://github.com/waylau/netty-4-user-guide-demos)
2. [Netty内存池](https://blog.csdn.net/cq_pf/article/details/107767775) 

<span style="color: rgb(242, 157, 0);box-sizing: border-box;">颜色</span>