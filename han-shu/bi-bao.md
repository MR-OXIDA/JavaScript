# 闭包

JavaScript闭包是指函数能够访问并操作在其词法作用域之外定义的变量的能力。简单来说，闭包是由函数以及其周围的词法环境组成的组合体。

当一个函数内部定义了另一个函数，并且内部函数引用了外部函数的变量时，就创建了一个闭包。这意味着内部函数可以访问外部函数的变量，即使外部函数已经执行完毕。

闭包的一个常见应用是创建私有变量。通过使用闭包，我们可以在函数内部定义变量，并且这些变量对外部是不可见的。

下面是一个示例，演示了如何使用闭包创建一个计数器：

```javascript
function createCounter() {
  let count = 0;

  function increment() {
    count++;
    console.log(count);
  }

  return increment;
}

const counter = createCounter();
counter(); // 输出 1
counter(); // 输出 2
```

在这个示例中，`createCounter` 函数定义了一个内部变量 `count` 和一个内部函数 `increment`。`increment` 函数引用了外部函数的变量 `count`，并且每次调用 `increment` 函数时，`count` 的值会增加并输出。

通过调用 `createCounter` 函数，我们得到了一个闭包 `counter`。每次调用 `counter` 函数时，都会访问和修改闭包中的变量 `count`。

闭包在 JavaScript 中有许多其他的应用场景，比如实现模块化、封装私有数据等。但需要注意的是，过度使用闭包可能会导致内存泄漏，因为闭包会持有对外部变量的引用，使得这些变量无法被垃圾回收。因此，在使用闭包时要注意内存管理。
