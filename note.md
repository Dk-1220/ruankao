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

## 4. 数据库系统

### 4.1 三级模式—两级映射

<img src="/img/0984dc2f9b701f67356f0e5533d9034.png" alt="0984dc2f9b701f67356f0e5533d9034" style="zoom:50%;" />

### 4.2 数据库设计过程

<img src="/img/32e94963a018f7e53d298b2a51f598c.png" alt="32e94963a018f7e53d298b2a51f598c" style="zoom:50%;" />

### 4.3 E-R模型

- 概念

<img src="/img/80ac96d905d2495886e6daffac29ffd.png" alt="80ac96d905d2495886e6daffac29ffd" style="zoom:50%;" />

- E-R图集成方法、冲突及解决办法

<img src="/img/70a47fbf301f31a8f2ffd0a02277ef9.png" alt="70a47fbf301f31a8f2ffd0a02277ef9" style="zoom:50%;" />

- 例题

<img src="/img/973c8291dea7cf3ce3e2ddea2f58b7a.png" alt="973c8291dea7cf3ce3e2ddea2f58b7a" style="zoom:50%;" />

### 4.4 关系代数（选择题）

#### 4.4.1 交、并、差

<img src="/img/e49f957aca5e805939f3f44b748268e.png" alt="e49f957aca5e805939f3f44b748268e" style="zoom:50%;" />

- 交：选择相同部分
- 并：合并之后去除重复部分
- 差：去除相同部分

#### 4.4.2 笛卡尔积

<img src="/img/e2ea13fcce3444e2d4c8decbffd437d.png" alt="e2ea13fcce3444e2d4c8decbffd437d" style="zoom:50%;" />

#### 4.4.3 投影、选择

<img src="/img/fa8291cb176cbc5b1499e8e1cf5e0e7.png" alt="fa8291cb176cbc5b1499e8e1cf5e0e7" style="zoom:50%;" />

- 投影：列出特定列
- 选择：列出特定行
- 注：这里可用数值代表投影或选择第几个字段

#### 4.4.4 联接

<img src="/img/75604504db54bcbad7f81c716403e10.png" alt="75604504db54bcbad7f81c716403e10" style="zoom:50%;" />

- 与笛卡尔积不同之处：相同的字段只会保留一个，且需要指明连接条件，若没有指明连接条件且只有一个相同的字段，则默认选择该字段作为条件进行连接。

### 4.5 规范化理论

#### 4.5.1 函数依赖

<img src="/img/b178f8db124bb25edfafdbb49205301.png" alt="b178f8db124bb25edfafdbb49205301" style="zoom:50%;" />

#### 4.5.2 价值与用途

<img src="/img/8421a99eb1782f45552b9f9df4ceb2a.png" alt="8421a99eb1782f45552b9f9df4ceb2a" style="zoom:50%;" />

#### 4.5.3 键

- 概念

<img src="/img/a8558a943ad8a64f90bea65f8c0f923.png" alt="a8558a943ad8a64f90bea65f8c0f923" style="zoom:50%;" />

注：超键和候选键的区别：超键存在多余属性

- 求候选键

<img src="/img/805cae2eb4c2e1211dffa25741ca0e8.png" alt="805cae2eb4c2e1211dffa25741ca0e8" style="zoom:50%;" />

- 例题<img src="/img/fb1fdeffe0703ff44e18cd89d6b5849.png" alt="fb1fdeffe0703ff44e18cd89d6b5849" style="zoom:50%;" />

#### 4.5.4 范式

- 概念

 <img src="/img/214cd9380b7a29ae9df821fd5278754.png" alt="214cd9380b7a29ae9df821fd5278754" style="zoom:50%;" />

- 第一范式

<img src="/img/ecd36c95aa4368d92c9f2ce34778026.png" alt="ecd36c95aa4368d92c9f2ce34778026" style="zoom:50%;" />

- 第二范式

<img src="/img/eb3ff4e052d3b722d66d7bef7e70f8d.png" alt="eb3ff4e052d3b722d66d7bef7e70f8d" style="zoom:50%;" />

- 第三范式

<img src="/img/f6afe23e3ad403e66a8184dd4272e57.png" alt="f6afe23e3ad403e66a8184dd4272e57" style="zoom:50%;" />

- BC范式

<img src="/img/e89a59a90968afc84a4cc4e5c9d7f4c.png" alt="e89a59a90968afc84a4cc4e5c9d7f4c" style="zoom:50%;" />

注：满足BC范式的函数依赖的左边部分都是候选码（上图T->J不符合条件，因为T不是候选码，候选码有ST、SJ）。

- 例题

<img src="/img/b840e3d6ce75e026cb0947636c16558.png" alt="b840e3d6ce75e026cb0947636c16558" style="zoom:50%;" />

#### 4.5.5 模式分解

- 保持函数依赖分解

<img src="img/image-20220512204618873.png" alt="image-20220512204618873" style="zoom:50%;" />

注：分解之后的R1、R2...Rn包含原来的R的所有函数依赖。

- 无损分解

<img src="img/image-20220512204812763.png" alt="image-20220512204812763" style="zoom:50%;" />

- 判别无损分解的方法

1. 列表法

<img src="img/image-20220512204930862.png" alt="image-20220512204930862" style="zoom:50%;" />

<img src="img/image-20220512205117708.png" alt="image-20220512205117708" style="zoom:50%;" />

注：红色表示分解之后的各关系中的属性，若能通过其他关系补全则说明为无损分解。

2. 集合推导

<img src="img/image-20220512205509137.png" alt="image-20220512205509137" style="zoom:50%;" />

注：该方法只适合两个属性分解的情景，根据条件推导出R1->R2和R2->R1，若有其中一个属于函数依赖中的一项，则为无损分解。

### 4.6 并发控制

- 概念

<img src="img/image-20220512210433139.png" alt="image-20220512210433139" style="zoom:50%;" />

- 存在的问题

<img src="img/image-20220512210500646.png" alt="image-20220512210500646" style="zoom:50%;" />

- 封锁协议

<img src="img/image-20220512210523453.png" alt="image-20220512210523453" style="zoom:50%;" />

### 4.7 完整性约束

<img src="img/image-20220512211546003.png" alt="image-20220512211546003" style="zoom:50%;" />

### 4.8 数据库安全

<img src="img/image-20220512211716620.png" alt="image-20220512211716620" style="zoom:50%;" />

### 4.9 数据备份

<img src="img/image-20220512212702617.png" alt="image-20220512212702617" style="zoom:50%;" />

<img src="img/image-20220512212721046.png" alt="image-20220512212721046" style="zoom:50%;" />

注：差量备份是相对于完全备份。

### 4.10 数据库故障与恢复

<img src="img/image-20220512212825253.png" alt="image-20220512212825253" style="zoom:50%;" />

### 4.11 数据仓库与数据挖掘

<img src="img/image-20220512212919931.png" alt="image-20220512212919931" style="zoom:50%;" />

<img src="img/image-20220512213557488.png" alt="image-20220512213557488" style="zoom:50%;" />

### 4.12 反规范化

<img src="img/image-20220512214031393.png" alt="image-20220512214031393" style="zoom:50%;" />

### 4.13 大数据

<img src="img/image-20220512214336275.png" alt="image-20220512214336275" style="zoom:50%;" />

## 5. 计算机网络

### 5.1 七层模型

- 概念

<img src="img/image-20220516111515729.png" alt="image-20220516111515729" style="zoom:50%;" />

- 例题

<img src="img/image-20220516111620536.png" alt="image-20220516111620536" style="zoom:50%;" />

注：全局广播只能在局域网中，所以在网络层及以上使用的设备都不能通过。

### 5.2 网络技术标准与协议

#### 5.2.1 概念

<img src="img/image-20220516115116752.png" alt="image-20220516115116752" style="zoom:50%;" />

- Samba、CIFS和NFS三种协议可以使用TCP和UDP实现。

#### 5.2.2 DHCP协议

<img src="img/image-20220516115333411.png" alt="image-20220516115333411" style="zoom:50%;" />

- 当分配到**169.254.X.X**或**0.0.0.0**时说明IP分配失败，因为上述两个IP均为假IP，不能用于互联网通信。

#### 5.2.3 DNS协议

<img src="img/image-20220516115459218.png" alt="image-20220516115459218" style="zoom:50%;" />

- 迭代查询：由目标客户机请求本地域名服务器，然后本地域名服务器分别从根域名服务器、顶级域名服务器、权限域名服务器等自顶向下查询域名对应的IP地址。

<img src="img/image-20220516115731431.png" alt="image-20220516115731431" style="zoom:50%;" />

- 递归查询：由目标客户机请求本地域名服务器，然后本地域名服务器请求根域名服务器，根域名服务器请求下一层的顶级域名服务器，逐步向下层查询直到查询到为止，查询之后逐层返回查询结果。

- 例题

<img src="img/image-20220516120103513.png" alt="image-20220516120103513" style="zoom:50%;" />

#### 5.2.4 TCP协议

<img src="img/image-20220516120435180.png" alt="image-20220516120435180" style="zoom:50%;" />

### 5.3 网络类型与拓扑结构

<img src="img/image-20220516204817432.png" alt="image-20220516204817432" style="zoom:50%;" />

### 5.4 网络规划与设计

<img src="img/image-20220516205441141.png" alt="image-20220516205441141" style="zoom:50%;" />

#### 5.4.1 逻辑网络设计

<img src="img/image-20220516205531781.png" alt="image-20220516205531781" style="zoom:50%;" />

#### 5.4.2 物理网络设计

<img src="img/image-20220516205613887.png" alt="image-20220516205613887" style="zoom:50%;" />

#### 5.4.3 分层设计

<img src="img/image-20220516205657379.png" alt="image-20220516205657379" style="zoom:50%;" />

### 5.5 IP地址与子网划分

#### 5.5.1 IP地址分类

<img src="img/image-20220517133424645.png" alt="image-20220517133424645" style="zoom:50%;" />

注：全0和全1地址一般不使用，计算地址数量时需减2。

#### 5.5.2 子网划分

<img src="img/image-20220517133648983.png" alt="image-20220517133648983" style="zoom:50%;" />

注：子网号可以使用全0和全1。

- 例题

<img src="img/image-20220517134052691.png" alt="image-20220517134052691" style="zoom:50%;" />

#### 5.5.3 无分类编址（无类域间路由）

<img src="img/image-20220517133857859.png" alt="image-20220517133857859" style="zoom:50%;" />

- 例题

<img src="img/image-20220517134125525.png" alt="image-20220517134125525" style="zoom:50%;" />

#### 5.5.4 特殊含义的IP地址

<img src="img/image-20220517134802173.png" alt="image-20220517134802173" style="zoom:50%;" />

### 5.6 HTML

<img src="img/image-20220517135113771.png" alt="image-20220517135113771" style="zoom:50%;" />

### 5.7 无线网

<img src="img/image-20220517135518403.png" alt="image-20220517135518403" style="zoom:50%;" />

### 5.8 网络接入技术

<img src="img/image-20220517140217618.png" alt="image-20220517140217618" style="zoom:50%;" />

- TDD为时分复用技术（基于TD-SCDMA），FDD为频分复用技术（基于WCDMA）。

### 5.9 IPv6

<img src="img/image-20220517141149131.png" alt="image-20220517141149131" style="zoom:50%;" />

## 6. 系统安全分析与设计

### 6.1 信息系统安全属性

<img src="img/image-20220517141605524.png" alt="image-20220517141605524" style="zoom:50%;" />

### 6.2 对称加密与非对称加密

- 对称加密技术

<img src="img/image-20220517142744951.png" alt="image-20220517142744951" style="zoom:50%;" />

- 非对称加密技术

<img src="img/image-20220517142714769.png" alt="image-20220517142714769" style="zoom:50%;" />

### 6.3 信息摘要

<img src="img/image-20220517143230893.png" alt="image-20220517143230893" style="zoom:50%;" />

### 6.4 数字签名

<img src="img/image-20220517172441918.png" alt="image-20220517172441918" style="zoom:50%;" />

### 6.5 数字信封与PGP

<img src="img/image-20220517173413737.png" alt="image-20220517173413737" style="zoom:50%;" />

- 练习题

<img src="img/image-20220517174633238.png" alt="image-20220517174633238" style="zoom:50%;" />

### 6.6 网络安全

#### 6.6.1 各个网络层次的安全保障

<img src="img/image-20220517174903684.png" alt="image-20220517174903684" style="zoom:50%;" />

注意：SSL适用于多个网络层级。

#### 6.6.2 网络威胁与攻击

<img src="img/image-20220517175400866.png" alt="image-20220517175400866" style="zoom:50%;" />

<img src="img/image-20220517175704554.png" alt="image-20220517175704554" style="zoom:50%;" />

#### 6.6.3 防火墙

<img src="img/image-20220517175811498.png" alt="image-20220517175811498" style="zoom:50%;" />

## 7. 数据结构与算法

### 7.1 数组

<img src="img/image-20220518154915350.png" alt="image-20220518154915350" style="zoom:50%;" />

- 例题

<img src="img/image-20220518154930876.png" alt="image-20220518154930876" style="zoom:50%;" />

  答：存储地址=a + (5 x 2 + 3) x 2 = a + 26。

### 7.2 稀疏矩阵

<img src="img/image-20220518155609823.png" alt="image-20220518155609823" style="zoom:50%;" />

- 例题

<img src="img/image-20220518155634247.png" alt="image-20220518155634247" style="zoom:50%;" />

注：推荐使用代入法求解。

### 7.3 数据结构的定义

<img src="img/image-20220518155841033.png" alt="image-20220518155841033" style="zoom:50%;" />

### 7.4 线性表

#### 7.4.1 顺序表和链表

<img src="img/image-20220518160639856.png" alt="image-20220518160639856" style="zoom:50%;" />

<img src="img/image-20220518160601482.png" alt="image-20220518160601482" style="zoom:50%;" />

注：主要掌握单链表结点的操作步骤。

#### 7.4.2 顺序存储与链式存储

<img src="img/image-20220518162232879.png" alt="image-20220518162232879" style="zoom:50%;" />

#### 7.4.3 队列与栈

<img src="img/image-20220518163441000.png" alt="image-20220518163441000" style="zoom:50%;" />

1. **tail**指针在最后一个元素的下一位。

2. 为避免队空和队满的条件一致，即**head=tail**，通常最后一个空间不存放元素。

- 例题

<img src="img/image-20220518163655495.png" alt="image-20220518163655495" style="zoom:50%;" />

注：推荐使用排除法和代入法解题。

### 7.5 广义表

<img src="img/image-20220518164215674.png" alt="image-20220518164215674" style="zoom:50%;" />

1. **表尾**是除了第一个表元素的所有元素的组合。
2. **宽度**为表元素的个数，**深度**为括号嵌套的次数。

3. 取出元素时通过**head**和**tail**步骤进行逐层取出。

### 7.6 树与二叉树

#### 7.6.1 基本概念

<img src="img/image-20220518165425084.png" alt="image-20220518165425084" style="zoom:50%;" />

1. 结点的度：当前结点的子结点个数
2. 树的度：所有结点的度的最大值
3. 叶子结点：没有子结点的结点
4. 分支结点：含有分支的结点
5. 内部结点：非根结点与叶子结点的结点（中间的结点）
6. 父、子结点：相对于某几个结点而言
7. 兄弟结点：相对于某几个结点而言，两个结点处于同一层且归属于同个父节点

#### 7.6.2 满二叉树与完全二叉树

<img src="img/image-20220518170937862.png" alt="image-20220518170937862" style="zoom:50%;" />

1. 满二叉树：每个非叶子结点都含有两个子结点
2. 完全二叉树：结点以广度优先的方式进行放置，最后一层可能不放满

#### 7.6.3 二叉树遍历

<img src="img/image-20220519102253260.png" alt="image-20220519102253260" style="zoom:50%;" />

1. 前序遍历：根->左->右
2. 中序遍历：左->根->右
3. 后序遍历：左->右->根
4. 层次遍历：一层一层由左到右进行遍历

#### 7.6.4 反向构造二叉树（主要考察前中/中后序推出二叉树）

<img src="img/image-20220519102900439.png" alt="image-20220519102900439" style="zoom:50%;" />

<img src="img/image-20220519103042748.png" alt="image-20220519103042748" style="zoom:50%;" />

1. 先从前序/后序遍历确定根结点，再结合中序遍历确定左右结点
2. 重复以上步骤，直到确定全部结点

#### 7.6.5 树转二叉树

<img src="img/image-20220519103735492.png" alt="image-20220519103735492" style="zoom:50%;" />

#### 7.6.6 查找二叉树

<img src="img/image-20220519104322316.png" alt="image-20220519104322316" style="zoom:50%;" />

#### 7.6.7 最优二叉树（哈夫曼树）

<img src="img/image-20220519104449289.png" alt="image-20220519104449289" style="zoom:50%;" />

1. 树的路径长度：树的所有路径长度之和
2. 权：在结点上有一个数值代表某一种字符出现的频度

3. 带权路径长度：（结点距离根节点的路径长度）*权值

4. 树的带权路径长度（树的代价）：树每个结点（叶子结点）的带权路径长度之和

#### 7.6.8 线索二叉树

<img src="img/image-20220519110816681.png" alt="image-20220519110816681" style="zoom:50%;" />

- 线索二叉树：利用结点中的空指针位置放置特定遍历方式的前驱（左指针）和后继（右指针）结点的地址。

#### 7.6.9 平衡二叉树

<img src="img/image-20220519111356040.png" alt="image-20220519111356040" style="zoom:50%;" />

- 平衡二叉树：保证每个结点的**平衡度**只能为**-1**、**0**或**1**，**平衡度=左子树深度 - 右子树深度**。

### 7.7 图

#### 7.7.1 基本概念

<img src="img/image-20220519141206595.png" alt="image-20220519141206595" style="zoom:50%;" />

#### 7.7.2 图的存储

- 邻接矩阵

<img src="img/image-20220519141400666.png" alt="image-20220519141400666" style="zoom:50%;" />

- 邻接表

<img src="img/image-20220519141430524.png" alt="image-20220519141430524" style="zoom:50%;" />

#### 7.7.3 图的遍历

<img src="img/image-20220519141933136.png" alt="image-20220519141933136" style="zoom:50%;" />

<img src="img/image-20220519142001787.png" alt="image-20220519142001787" style="zoom:50%;" />

#### 7.7.4 拓扑排序

<img src="img/image-20220519142236253.png" alt="image-20220519142236253" style="zoom:50%;" />

#### 7.7.5 最小生成树

- 普里姆算法

<img src="img/image-20220519171734657.png" alt="image-20220519171734657" style="zoom:50%;" />

1. 选取一个点放入一个集合
2. 计算该集合中各个点到其他未连接的点的距离
3. 选择最小距离的点，连接，并将其放入集合中
4. 重复第2-3步骤直到所有的点均已连接（注意：连接过程中不能形成环路）

- 克鲁斯卡尔算法

<img src="img/image-20220519172041756.png" alt="image-20220519172041756" style="zoom:50%;" />

1. 找出未连接的最小距离的边
2. 连接
3. 重复第1-2步骤直到所有的点均已连接（注意：连接过程中不能形成环路）

### 7.8 算法基础

#### 7.8.1 算法的特性

<img src="img/image-20220519172258526.png" alt="image-20220519172258526" style="zoom:50%;" />

#### 7.8.2 算法的复杂度

<img src="img/image-20220519172434768.png" alt="image-20220519172434768" style="zoom:50%;" />

### 7.9 查找

#### 7.9.1 顺序查找

<img src="img/image-20220519173648576.png" alt="image-20220519173648576" style="zoom:50%;" />

#### 7.9.2 二分查找

- 思想与步骤

<img src="img/image-20220519174111301.png" alt="image-20220519174111301" style="zoom:50%;" />

- 例题

<img src="img/image-20220519174007206.png" alt="image-20220519174007206" style="zoom:50%;" />

#### 7.9.3 散列表

<img src="img/image-20220519175058502.png" alt="image-20220519175058502" style="zoom:50%;" />

- 线性探测法：若发生冲突则往下一个地址探测，直到找到第一个空的位置将其置入。

### 7.10 排序

#### 7.10.1 概念与分类

<img src="img/image-20220519175616508.png" alt="image-20220519175616508" style="zoom:50%;" />

- 稳定排序与不稳定排序的区别：前者对于相等的元素不会改变原顺序，造成不必要的操作。

#### 7.10.2 直接插入排序

<img src="img/image-20220520100118284.png" alt="image-20220520100118284" style="zoom:50%;" />

#### 7.10.3 希尔排序

<img src="img/image-20220520100652641.png" alt="image-20220520100652641" style="zoom:50%;" />

#### 7.10.4 直接选择排序

<img src="img/image-20220520100858017.png" alt="image-20220520100858017" style="zoom:50%;" />

#### 7.10.5 堆排序

- 堆的概念

<img src="img/image-20220520101844643.png" alt="image-20220520101844643" style="zoom:50%;" />

- 初堆的建立

<img src="img/image-20220520102014984.png" alt="image-20220520102014984" style="zoom:50%;" />

1. 从后到前选择分支结点对应的子树，对比其根节点与子节点的大小，按照条件进行交换；
2. 交换过程如果使得其他子树不满足堆的条件也需要进行调整；
3. 重复以上步骤，直到所有子树满足堆的条件，即初堆构建完成。

- 堆排序

<img src="img/image-20220520102316534.png" alt="image-20220520102316534" style="zoom:50%;" />

1. 取出最小/大的元素（即树的根节点），然后将最后一个结点移动到根结点；
2. 按照堆的条件对新形成的二叉树进行调整；
3. 重复以上步骤，直到所有元素均全部取出，即堆排序完成。

#### 7.10.6 冒泡排序

<img src="img/image-20220520102737166.png" alt="image-20220520102737166" style="zoom:50%;" />

#### 7.10.7 快速排序

<img src="img/image-20220520103143657.png" alt="image-20220520103143657" style="zoom:50%;" />

#### 7.10.8 归并排序

<img src="img/image-20220520103701561.png" alt="image-20220520103701561" style="zoom:50%;" />

#### 7.10.9 基数排序

<img src="img/image-20220520104048612.png" alt="image-20220520104048612" style="zoom:50%;" />

#### 7.10.10 排序算法的时间和空间复杂度

<img src="img/image-20220520104129046.png" alt="image-20220520104129046" style="zoom:50%;" />

## 8. 程序设计语言与语言处理程序

### 8.1 编译与解释

- 编译过程

<img src="img/image-20220520105848737.png" alt="image-20220520105848737" style="zoom:50%;" />

### 8.2 文法

- 定义

<img src="img/image-20220520110327356.png" alt="image-20220520110327356" style="zoom:50%;" />

<img src="img/image-20220520110404570.png" alt="image-20220520110404570" style="zoom:50%;" />

- 语法推导树

<img src="img/image-20220520110516237.png" alt="image-20220520110516237" style="zoom:50%;" />

### 8.3 正规式（必考）

<img src="img/image-20220520112125399.png" alt="image-20220520112125399" style="zoom:50%;" />

- 例题

<img src="img/image-20220520112155194.png" alt="image-20220520112155194" style="zoom:50%;" />

<img src="img/image-20220520112227642.png" alt="image-20220520112227642" style="zoom:50%;" />

### 8.4 有限自动机

<img src="img/image-20220520111212995.png" alt="image-20220520111212995" style="zoom:50%;" />

- 例题

<img src="img/image-20220520113004055.png" alt="image-20220520113004055" style="zoom:50%;" />

### 8.5 表达式（必考）

<img src="img/image-20220520113305892.png" alt="image-20220520113305892" style="zoom:50%;" />

注意：括号不能构造到树中，只表达计算的优先级顺序。

### 8.6 传值与传址（必考）

<img src="img/image-20220520113847899.png" alt="image-20220520113847899" style="zoom:50%;" />

### 8.7 各种程序语言特点

<img src="img/image-20220520113915079.png" alt="image-20220520113915079" style="zoom:50%;" />

## 9. 法律法规知识（2~3分）

### 9.1 内容概要

<img src="img/image-20220522160857173.png" alt="image-20220522160857173" style="zoom:50%;" />

- 邻接权：保护除了作者以外的第三方的权益，如出版商。

### 9.2 保护期限

<img src="img/image-20220522161644007.png" alt="image-20220522161644007" style="zoom:50%;" />

### 9.3 知识产权人的确定

<img src="img/image-20220522162925537.png" alt="image-20220522162925537" style="zoom:50%;" />

### 9.4 侵权判定

<img src="img/image-20220522163734418.png" alt="image-20220522163734418" style="zoom:50%;" />

<img src="img/image-20220522163753619.png" alt="image-20220522163753619" style="zoom:50%;" />

### 9.5 标准化

#### 9.5.1 标准的分类

<img src="img/image-20220522164124551.png" alt="image-20220522164124551" style="zoom:50%;" />

<img src="img/image-20220522164152089.png" alt="image-20220522164152089" style="zoom:50%;" />

## 10. 多媒体基础（1~3分）

### 10.1 音频相关概念

<img src="img/image-20220522165209004.png" alt="image-20220522165209004" style="zoom:50%;" />

### 10.2 图像相关概念

<img src="img/image-20220522165825500.png" alt="image-20220522165825500" style="zoom:50%;" />

<img src="img/image-20220522165745024.png" alt="image-20220522165745024" style="zoom:50%;" />

1. CMY：应用于印刷
2. HSV：应用于艺术

### 10.3 媒体的种类

<img src="img/image-20220522170026559.png" alt="image-20220522170026559" style="zoom:50%;" />

### 10.4 多媒体相关计算问题

<img src="img/image-20220522171046780.png" alt="image-20220522171046780" style="zoom:50%;" />

- 例题

<img src="img/image-20220522171139465.png" alt="image-20220522171139465" style="zoom:50%;" />

### 10.5 常见多媒体标准

<img src="img/image-20220522171519094.png" alt="image-20220522171519094" style="zoom:50%;" />

### 10.6 数据压缩基础

<img src="img/image-20220522172021095.png" alt="image-20220522172021095" style="zoom:50%;" />

### 10.7 有损压缩与无损压缩

<img src="img/image-20220522172326349.png" alt="image-20220522172326349" style="zoom:50%;" />

## 11. 软件工程

### 11.1 软件开发模型

#### 11.1.1 瀑布模型（SDLC）

<img src="img/image-20220522172628944.png" alt="image-20220522172628944" style="zoom:50%;" />

- 应用场景：结构化开发
- 适合场景：需求明确、二次开发

#### 11.1.2 原型模型

<img src="img/image-20220522173434755.png" alt="image-20220522173434755" style="zoom:50%;" />

- 开发时做出简易系统或者界面形成原型与用户进行沟通修正需求。

#### 11.1.3 增量模型与螺旋模型

<img src="img/image-20220522173607686.png" alt="image-20220522173607686" style="zoom:50%;" />

- 增量模型：核心功能先完成，其他次要功能一层一层实现，最后实现一个完整的产品。

- 螺旋模型：整合了原型模型等各种开发模型，主要特点是增加了**风险分析**。

#### 11.1.4 V模型、喷泉模型、RAD

<img src="img/image-20220522174209878.png" alt="image-20220522174209878" style="zoom:50%;" />

- V模型：把测试分成几个类型，并将开发与测试的过程结合进行
- 喷泉模型：面向对象的开发模型
- RAD（快速开发模型）：结合瀑布模型和构件化开发模型

#### 11.1.5 构件组装模型（CBSD）

<img src="img/image-20220522175032423.png" alt="image-20220522175032423" style="zoom:50%;" />

#### 11.1.6 统一过程（UP/RUP）

<img src="img/image-20220522175551204.png" alt="image-20220522175551204" style="zoom:50%;" />

#### 11.1.7 敏捷开发方法

<img src="img/image-20220522180045435.png" alt="image-20220522180045435" style="zoom:50%;" />

### 11.2 信息系统开发方法

<img src="img/image-20220522180743875.png" alt="image-20220522180743875" style="zoom:50%;" />

### 11.3 需求开发

<img src="img/image-20220522205618654.png" alt="image-20220522205618654" style="zoom:50%;" />

- 分类
  - 业务需求：系统需要实现哪些具体业务
  - 用户需求：不同用户角色对该系统的需求
  - 系统需求：系统要实现哪些具体需求，该需求可为后续开发做参考

- QFD
  - 基本需求：客户需要该系统实现的最基本的需求
  - 期望需求：客户没有告知开发者需要实现的需求但是是必须实现的需求
  - 兴奋需求：客户没想到的需求或者系统不太需要的需求

### 11.4 结构化设计

 #### 11.4.1 基本原则

<img src="img/image-20220522210734315.png" alt="image-20220522210734315" style="zoom:50%;" />

#### 11.4.2 内聚和耦合

<img src="img/image-20220522210819118.png" alt="image-20220522210819118" style="zoom:50%;" />

#### 11.4.3 系统结构/模块结构

<img src="img/image-20220522210854854.png" alt="image-20220522210854854" style="zoom:50%;" />

### 11.5 软件测试

#### 11.5.1 测试原则与类型

<img src="img/image-20220522211539622.png" alt="image-20220522211539622" style="zoom:50%;" />

#### 11.5.2 测试用例设计

<img src="img/image-20220522213834985.png" alt="image-20220522213834985" style="zoom:50%;" />

<img src="img/image-20220522220616591.png" alt="image-20220522220616591" style="zoom:50%;" />

#### 11.5.3 McCabe复杂度

<img src="img/image-20220522221456435.png" alt="image-20220522221456435" style="zoom:50%;" />

#### 11.5.4 系统运行与维护

<img src="img/image-20220522221752536.png" alt="image-20220522221752536" style="zoom:50%;" />

- 适应性维护：能适应操作系统、数据库等升级的维护
- 完善性维护：能逐步完善系统的功能的维护
- 预防性维护：对未来即将出现的错误进行修正的维护

### 11.6 软件过程改进—CMMI

<img src="img/image-20220522224307520.png" alt="image-20220522224307520" style="zoom:50%;" />

### 11.7 项目管理（2-3分）

<img src="img/image-20220522225353307.png" alt="image-20220522225353307" style="zoom:50%;" />

- 例题

<img src="img/image-20220522225433004.png" alt="image-20220522225433004" style="zoom:50%;" />

1. PERT图先计算出各个任务的最早开始时间，然后从最后一个任务逆推出最晚开始时间。

<img src="img/image-20220522225616247.png" alt="image-20220522225616247" style="zoom:50%;" />

## 12. 面向对象技术（OOA）

### 12.1 基本概念

<img src="img/image-20220522225921326.png" alt="image-20220522225921326" style="zoom:50%;" />

- 边界类：负责与外部系统链接的类

### 12.2 设计原则

<img src="img/image-20220522230442222.png" alt="image-20220522230442222" style="zoom:50%;" />

- 李氏替换原则：子类尽可能不要去重载父类的方法（即修改父类的具体实现方法）

### 12.3 UML

<img src="img/image-20220522231444932.png" alt="image-20220522231444932" style="zoom:50%;" />

- 部署图：反映系统部署在硬件的关系
- 用例图：反映系统与外部人员的交互关系

- 顺序图/序列图：着重时间顺序
- 通信图/协作图：没有时间顺序
- 状态图：反映状态的变迁和转移
- 活动图：与流程图结构一致

### 12.4 设计模式的概念

<img src="img/image-20220522232103433.png" alt="image-20220522232103433" style="zoom:50%;" />

### 12.5 设计模式的分类

<img src="img/image-20220523123312441.png" alt="image-20220523123312441" style="zoom:50%;" />

### 12.6 创建型模式

<img src="img/image-20220523123712514.png" alt="image-20220523123712514" style="zoom:50%;" />

### 12.7 结构型模式

<img src="img/image-20220523124718547.png" alt="image-20220523124718547" style="zoom:50%;" />

### 12.8 行为型模式

<img src="img/image-20220523131959734.png" alt="image-20220523131959734" style="zoom:50%;" />

<img src="img/image-20220523132031832.png" alt="image-20220523132031832" style="zoom:50%;" />

## 13. 数据流图（DFD）（下午第1题15分）

### 13.1 基本概念

<img src="img/image-20220523133224986.png" alt="image-20220523133224986" style="zoom:50%;" />

<img src="img/image-20220523133540110.png" alt="image-20220523133540110" style="zoom:50%;" />

### 13.2 数据字典

<img src="img/image-20220523134057059.png" alt="image-20220523134057059" style="zoom:50%;" />

### 13.3 数据流图平衡原则

<img src="img/image-20220523135355374.png" alt="image-20220523135355374" style="zoom:50%;" />

- 父图与子图之间的平衡

<img src="img/image-20220523135427747.png" alt="image-20220523135427747" style="zoom:50%;" />

### 13.4 答题技巧

<img src="img/image-20220523140041899.png" alt="image-20220523140041899" style="zoom:50%;" />

### 13.5 例题一

- 问题

<img src="img/image-20220523141136716.png" alt="image-20220523141136716" style="zoom:50%;" />

<img src="img/image-20220523141159360.png" alt="image-20220523141159360" style="zoom:50%;" />

<img src="img/image-20220523141310806.png" alt="image-20220523141310806" style="zoom:50%;" />

- 答案

1. 题解1

<img src="img/image-20220523141413544.png" alt="image-20220523141413544" style="zoom:50%;" />

2. 题解2

<img src="img/image-20220523141503334.png" alt="image-20220523141503334" style="zoom:50%;" />

3. 题解3

<img src="img/image-20220523141548935.png" alt="image-20220523141548935" style="zoom:50%;" />

4. 题解4

- 出现的错误：黑洞（有入没出）、奇迹（有出没入）、数据流命名问题（输入和输出同名）和输入流和输出流不匹配等等

### 13.6 例题二

- 问题

<img src="img/image-20220523144500911.png" alt="image-20220523144500911" style="zoom:50%;" />

<img src="img/image-20220523144518212.png" alt="image-20220523144518212" style="zoom:50%;" />

<img src="img/image-20220523144544510.png" alt="image-20220523144544510" style="zoom:50%;" />

- 答案

1. 题解1

<img src="img/image-20220523144656109.png" alt="image-20220523144656109" style="zoom:50%;" />

2. 题解2

<img src="img/image-20220523144744248.png" alt="image-20220523144744248" style="zoom:50%;" />

3. 题解3

<img src="img/image-20220523144853415.png" alt="image-20220523144853415" style="zoom:50%;" />

4. 题解4

- P1：交易信息管理
- P2：客户信息管理
- P3：信用卡激活
- P4：信用卡申请

## 14. 数据库设计（15分）

### 14.1 数据库设计过程

<img src="img/image-20220523163434573.png" alt="image-20220523163434573" style="zoom:50%;" />

### 14.2 ER模型

- 实体间联系类型

<img src="img/image-20220523163826857.png" alt="image-20220523163826857" style="zoom:50%;" />

- ER模型转换为关系模型

<img src="img/image-20220523163907562.png" alt="image-20220523163907562" style="zoom:50%;" />

### 14.3 例题一

- 题目

<img src="img/image-20220523164118598.png" alt="image-20220523164118598" style="zoom:50%;" />

<img src="img/image-20220523164138175.png" alt="image-20220523164138175" style="zoom:50%;" />

<img src="img/image-20220523164153251.png" alt="image-20220523164153251" style="zoom:50%;" />

<img src="img/image-20220523164214585.png" alt="image-20220523164214585" style="zoom:50%;" />

- 答案

1. 客房和客户为m：n关系

4. 优点：查询时不用进行联接查询权限表，使查询速度加快；缺点：员工表权限属性数据会重复出现，造成冗余

### 14.4 例题二

<img src="img/image-20220523165357658.png" alt="image-20220523165357658" style="zoom:50%;" />

<img src="img/image-20220523165416285.png" alt="image-20220523165416285" style="zoom:50%;" />

<img src="img/image-20220523165433291.png" alt="image-20220523165433291" style="zoom:50%;" />

<img src="img/image-20220523165449651.png" alt="image-20220523165449651" style="zoom:50%;" />

<img src="img/image-20220523165508536.png" alt="image-20220523165508536" style="zoom:50%;" />

- 答案

1. 题解1

<img src="img/image-20220523165536016.png" alt="image-20220523165536016" style="zoom:50%;" />

2. 题解2

<img src="img/image-20220523170324454.png" alt="image-20220523170324454" style="zoom:50%;" />

3. 题解3

<img src="img/image-20220523170201796.png" alt="image-20220523170201796" style="zoom:50%;" />

## 15. UML建模

