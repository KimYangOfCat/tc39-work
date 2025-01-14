---
title: "如何阅读一份提案草案？"
date: 2021-05-22
tags: [ECMA]
categories: [🌏 翻译校对]
---

每个处于第二阶段或更高阶段的提案都有一个规范文本草案，存储在 `https://tc39.es/proposal-<name>`。这些草案都是供实现该功能时所参考的权威定义；README 或 Issue 中的内容或讨论可能会引用这份草案作为背景<!-- more -->。

提案规范文本的表达可能会与[当前规范的草案](https://tc39.es/ecma262)有所不同，也可能会对某些其他提案有所添加。当添加一个全新的章节时，它不会突出显示，但是当修改现有章节时，它们会以绿色突出显示，强调是插入的内容，而红色的标识则表示删除。

规范文本旨在被抽象地解释（译者注：即，只对实现的运行效果有所要求，而在如何实现上没有规定）。只有*“可观察到的语义”*，即执行 JavaScript 代码时的行为表现，才需要与规范匹配。具体实现可以使用他们想要的任何策略，包括使用能达到相同结果的不同算法。

想要查看更多有关如何阅读一份规范文本的详细信息？请参考 Timothy Gu 的[如何阅读 ECMAScript 规范](https://timothygu.me/es-howto/) 一文和 ECMAScript 规范一文中的[标志性公约](https://tc39.es/ecma262/#sec-notational-conventions)章节部分内容。


> * 原文地址：[Reading a proposal draft](https://github.com/tc39/how-we-work/blob/master/how-to-read.md)
> * 原文作者：[Ecma TC39](https://github.com/tc39/how-we-work)
> * 译文出自：[掘金翻译计划](https://github.com/xitu/gold-miner)
> * 本文永久链接：[https://github.com/xitu/gold-miner/blob/master/article/ECMA-TC39/Reading-a-proposal-draft.md](https://github.com/xitu/gold-miner/blob/master/article/ECMA-TC39/Reading-a-proposal-draft.md)
> * 译者：[霜羽 Hoarfroster](https://github.com/PassionPenguin)
> * 校对者：[Kim Yang](https://github.com/KimYangOfCat)