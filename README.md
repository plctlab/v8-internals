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

## V8 相关的技术分享和资源

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
