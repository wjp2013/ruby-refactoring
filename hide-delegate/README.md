# Hide Delegate 隐藏委托关系

## 何时使用这种重构方法？

如果你看到用户向一个对象索求另一个对象 a，然后再向后者 a 索求另一个对象 b，然后再向 b 索求另一个对象 c 这就是 Message Chain。

## 可能带来的问题？

理论上你可以重构Message Chain上的任何一个对象，但这么做往往会把所有中介对象都变成Middle Man。

## 如何做？

1. 先观察 Message Chain 最终得到的对象是用来干什么的。
2. 看看能否以Extract Method把使用该对象的代码提炼到一个独立函数中。
3. 再运用 Move Method 把这个函数推入 Message Chain。
4. 如果这条链上的某个对象有多位客户打算航行此航线的剩余部分，就加一个函数来做这件事。

## 好处

* 可以减少耦合性
* 一旦对象间(Models)的关系发生任何变化，客户端(View, APIs)不用做出修改。