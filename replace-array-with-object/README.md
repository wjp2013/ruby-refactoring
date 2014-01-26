# Replace Array with Object 以对象取代数组

你有一个数组，其中的元素各自代表不同的东西。

以对象替换数组，对于数组中的每个元素，以一个字段来表示。


## 好处

数组时一种常见的用以组织数据的结构。不过，它们应该只用于“以某种顺序容纳一组相似对象”。

有时候你会发现，一个数组容纳了多种不同对象，这会给用户带来麻烦，因为他们很难记住像“数组的第一个元素是人名”这样的约定。

对象就不同了，你可以运用字段名和函数名来传达这样的信息，因此你无需死记它，也无需依赖注释。

而且如果使用对象，你还可以将信息封装起来。并使用 Move Method （搬移函数）为它加上相关行为。