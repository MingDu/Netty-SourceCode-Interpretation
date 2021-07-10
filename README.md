# 读Netty源码

### 一. 版本:

​	Netty Version: 4.1.63
​	Doc Version: 1.0.0

### 二. 作者:	

| 名称 | 贡献 | 联系方式 |
|:------------:|:------------:|:----------:|
| 阿杜看源码 | 中文版本 | [@阿杜看源码]() <img src="./netty_4.1.63/images/weixin.png" alt="二维码" style="zoom:15%;" /> |

### 三. 介绍:

​	本文主要讨论Netty的Server主体框架, PipeLine处理流程, ByteBuf空间管理及一些示例的Handler.
​	从源码细节到大体的流程梳理, 希望通过图示的方式能把Netty的大体运行说清楚, 图意在基于UML 2的规范, 但还是有很多场景没找到对应的示例, 还请多提意见. 
​	有错误及不足的地方还请多指正, 希望能对大家有帮助. 

### 四. 内容:

1. 总体介绍(未完成).

2. 服务端与客户端的互动(未完成).

3. Pipeline 的执行过程(未完成).

4. 内存管理过程, PooledByteBuf 的管理过程.

   - PooledByteBuf 概括(进行中).
   - [1.SizeClasses 标准制定者](https://mingdu.github.io/Reading-Netty-SourceCode/netty_4.1.63/1.SizeClasses.html).
   - [2.PoolSubpage 共享区域的管理](https://mingdu.github.io/Reading-Netty-SourceCode/netty_4.1.63/2.PoolSubpage.html).
   - [3.PoolChunk](./netty_4.1.63/3.PoolChunk.html)

5. Handler 的执行过程(未完成).

   

   **注**: github上不能正常显示公式, 可以下载chrome插件: [MathJax Plugin for Github](https://chrome.google.com/webstore/detail/mathax-plugin-for-github/ioemnmodlmafdkllaclgeombjnmnbima/related)

### 五. 参考:

1. [Netty案例大全](https://github.com/waylau/netty-4-user-guide-demos)
2. [Netty内存池](https://blog.csdn.net/cq_pf/article/details/107767775)
3. [Netty Github上的ByteBuf测试用例]( https://github.com/netty/netty/tree/4.1/buffer/src/test/java/io/netty/buffer)



#### 	"阿杜看源码"所有稿件, 未经正式授权一律不得转载、出版、改编，或进行与"阿杜看源码"版权相关的其他行为，违者必究！
