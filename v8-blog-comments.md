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
### 050
### 049
### 048
### 047
### 046
### 045
### 044
### 043
### 042
### 041
### 040
### 039
### 038
### 037
### 036
### 035
### 034
### 033
### 032
### 031
### 030
### 029
### 028
### 027
### 026
### 025
### 024
### 023
### 022
### 021
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
