## 1. 考试概要介绍

- 考试形式

  - 计算机与软件工程知识
    - 150分钟，笔试，75道选择题（每空一分，合格45分）
  - 软件设计
    - 150分钟，笔试，问答题（数据流、数据库、UML、算法、面向对象编程（C++和Java二选一，以设计模式为背景））

- 知识点及分值

  <img src="./img/8c144cc0f0c4aaa56dd357f62017cc9.png" alt="8c144cc0f0c4aaa56dd357f62017cc9" style="zoom:50%;" />



## 2. 计算机组成原理

### 2.1 进制转换

- R进制  --> 十进制

<img src="./img/fe115d9724a91834278bc373797dee3.png" alt="fe115d9724a91834278bc373797dee3" style="zoom:50%;" />

- 十进制  --> 二进制

<img src="./img/03f5c39724a6fea9671bf0a0b3f2c7c.png" alt="03f5c39724a6fea9671bf0a0b3f2c7c" style="zoom:50%;" />

- 二进制  <--> 八/十六进制

<img src="./img/cd1509f90b99b3095679618c3cea35d.png" alt="cd1509f90b99b3095679618c3cea35d" style="zoom:50%;" />

### 2.2 数据的表示（原、反、补和移码）

- 移码：对补码的最高位取反得到
- 数值表示范围

<img src="./img/98de6723b341d064aa0f90d4144ead4.png" alt="98de6723b341d064aa0f90d4144ead4" style="zoom:50%;" />

- 补码比原码多一个范围原因：补码中正0和负0共用一个表示。

### 2.3 浮点数运算

- 浮点数运算及步骤

![b2b086b16212770b77e34c8162f0ba0](./img/b2b086b16212770b77e34c8162f0ba0.png)

- 对阶：以高位的为准，使两个浮点数的指数相等。
- 结果格式化：
  - 尾数整数部分只能为1位
  - 尾数整数部分不能为0
  - 例子：1.19 x 10²

### 2.4 计算机结构

- 计算机结构图

<img src="./img/5d57a299517e2c3e48f6f6a664e8703.png" alt="5d57a299517e2c3e48f6f6a664e8703" style="zoom:50%;" />

- 累加寄存器AC：通用寄存器，用于存储运算相应的值（不仅仅是加法运算）。
- 数据缓冲寄存器DR：对内存储器进行读写操作时，用来暂存数据。
- 状态条件寄存器PSW：用来存储在运算过程中相关的状态标志位（进位、溢出和中断等）。
- 程序计数器PC：用来存放下一条执行指令地址（若顺序执行，则在原指令地址加1；若涉及跳转，则需要加多几个）。

### 2.5 Flynn分类法

- Flynn分类下的计算机体系结构图

<img src="./img/d93f96743771d363b8df37b7c5e76dd.png" alt="d93f96743771d363b8df37b7c5e76dd" style="zoom:50%;" />

### 2.6 CISC与RISC

- 指令系统类型

<img src="./img/c19e40ab020914904ce1b89bd4b11bd.png" alt="c19e40ab020914904ce1b89bd4b11bd" style="zoom:50%;" />

### 2.7 流水线

#### 2.7.1 概念

<img src="./img/90de7f0766d775e5f408f3e8b5390e8.png" alt="90de7f0766d775e5f408f3e8b5390e8" style="zoom:50%;" />

#### 2.7.2 指令执行过程

<img src="./img/c4098b89c3904761afa990dcdb02888.png" alt="c4098b89c3904761afa990dcdb02888" style="zoom:50%;" />

#### 2.7.3 流水线周期及执行时间计算

<img src="./img/f2a026daeec9e55244f72aa2a175c79.png" alt="f2a026daeec9e55244f72aa2a175c79" style="zoom:50%;" />

- 流水线周期：取值、分析和执行三个阶段时间最长的一段。
- 理论公式中 tn 为第一条指令中第n个步骤的执行时间。
- 实践公式中k为一个指令的执行步骤个数，n为流水线中要执行的指令个数。
- 注意：考试通常优先使用理论公式，若找不到解则使用实践公式。

#### 2.7.4 流水线吞吐率计算

- 吞吐量计算公式

<img src="./img/763b58c19187dca09e45cd698988e3a.png" alt="763b58c19187dca09e45cd698988e3a" style="zoom:50%;" />

- 最大吞吐率公式

<img src="./img/65b0210a5ffd5c70c16d8a8acd53e14.png" alt="65b0210a5ffd5c70c16d8a8acd53e14" style="zoom:50%;" />

#### 2.7.5 流水线的加速比及效率计算

- 加速比计算公式

<img src="./img/1c0e7d6212d2369dbb227e3ce55b00d.png" alt="1c0e7d6212d2369dbb227e3ce55b00d" style="zoom:50%;" />

- 效率计算公式<img src="./img/f7bfa48c620d22d950a5c257657fcc6.png" alt="f7bfa48c620d22d950a5c257657fcc6" style="zoom:50%;" />

### 2.8 层次化存储结构

- 层次化存储结构图

<img src="./img/c6fbd28abf0049a1a803c37c57c2faa.png" alt="c6fbd28abf0049a1a803c37c57c2faa" style="zoom:50%;" />

### 2.9 Cache

- 概念

<img src="./img/dfdfa0bc804fed958b24ac9b698e233.png" alt="dfdfa0bc804fed958b24ac9b698e233" style="zoom:50%;" />

- 引入Cache后系统的平均周期计算公式

<img src="./img/def92320e8a99b8ed7085368d3eb102.png" alt="def92320e8a99b8ed7085368d3eb102" style="zoom:50%;" />

### 2.10 局部性原理

- 概念

<img src="./img/5c3720b787b3ad1b0504f441d5704d3.png" alt="5c3720b787b3ad1b0504f441d5704d3" style="zoom:50%;" />

- 时间局部性原理：程序执行过程在短期时间内频繁访问同个内存空间。
- 空间局部性原理：程序执行过程频繁访问某一片临近的内存空间。

### 2.11 主存

- 主存分类

<img src="./img/64efdac66cdb766dbc768cbd05f201f.png" alt="64efdac66cdb766dbc768cbd05f201f" style="zoom:50%;" />

- 主存编址

<img src="./img/74a0afca60b22fec17503ee988fe07c.png" alt="74a0afca60b22fec17503ee988fe07c" style="zoom:50%;" />

### 2.12 磁盘工作原理

- 磁盘结构与参数

<img src="./img/5faa2baa5ef0fea646be1286a790c53.png" alt="5faa2baa5ef0fea646be1286a790c53" style="zoom:50%;" />

- 试题

<img src="./img/3575a31e23cecadd9cff134c2f81628.png" alt="3575a31e23cecadd9cff134c2f81628" style="zoom:50%;" />

- 题解

1. 顺序处理

<img src="./img/cf3e1b16a88e471ac2ef4f9fd7ea7d9.png" alt="cf3e1b16a88e471ac2ef4f9fd7ea7d9" style="zoom:50%;" />

2. 优化处理
   - t = 11 x (3+3) = 66ms

### 2.13 总线

- 分类

<img src="./img/e91a8ce47427ca44b1513cf7e092a1d.png" alt="e91a8ce47427ca44b1513cf7e092a1d" style="zoom:50%;" />

- 内部总线：微机内部各个外围芯片与处理器之间的总线。
- 系统总线：微机中各个插件板和系统板的总线（PCI，VGA）。

### 2.14 系统可靠性分析

#### 2.14.1 串联系统

<img src="./img/82164d6db3bec79d2255e481478ba01.png" alt="82164d6db3bec79d2255e481478ba01" style="zoom:50%;" />

- 其中R为可靠度，λ为失效率。

#### 2.14.2 并联系统

<img src="./img/9f35c199c9ea167bdd9452ef41a4d1c.png" alt="9f35c199c9ea167bdd9452ef41a4d1c" style="zoom:50%;" />

- 上述μ的计算公式过于复杂，可以使用 μ = 1 - R 方法计算得出。

#### 2.14.3 模冗余系统与混合系统（几乎不考）

<img src="./img/2d6f50a4be3886344c56664d16b1631.png" alt="2d6f50a4be3886344c56664d16b1631" style="zoom:50%;" />

- 例题

<img src="./img/eff3cdcc18558e8d59f4d4237ced7eb.png" alt="eff3cdcc18558e8d59f4d4237ced7eb" style="zoom:50%;" />

### 2.15 校验码

#### 2.15.1 概念

- 什么是检错和纠错？
  - 检错：检测出错误
  - 纠错：检测出错误之后能进一步纠正
- 什么是码距？
  - 一个编码系统的码距是整个编码系统中任意（所有）两个码字的最小距离。（简单来说，就是一个码改变x个位可以变成另一个码，x为码距）
- 码距与检错、纠错的关系

<img src="./img/2ddcea66d760e7673df5c3c53c9bf3b.png" alt="2ddcea66d760e7673df5c3c53c9bf3b" style="zoom:50%;" />

#### 2.15.2 CRC循环校验码（只能检错）

- 原理：对原始报文后面加上n个0，然后与生成**多项式对应的n位二进制数**进行模2除法，然后在原始报文加上余数（n位）生成校验码，此时校验码除以**多项式对应的二进制数**结果为0。（通过结果检测报文是否有差错）。
- 模2除法中间值不是相减，而是做异或运算。

<img src="./img/8c5fa71607d104b0753eeda95cd8d7c.png" alt="8c5fa71607d104b0753eeda95cd8d7c" style="zoom:50%;" />

- 例题

<img src="./img/7a3c8163405ea380c1e2106e8cd085e.png" alt="7a3c8163405ea380c1e2106e8cd085e" style="zoom:50%;" />

#### 2.15.2 海明校验码（可以检错和纠错）

- 原理：在第 2^n 位上放置校验位（校验位通过**校验位公式**计算得出），其他的做信息位。收到报文之后，使用报文的信息位生成**新校验位**，再使用报文中的校验位与**新校验位**做异或运算，再将二进制结果转为十进制d，代表报文中第d位出错，此时将其取反则可以得到正确的报文。
- 信息位数 x 与校验位  r 的关系
  - 2^r >= x + r + 1

- 例题（包含校验位公式）

<img src="./img/af72e00263a0788fc1905e62bed68a5.png" alt="af72e00263a0788fc1905e62bed68a5" style="zoom:50%;" />

## 3. 操作系统（5~7分）

### 3.1 概述

<img src="./img/cf8bfb8eb09f43baec6ee73401c8221.png" alt="cf8bfb8eb09f43baec6ee73401c8221" style="zoom:50%;" /><img src="./img/5d7f9d93e71cb8d77a7b7cbaee2a904.png" alt="5d7f9d93e71cb8d77a7b7cbaee2a904" style="zoom:50%;" />

### 3.2 进程管理

#### 3.2.1 进程的状态及转换

<img src="./img/d1ac3b857967894f97a718b1ac0f3c9.png" alt="d1ac3b857967894f97a718b1ac0f3c9" style="zoom:50%;" />

#### 3.2.2 前趋图

<img src="./img/3cc82b530e4015c424c3342c4e38d49.png" alt="3cc82b530e4015c424c3342c4e38d49" style="zoom:50%;" />

#### 3.2.3 进程的同步与互斥

<img src="./img/70b9581ce30f73160269ea605a24e79.png" alt="70b9581ce30f73160269ea605a24e79" style="zoom:50%;" />

- 互斥：指的是同一时间内只能有一个线程去访问特定资源。
- 同步：指的是多个线程操作以一定的时序进行。

#### 3.2.4 PV操作

- 概念

<img src="./img/bc5d2fa958fc2464836a8232cb4d989.png" alt="bc5d2fa958fc2464836a8232cb4d989" style="zoom:50%;" />

- 单缓冲区生产者、消费者例子

<img src="./img/189fc809e21ebdfe9500e83aeb2a9a4.png" alt="189fc809e21ebdfe9500e83aeb2a9a4" style="zoom:50%;" />

   注：其中S1为缓冲区空闲空间的大小，S2为缓冲区产品的数量。

- 例题

<img src="./img/f545664e4f6bdf3ade4b66f229ea44e.png" alt="f545664e4f6bdf3ade4b66f229ea44e" style="zoom:50%;" />

#### 3.2.5 PV操作与前趋图

<img src="./img/114278ad41a0781eca29cfdb4d646b2.png" alt="114278ad41a0781eca29cfdb4d646b2" style="zoom:50%;" />

- 例题

<img src="./img/ce8182c523832a407b280a43a202d91.png" alt="ce8182c523832a407b280a43a202d91" style="zoom:50%;" />

#### 3.2.6 死锁问题

- 概念



<img src="./img/1786efb3385fd3ef1798ca29acbd360.png" alt="1786efb3385fd3ef1798ca29acbd360" style="zoom:50%;" />

  注：n个进程，每个进程需要x个资源，至少需要 **n(x-1)+1** 个资源才不可能发生死锁。

- 死锁预防与避免

<img src="./img/2bb34b567b8dde063867aa140a3346d.png" alt="2bb34b567b8dde063867aa140a3346d" style="zoom:50%;" />

#### 3.2.7 银行家算法

- 概念

<img src="./img/9359d1f4116d9f06f2c155299152926.png" alt="9359d1f4116d9f06f2c155299152926" style="zoom:50%;" />

- 例题

<img src="./img/873ab94f4808490340022468b38035d.png" alt="873ab94f4808490340022468b38035d" style="zoom:50%;" />

### 3.3 存储管理

#### 3.3.1 分区存储组织

<img src="./img/73716d0017619d0443c7cca75fedc30.png" alt="73716d0017619d0443c7cca75fedc30" style="zoom:50%;" />

#### 3.3.2 页式存储组织

<img src="./img/9af7c2a4cb8e2824082e91f5b012db4.png" alt="9af7c2a4cb8e2824082e91f5b012db4" style="zoom:50%;" />

- 例题

<img src="./img/65474ca45cd8d272d93678605e2eca1.png" alt="65474ca45cd8d272d93678605e2eca1" style="zoom:50%;" />

#### 3.3.3 段式存储组织

<img src="./img/4103bc565a831f17f5df5cf4f9d750e.png" alt="4103bc565a831f17f5df5cf4f9d750e" style="zoom:50%;" />

#### 3.3.4 段页式存储组织

<img src="./img/3b488d2c01473518ca5873ebf1c370b.png" alt="3b488d2c01473518ca5873ebf1c370b" style="zoom:50%;" />

#### 3.3.5 快表

<img src="./img/ca0f33970fd81a62113cbb012aa0f34.png" alt="ca0f33970fd81a62113cbb012aa0f34" style="zoom:50%;" />

#### 3.3.6 页面置换算法

- 常见算法

<img src="./img/46b18967abc972d2e5f468019270907.png" alt="46b18967abc972d2e5f468019270907" style="zoom:50%;" />

- 抖动现象

<img src="./img/0ac9d51621c645e9706fc2439e56c88.png" alt="0ac9d51621c645e9706fc2439e56c88" style="zoom:50%;" />

- 例题

<img src="./img/9455a05372cb8382e5f7114c269098e.png" alt="9455a05372cb8382e5f7114c269098e" style="zoom:50%;" />

- 练习题

<img src="./img/a310359b5c598659b0b487e3ea96616.png" alt="a310359b5c598659b0b487e3ea96616" style="zoom:50%;" />

注：当一条指令存储在多个页面时，调入内存只会产生一次缺页中断，而操作数则是一个页面产生一个缺页中断。

### 3.4 文件管理

#### 3.4.1 索引文件结构

<img src="./img/9819418ff97e4a4a04911f05c89505a.png" alt="9819418ff97e4a4a04911f05c89505a" style="zoom:50%;" />

<img src="./img/2fecf61d68391e85d4916c03e2b2086.png" alt="2fecf61d68391e85d4916c03e2b2086" style="zoom:50%;" />

#### 3.4.2 文件和树型目录结构

<img src="./img/bc18d21453cf9a72b517652e34d6384.png" alt="bc18d21453cf9a72b517652e34d6384" style="zoom:50%;" />

 

#### 3.4.3 空闲存储空间的管理

<img src="./img/886030b12886d3b01b6010d950d6c19.png" alt="886030b12886d3b01b6010d950d6c19" style="zoom:50%;" />

- 例题

<img src="./img/3e753c3d0ad12818b061714c63a6d18.png" alt="3e753c3d0ad12818b061714c63a6d18" style="zoom:50%;" />

<img src="./img/e2a47d3adaa17aed4451f6aa456f768.png" alt="e2a47d3adaa17aed4451f6aa456f768" style="zoom:50%;" />

注：考试默认字从**1**开始，位从**0**开始。

### 3.5 设备管理

#### 3.5.1 数据传输控制方式

<img src="./img/c56d1102962d64fbb3a77499a15173c.png" alt="c56d1102962d64fbb3a77499a15173c" style="zoom:50%;" />

#### 3.5.2 虚设备与SPOOLING技术

<img src="./img/4d37b8e74f8d7fedc7cc0bd388b6520.png" alt="4d37b8e74f8d7fedc7cc0bd388b6520" style="zoom:50%;" />

### 3.6 微内核操作系统

<img src="./img/7d8b445b4bc4539773e24dac3b147b7.png" alt="7d8b445b4bc4539773e24dac3b147b7" style="zoom:50%;" />
