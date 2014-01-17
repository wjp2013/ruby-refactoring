# Form Template Method 塑造模板方法

常见的一种情况是：你有一些子类，其中相应的某些函数以相同的顺序执行大致相近的操作，但是各操作不完全相同。

这种情况下我们可以将执行的序列移至超类，并借助多态保证各子类中的操作仍得以保持差异性。

这样的函数被称为 Template Method（模板函数）

# 何时使用这种重构方法？

无论何时，只要你看见2个子类之中有类似的方法，就可以把它们提升到超类。

但是如果这些函数并不完全相同该这么办？仍有必要尽量避免重复，但又必须保持这些函数之间的实质差异。

# 好处

避免重复代码的一个强大工具