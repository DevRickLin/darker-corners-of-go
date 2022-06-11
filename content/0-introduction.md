# Go 鲜为人知的角落｜第 0 章 介绍｜《Darker Corners of Go》独译（已授权）

> 当前译本仍不稳定，如翻译有问题请及时联系 jacob953@csu.edu.cn。

## 译者序

决定翻译《Darker Corners of Go》那日，与 Rytis 先生结束初步交流时，已经凌晨 5 点了，想来更多是一种冲动。自从开始学习 Go 以来，越来越感到 Go 语言核心理论的简单美。
在学习 Go 之初，我也硬着头皮去仔细阅读过《Effective Go》。但对于一个初学者来说，很难领会“圣经”中所表达的核心理念。

于是，我试着去阅读《Darker Corners of Go》，精确、易懂、简短，以类型的方式对陷阱进行分类。尽管它不是很典型的入门类型书籍，但它依然让我直观地感受到了 Go 语言的特性，还帮助我更快地锁定查阅的范围。
所以，我打算干脆将它用更加地道的方式翻译出来，直接分享给大家。一方面，可以锻炼自己的英文水平，面向更加开阔的技术世界；另一方面，可以对 Go 有更加深入的了解，还可以为 Go 的中文资源做贡献。

这篇文章的篇幅很短，所以翻译得比较轻松，以不至于萌生放弃的念头。翻译工作仍在继续，我会逐步发布新的章节，在此面向中文社区的 Gopher 征求意见，希望给读者带来更好的阅读体验。
这本书是根据《Darker Corners of Go》的电子版翻译过来的，与网上的电子版有一定的差异，有些内容是电子版没有的，或许后续会更新上去。

实际上，在多年前，Kyle Quest 发布过一篇 "50 Shades of Go: Traps, Gotchas, and Common Mistakes for New Golang Devs"，当然，这篇文章也有中文译本。
那篇文章以难度高低的方式对陷阱进行分类，而《Go 鲜为人知的角落》以类型的方式对陷阱进行分类。对于一个经验不足的 Gopher 来说，我认为后者或许更易被接受和学习。

由于本人也是 Gopher 新手，翻译过程中难免会有一些错误和问题，还希望各位高手批评指正。如果您觉得翻译或内容中有任何错误和问题，请您及时反馈给我，以便及时地进行修正：jacob953@csu.edu.cn

最后，我要感谢 Rytis Bieliunas 先生，是他给予了我极大的信任，让我以独译的角色翻译这本书，并时刻关注译本的进度，同时也要感段桂华女士，在翻译筹备过程中，是她在背后给予了我很多支持。

我希望本书能对那些想了解、学习和研究 Go 的人们有所帮助！

## 作者序

### 这是什么？

在我刚开始学习 Go 的时候，读过一些相关的介绍书籍和语言规范，并且在此之前，我已经熟悉过其他几种编程语言。
尽管如此，在学习了这些书籍之后，我认为我对 Go 的了解真的不够多，很难进行实际的工作。
我觉得我对 Go 的工作方式了解得还不够深入，可能需要掉进很多坑里，才能对使用 Go 有所把握。

**事实证明，我的判断是对的。**

虽然 `简单`、`诗意`、`简洁` 是 Go 语言的核心理论，但当你深入使用 Go 时，你会发现，它的许多创造性方法会使你掉进坑里。

目前为止，在使用 Go 制作应用程序的这几年时间中，我踩过数不胜数的坑，于是，我打算将这些经验总结到一起，为 Go 的新手们编写一份指南。

我的目标是将 Go 中的各种可能让新开发者意料之外的知识点都收集到一起，这也许还能对一些不寻常的功能有所启发。
希望这样可以为读者节省大量的查询和调试时间，并尽可能避免一些代价昂贵的漏洞。

在阅读这本书之前，我认为你应该至少已经知道 Go 的语法，才能确保这本书对你是有用的。如果你已经有一定 Go 的编程经验，或已经熟悉其他编程语言，并且希望学习 Go，那就最好不过了。

如果你发现书籍中有撰写错误的地方，或者我总结的例子中没有包括令你最意外的 Go 的用法，请联系我：rytbiel@gmail.com。

非常感谢 [Vytautas Shaltenis](https://rtfb.lt/) 和 [Jon Forrest](https://jlforrest.wordpress.com/) ，在他们的帮助下，这本书变得更加完整。

## 目录

（持续更新中）