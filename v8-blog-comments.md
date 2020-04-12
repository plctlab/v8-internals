# V8 Blog 的内容同步阅读

Google V8 团队的技术博客（Blog）是理解V8架构和实现细节、后续研发进展的重要的来源。
另一方面，V8的技术实现一直在快速变化，博客内容从2015到2020时间跨度很大，
是否与代码一致，需要读者自己去对比才行。
我们在《深入V8引擎》的repo中记录自己阅读V8博客中的笔记和评论，方便后续我们新加入V8项目的同事理解。

目前的技术评论的时间节点是2020年第二季度。

## V8 Blog

### 100
### 099
### 098
### 097
### 096
### 095
### 094
### 093
### 092
### 091
### 090
### 089
### 088
### 087
### 086
### 085
### 084
### 083
### 082
### 081
### 080
### 079
### 078
### 077
### 076
### 075
### 074
### 073
### 072
### 071
### 070
### 069
### 068
### 067
### 066
### 065
### 064
### 063
### 062
### 061
### 060
### 059
### 058
### 057
### 056
### 055
### 054
### 053
### 052
### 051
### 050 V8 release v6.3
Published 25 October 2017 · tagged with release

可以不看。

### 049 Optimizing ES2015 proxies in V8
Published 05 October 2017 · tagged with ECMAScript benchmarks internals

需要看。

### 048 An internship on laziness: lazy unlinking of deoptimized functions
Published 04 October 2017 · tagged with memory internals

这位同学的PPT很魔性😄推荐看看。

### 047 Temporarily disabling escape analysis
Published 22 September 2017 · tagged with security

不用看了。

### 046 Elements kinds in V8
Published 12 September 2017 · tagged with internals presentations

视频我搬运到了B站，可以组合看下，如果是编译领域从业，对JS不熟悉的话，可以解惑：

Mathias Bynens - V8 internals for JavaScript developers
https://www.bilibili.com/video/BV1oJ411J7j1

### 045 V8 release v6.2
Published 11 September 2017 · tagged with release

不用看。

### 044 Fast properties in V8
Published 30 August 2017 · tagged with internals

需要看。

### 043 About that hash flooding vulnerability in Node.js…
Published 11 August 2017 · tagged with security

不做安全的话不用看，已经过去了。

### 042 V8 release v6.1
Published 03 August 2017 · tagged with release

不用看。


### 041 V8 release v6.0
Published 09 June 2017 · tagged with release

不用看。

### 040 Launching Ignition and TurboFan
Published 15 May 2017 · tagged with internals

第一次接触V8的需要看一下。

那个logo应该不是一个灯笼，是两个火花装置尖端放电？
### 039 V8 release v5.9
Published 27 April 2017 · tagged with release

v5.9 开始启用了 Igniton + TurboFan。

### 038 Retiring Octane
Published 12 April 2017 · tagged with benchmarks

不用看。其实我们还是在用 Octane 的。

### 037 V8 release v5.8
Published 20 March 2017 · tagged with release

可以不看。

### 036 Fast for-in in V8
Published 01 March 2017 · tagged with internals

需要看一下。涉及到 for-in 的内部处理。性能提升部分不用细看，看原理就行。

### 035 High-performance ES2015 and beyond
Published 17 February 2017 · tagged with ECMAScript

不用看。

### 034 Help us test the future of V8!
Published 14 February 2017 · tagged with internals

不用看。

### 033 One small step for Chrome, one giant heap for V8
Published 09 February 2017 · tagged with memory

Dev工具改进，感知内存压力并自动停止，防止对V8的堆造成压力。

我们目前是只做V8的话不用看这篇。以后做Chromium的时候需要关注下是不是还是当前的实现。

### 032 V8 release v5.7
Published 06 February 2017 · tagged with release

启用了 webassemly。 其它主要是性能改进。

### 031 Speeding up V8 regular expressions
Published 10 January 2017 · tagged with internals RegExp

从 v5.7 开始ship新的regexp，从第三方的库实现，转移到了turbofan中，使用CSA形式。

具体RE这部分实现我还没看。目前感觉不需要阅读。

### 030 How V8 measures real-world performance
Published 21 December 2016 · tagged with benchmarks

在做性能测试之前需要阅读下这篇博客，给出了比技术分享视频更加简洁的 brief history。

### 029 V8 ❤️ Node.js
Published 15 December 2016 · tagged with Node.js

好的好的。可以在 DevTools 中对 Node.js 进行调试。

### 028 V8 release v5.6
Published 02 December 2016 · tagged with release

是个大版本更新。Ignition/TurboFan的两阶段架构开始启用，原有的Crankshaft在后续的版本中被移除了。
内存的性能改进还是围绕着 Orinoco GC 的改进进行。这部分更小众，暂时没有关注。
速度优化覆盖了一系列原先加入的ES6特性（估计是跟各个浏览器厂商在PK的结果）。

相关阅读：
https://benediktmeurer.de/2016/11/25/v8-behind-the-scenes-november-edition/


### 027 WebAssembly browser preview
Published 31 October 2016 · tagged with WebAssembly

联合几个浏览器大厂宣布了 WebAssembly。
由于目前我们还没有关注到 WebAssembly，暂时没有评论。
时至今日wasm还是作为一个输入进入 turbofan 的。所以在 turbofan 的知识是共用的。

### 026 V8 release v5.5
Published 24 October 2016 · tagged with release

语言特性介绍了 async functions，继续改进了内存优化。

> The V8 inspector was migrated from Chromium to V8. The inspector code now fully resides in the V8 repository.

### 025 Optimizing V8 memory consumption
Published 07 October 2016 · tagged with memory benchmarks

介绍了Chrome/V8模拟在野评测的评测的方法。

提供了新的 V8 heap visualizer，同时介绍了内存优化的几个技术概述。
如果是做浏览器或者后续的嵌入式的环境的话，或许需要看一看。

有关 Tracing 的内容可以进一步从
https://www.chromium.org/developers/how-tos/trace-event-profiling-tool
获得。

### 024 V8 release v5.4
Published 09 September 2016 · tagged with release

本次发布没有说ES6特性，主要是性能和内存改进的说明。

### 023 Firing up the Ignition interpreter 23 August 2016 internals

技术细节可以参考
BlinkOn 6 Day 1 Talk 2- Ignition - an interpreter for V8
https://www.bilibili.com/video/BV15J411J7Gf/

以及V8的文档中的ignition部分。

### 022 V8 at the BlinkOn 6 conference
Published 21 July 2016 · tagged with presentations

会议内容有价值，值得观看。
油管内容已经搬运到B站：

Real-world JavaScript performance
https://www.bilibili.com/video/BV1e54y1d7HX/

BlinkOn 6 Day 1 Talk 2- Ignition - an interpreter for V8
https://www.bilibili.com/video/BV15J411J7Gf/

How we measure and optimize for RAIL in V8’s GC #


ECMAScript 2015 and beyond

Tracing wrappers from V8 to Blink (lightning talk)


### 021 V8 release v5.3
Published 18 July 2016 · tagged with release

启用了 Ignition 解释器。


### 020 V8 release v5.2
Published 04 June 2016 · tagged with release

其中提到的油管视频，我搬运到了B站，可以直接看：
[BV1WK411L7zS](https://www.bilibili.com/video/BV1WK411L7zS/)

### 019 ES2015, ES2016, and beyond
Published 29 April 2016 · tagged with ECMAScript

对ES6标准不熟悉的可以看看。不涉及V8细节。

### 018 V8 release v5.1
Published 23 April 2016 · tagged with release

新增JS特性我已经看不懂了。

v5.1 版本开始有初步的wasm支持；继续改进了 orinoco。

### 017 Jank Busters Part Two: Orinoco
Published 12 April 2016 · tagged with internals memory

有关V8的GC的，是必须要看的内容。

对照 [Orinoco: The new V8 Garbage Collector Peter Marshall](https://www.bilibili.com/video/BV1TJ411n7pi)
一起看。

### 016 V8 release v5.0
Published 15 March 2016 · tagged with release

不熟悉ES6的同学可以按照 🏷️release 标签一步一步学习下。不至于一次知识点太多噎住了。

### 015 Experimental support for WebAssembly in V8
Published 15 March 2016 · tagged with WebAssembly

等做到 WASM 的时候、并且要写PPT的时候需要回来考古下。

代码方面不用看了，可以以代码为准。

### 014 RegExp lookbehind assertions 26 February 2016 ECMAScript RegExp

JS的正则表达式的一个功能点介绍。默认可以不看。

### 013 V8 extras 04 February 2016 internals

TODO 确认是否还存在。

用更容易的方式从JS构建V8的 custom snapshot。

> V8 extras provide a new and lightweight way for embedders to implement features.

ref: https://v8.dev/blog/custom-startup-snapshots

### 012 V8 release v4.9 26 January 2016 release

JS的新技能。熟悉JS就不用看。

（btw，对于我是有帮助的，原来JS又添加了这么多的 feature …… Proxy & Reflect）

### 011 There’s Math.random(), and then there’s Math.random()

17 December 2015 🏷️ECMAScript 🏷️internals

安全问题相关。默认不用看。

### 010 V8 release v4.8

25 November 2015 🏷️release

ES6的两个特性的实现。

### 009 Jank Busters Part One

30 October 2015 🏷️memory

原理和开发人员的关注点（需求来源）可以看下。改进的目标讲解的比较清楚。技术细节没有讲。

### 008 V8 release v4.7

14 October 2015 🏷️release

不熟悉JS的可以看看，熟悉的可以跳过。

### 007 Custom startup snapshots

25 September 2015 🏷️internals

TODO 确认下这里的 snapshot 跟目前V8代码中的 mksnapshot 等概念是否是一致的。

概念上类似于将代码内容确定的 builtin 编译成 so 库直接加载。

另一个概念是JS是有宿主环境这个概念的，不同的宿主环境给出来的可用的函数不一样，例如nodejs和浏览器。

### 006 V8 release v4.6

28 August 2015 🏷️release

1. 介绍了几个ES6的特性。对JS熟悉的可以跳过，不熟悉的建议看看，多学习点。
2. 提到了四个避免 jank 的优化。目前建议是不用看了。可能已经过时。

### 005 Getting garbage collection for free

07 August 2015 🏷️internals 🏷️memory

如果是没有接触过GC的概念的话，这篇需要看下。目前的GC已经有了一些改进，参考
[Orinoco: The new V8 Garbage Collector Peter Marshall](https://www.bilibili.com/video/BV1TJ411n7pi)
同时，增量GGC的基本思路目前是没变的。

TODO 提到的Chromium的 task scheduler 不确定现在是否淘汰了。以及 vsync 的概念是否还有。

### 004 Code caching

27 July 2015 🏷️internals

TODO 确认，不确定是否目前还是同样的实现。

这里的 Code Caching 是类似将JS源代码解析到 BaseCompiler 编译之后的结果，
优化的假设是一个脚本文件可以被多次使用，那么可以节约AST解析和输出的时间。
现在这个想法可能逐步发展成了 WebAssembly？

### 003 V8 release v4.5

17 July 2015 🏷️release

版本发布类的并不需要仔细看。主要都是 feature 的内容。本次添加了一些ES2015的语言特性。

### 002 Digging into the TurboFan JIT

13 July 2015 🏷️internals

开始针对某些特定的JS代码启用 turbofan。提到了特性：SoN，多层次翻译和优化。
明确的区分了JS语言、VM层和特定架构后端。这个目前也还是的。
给了一个 SoN IR 的例子。具体的IR细节内容可以看V8文档中的 IR 介绍。

### 001 Hello, World!

https://v8.dev/blog/hello-world

从 chromium blog 中剥离出来的第一篇。没技术内容。

## Chromium Blog

这里收录了 Chromium Blog 中标记了 v8 tag 以及我们觉得跟理解V8代码相关的内容。

### Better code optimization decisions for V8
Tuesday, May 1, 2012

https://blog.chromium.org/2012/05/better-code-optimization-decisions-for.html

PR成分多一些，介绍的是 Chrome 20 相对于 Chrome 19 的提升。

### V8 Benchmark Suite extended with physics simulation
Thursday, March 15, 2012

https://blog.chromium.org/2012/03/v8-benchmark-suite-extended-with.html

内容关系不大，可以不看。

### A game changer for interactive performance.
Monday, November 21, 2011

https://blog.chromium.org/2011/11/game-changer-for-interactive.html

GC的内容，本篇是PR，没有技术细节。而后续可以参考另一个演讲视频：

[Orinoco: The new V8 Garbage Collector Peter Marshall](https://www.bilibili.com/video/BV1TJ411n7pi)

### Updating JavaScript Benchmarks for Modern Browsers

Wednesday, May 4, 2011

https://blog.chromium.org/2011/05/updating-javascript-benchmarks-for.html

内容相关，有效。信息量不大，知道 Kraken、SunSpider 和 Octane 是 JS 测试集就行。

### A New Crankshaft for V8
Tuesday, December 7, 2010

https://blog.chromium.org/2010/12/new-crankshaft-for-v8.html

Crankshaft 在 V8 7.x 之后就没有了。

## V8 开发人员或其他同行的博客内容

## 国内同行写的中文分析内容

欢迎国内的伙伴提交PR将自己的文章加入进来，一起积累❤️
