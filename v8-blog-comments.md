# V8 Blog 的内容同步阅读

Google V8 团队的技术博客（Blog）是理解V8架构和实现细节、后续研发进展的重要的来源。
另一方面，V8的技术实现一直在快速变化，博客内容从2015到2020时间跨度很大，
是否与代码一致，需要读者自己去对比才行。
我们在《深入V8引擎》的repo中记录自己阅读V8博客中的笔记和评论，方便后续我们新加入V8项目的同事理解。

目前的技术评论的时间节点是2020年第二季度。

## V8 Blog


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
