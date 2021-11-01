# 深入V8引擎

面向想要成为 Google V8 开发人员的MOOC。

V8 是 Google Chrome 浏览器和微软 Edge 浏览器的 JavaScript 执行引擎。本课程介绍如何成为 V8 的开发人员。注意这是硬核技术培训，每次视频请预留10个小时的上机编程练习时间。

NOTICE: 目前处于连载状态，预计连续更新到2020年底。
可以关注B站 [@lazypaser](https://space.bilibili.com/296494084) 接收课程更新的推送。

课件（Slides）、开源电子书、配套代码及相关资料存放在本仓库：

https://github.com/lazyparser/v8-internals

我们从2020年4月开始逐步对V8官方博客进行评论和内容有效性的梳理，请参考 [v8-blog-comments.md](v8-blog-comments.md)，
同时我们非常欢迎提交 Pull Request 分享你的文章或评论。

## 课程视频和幻灯片列表

|Video|Slides|Author|Title|
|----|----|----|----|
|[av83746754](https://www.bilibili.com/video/av83746754)|[01.pdf](https://github.com/lazyparser/v8-internals/blob/master/slides/01-igniton-bytecode-dump.pdf)|吴伟|第01课：上手开始看 V8 Ignition 解释器的字节码（Bytecodes）|
|[av87260107](https://www.bilibili.com/video/av87260107)|[02.pdf](https://github.com/lazyparser/v8-internals/blob/master/slides/02-v8-build-system-part1.pdf)|邱吉|第02课：从零开始分析V8的构建系统构成|
|[av89142028](https://www.bilibili.com/video/av89142028)|[03.pdf](https://github.com/lazyparser/v8-internals/blob/master/slides/03-v8-build-system-part2.pdf)|邱吉|第03课：V8的构建系统构成Part2|
|[BV1N7411N73m](https://www.bilibili.com/video/BV1N7411N73m)|[04.pdf](https://github.com/lazyparser/v8-internals/blob/master/slides/04-v8-build-system-part3.pdf)|邱吉|第04课：V8的构建系统构成Part3|
|TBD|TBD|吴伟|第05课：TBD，Ignition Bytecodes 解析|
|TBD|TBD|吴伟|第06课：TBD，torque|
|TBD|TBD|吴伟|第07课：TBD，torque|
|TBD|TBD|邱吉|第08课：TBD|

## 淦！移植个V8不可能这么难！
|Video|Slides|Author|Title|
|----|----|----|----|
|[BV1hp4y1t7Mx](https://www.bilibili.com/video/BV1hp4y1t7Mx?p=1)|[01.pdf](https://github.com/plctlab/v8-internals/blob/master/slides/V8-security-spectre-mitigation.pdf)|20210416 - 邱吉 - Security Strategies in V8: Spectre漏洞的防御|
|[BV1hp4y1t7Mx](https://www.bilibili.com/video/BV1hp4y1t7Mx?p=2)|[02.pdf](https://github.com/plctlab/v8-internals/blob/master/slides/v8%E4%B8%ADLinearScanRegisterAllocation%E7%9A%84%E4%BC%AA%E4%BB%A3%E7%A0%81%E5%92%8C%E6%BA%90%E7%A0%81%E5%88%86%E6%9E%90.pdf)|20210430 - 陆亚涵 - LinearScanRegisterAllocation 算法分析|
|[BV1hp4y1t7Mx](https://www.bilibili.com/video/BV1hp4y1t7Mx?p=3)|[03.pdf](https://github.com/plctlab/v8-internals/blob/master/slides/V8-constant-pool.pdf)|20210514 - 邱吉 - V8后端代码生成：常量池及其实现|
|[BV1hp4y1t7Mx](https://www.bilibili.com/video/BV1hp4y1t7Mx?p=4)|[04.pdf](https://docs.google.com/presentation/d/1LquBZxASLtkYMaI5DKmDLK2IyDgM6N61Y8XEOseoVl4/edit?usp=sharing)|20210528- 陆亚涵 - trampoline 和 Embedd Builtins|
|[BV1hp4y1t7Mx](https://www.bilibili.com/video/BV1hp4y1t7Mx?p=3)|[05.pdf](https://github.com/plctlab/v8-internals/blob/master/slides/V8-test-framework.pdf)|20210613 - 邱吉 - 学习V8的测试框架|
|[BV1hp4y1t7Mx](https://www.bilibili.com/video/BV1hp4y1t7Mx?p=12)|[012.pdf](https://github.com/plctlab/v8-internals/blob/master/slides/V8%E4%B8%AD%E7%9A%84inline%20cache%E5%AE%9E%E7%8E%B0.pdf)|20211031 - 陆亚涵 - v8中的inline cache实现||

## V8 相关的技术分享和资源
v8中LinearScanRegisterAllocation的伪代码和源码分析-陆亚涵-20210430-PLCT实验室

WebAssembly Compilation Pipeline - 姜宇辰 - 20210127 - PLCT实验室

https://www.bilibili.com/video/BV19o4y1R71F

How to debug V8 学习报告 - 梁斌 - 20210113 - PLCT实验室

https://www.bilibili.com/video/BV1jU4y147eD

王建中 - 在 V8 中添加一个 RISC-V B 扩展指令 - 20201216 - PLCT实验室

https://www.bilibili.com/video/BV1Gt4y1k7Bx

陆亚涵：V8中的指针压缩及其实现源码分析【第12届开源开发工具大会（OSDT2020）】

https://www.bilibili.com/video/BV1oK4y1572D

陶立强：V8寄存器分配源码分析——以添加RISCV-C扩展为背景【第12届开源开发工具大会（OSDT2020）】

https://www.bilibili.com/video/BV19X4y1M7Ax

RISC-V V8 移植调试记录：关于一次奇怪的 int32 的值 - 陆亚涵 - 20200801 - PLCT实验室

https://www.bilibili.com/video/BV1SZ4y1T7Rw

V8 for RISC-V 开发小结 - 陈家友 - 20200729 - PLCT实验室

https://www.bilibili.com/video/BV1cD4y1U74R/

RISC-V <3 V8 w/ Keynote: The Roadmap of V8 RISC-V Porting - Peng Wu |OSDT Meetup

https://www.bilibili.com/video/BV1da4y1a7JD

V8中的浮点转整型 - 陆亚涵 - 20200624 - PLCT实验室

https://www.bilibili.com/video/BV1yA411v7m2

V8：几个Torque语句分析 - 杨文章 - 20200610 - PLCT实验室

https://www.bilibili.com/video/BV1sZ4y1W7YQ

V8引擎TurboFan后端代码浅析 - 邱吉 - V8技术讨论会 - OSDT社区 - 20200607

https://www.bilibili.com/video/BV1oZ4y1n7E8

V8中的Snapshot机制分析 - 杨文章 - 20200606 - PLCT实验室

https://www.bilibili.com/video/BV1UV411r7Nq

杨文章-Dive-Into-V8-Torque-PLCT实验室-20200527

https://www.bilibili.com/video/BV1JK411s7Pv

邹小芳-V8移植简介-PLCT实验室-20200527

https://www.bilibili.com/video/BV11K4y1t76G

V8单元测试框架 - 陆亚涵 - 20200513 - PLCT实验室

https://www.bilibili.com/video/BV1pp4y1Q71M

深入V8引擎-技术分享：V8 Assembler 学习小结 - 陈家友

https://www.bilibili.com/video/BV1cc411h747

PLCT实验室分享 - 深入V8引擎：V8 Call Interface Descriptors - 邹小芳

https://www.bilibili.com/video/BV1TE411N7k7

PLCT实验室技术分享-V8解释器字节码代码浅析 - 张江涛

https://www.bilibili.com/video/BV1q741137GB

Sigurd Scheider- Inside V8- The choreography of Ignition and TurboFan

https://www.bilibili.com/video/BV1uJ411H7ok

V8- an open source JavaScript engine

https://www.bilibili.com/video/BV15J411J7sr

BlinkOn 6 Day 1 Talk 2- Ignition - an interpreter for V8

https://www.bilibili.com/video/BV15J411J7Gf

What’s new in JavaScript (Google I-O ’19)[00]

https://www.bilibili.com/video/BV1RJ411J7ZD

Embedding V8 in the real world by Stanimira Vlaeva - JSConf EU 2019

https://www.bilibili.com/video/BV1RJ411J7Wf

Franziska Hinkelmann- JavaScript engines - how do they even? - JSConf EU

https://www.bilibili.com/video/BV1oJ411J7kD

Franziska Hinkelmann - Performance Profiling for V8 - Script17

https://www.bilibili.com/video/BV1RJ411J7Y6

Franziska Hinkelmann- A Trip to the Zoo- SpiderMonkey, SquirrelFish, Nashorn, V8

https://www.bilibili.com/video/BV1oJ411J7z8

Mathias Bynens - V8 internals for JavaScript developers

https://www.bilibili.com/video/BV1oJ411J7j1

JavaScript Engines- The Good Parts™ - Mathias Bynens & Benedikt Meurer - JSConf

https://www.bilibili.com/video/BV1oJ411J72X

Orinoco: The new V8 Garbage Collector Peter Marshall

https://www.bilibili.com/video/BV1TJ411n7pi

Understanding Why The New V8 Is So Fast, One Demo At A Time

https://www.bilibili.com/video/BV1TJ411n78Y

MNUG 2017.03.23 TurboFan: A new code generation architecture for V8

https://www.bilibili.com/video/BV137411e7TQ


### 关于本项目的一些脚注

这个项目的目标是为了写一本书，能够让读者对于 V8 引擎的内部架构和源代码有所了解。
如果你翻阅过本仓库的提交历史，就会注意到这个仓库的首次公开commit可以追溯到2015年。
那个时候我正在念编译技术方向的博士（后来退学了），熟悉了 Spidermonkey 并进行了一些不成功的实验，对 JavaScript 执行引擎有着很高的兴趣。
但是写一个 V8 这种体量的分析是非常苦难的，我只是刚开始就咕咕咕了好几年。以上是第一阶段。

第二阶段则到了2020年，我成立了PLCT实验室，并跟邱吉一起启动了 V8 for RISC-V 的项目。
我们当时谁都没有看过（仔细研究过）V8的源代码，所以很自然的，第一步就是组织小组进行自我学习。
在这个过程中，我们自然的进行组内技术分享，并发送到了B站进行公开。这个过程启发我重新启动了本项目，并期待 V8 小队可以团体写一本书。
在这个过程中我们继续输出了一些技术分享视频、一些零散的文档，之后就奔命于追赶 upstream 的进度，跟FutureWei一起将 RISC-V 后端送入 V8 仓库。
于是又咕了一年。

第三阶段是2021年4月份开始。这个时候写书的权责已经完全落于邱吉的肩上，而此时《V8 Internals》这本书的出版印刷已经注定要跳票半年。
「来不及了，先出门课程吧！」
在2021年春节之后的会议上我这么对邱主管提议到。
于是就有了目前正在B站连载的《淦！移植个V8不可能这么难！》系列讨论班（笑）。
计划是保持最低两周一次技术报告的输出，让我们在追赶 upstream 的同时，能确保自己在写书和公开课这个任务上持续有产出。

由于已经不再是个人项目，本项目于2021年5月12日从 gh/lazyparser/ 移动到了 gh/plctlab 账号下，正式成为PLCT实验室的团队项目。邱吉主管是本项目的 owner。
感谢杨文章同学、陶立强同学即使在实习结束之后依然积极贡献本书的写作。我会敦促新的owner努力赶上进度的 :-P

@lazyparser on 2021-05-12 22:40 CST
