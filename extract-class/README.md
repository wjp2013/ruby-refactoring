# Extract Class 提炼类

*Extract Class* 是改善并发（concurrent）程序的一种常用技术，因为它使你可以提炼后的两个 classes 分别加锁（locks）。

如果某些数据和某些函数总是一起出现，如果某些数据经常同时变化甚至彼此依赖，这就表示你应该将它们分离出去。

某个class做了应该由两个class做的事。

## 何时会遇到这样的情况？

实际工作中，类会不断成长扩展。你会在这儿加入一些功能，在哪加入一些数据。给某个类添加一项新责任时，你会觉得不值得为这项责任分离出一个单独的类。于是，随着责任不断增加，这个类会变得过分复杂。很快，你的类就会变成一团乱麻。

## 这样的情况会有什么特征？

* 这样的类往往含有大量函数和数据。
* 这样的类往往太大而不易理解。
* 如果某些数据和某些函数总是一起出现，某些数据经常同时变化甚至彼此依赖。

## 好处

一个类应该是一个清楚地抽象，处理一些明确的责任。
