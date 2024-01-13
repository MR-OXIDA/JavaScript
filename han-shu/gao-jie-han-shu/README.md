# 高阶函数

高阶函数（Higher-Order Functions）是指能够接受函数作为参数，并/或者返回一个函数的函数。在JavaScript中，函数被视为一等公民，因此可以像其他值一样被传递和返回。

高阶函数可以提供一种抽象的方式来处理和操作函数，使代码更灵活、可复用和可组合。它们可以用于实现许多常见的编程模式，如函数式编程、回调函数、事件处理等。

下面是一些常见的高阶函数示例：

1. 函数作为参数：

```javascript
function applyOperation(x, y, operation) {
  return operation(x, y);
}

function add(x, y) {
  return x + y;
}

function subtract(x, y) {
  return x - y;
}

console.log(applyOperation(5, 3, add)); // 输出: 8
console.log(applyOperation(5, 3, subtract)); // 输出: 2
```

在上面的示例中，`applyOperation`是一个高阶函数，它接受两个数字和一个操作函数作为参数，并将操作函数应用于这两个数字。

2. 函数作为返回值：

```javascript
function multiplyBy(factor) {
  return function (number) {
    return number * factor;
  };
}

const multiplyBy2 = multiplyBy(2);
console.log(multiplyBy2(4)); // 输出: 8
```

在上面的示例中，`multiplyBy`是一个高阶函数，它返回一个新的函数，该函数将传入的数字乘以指定的因子。

高阶函数的应用非常广泛，它们可以用于函数组合、柯里化、延迟执行等场景。通过使用高阶函数，我们可以将代码变得更加模块化、可读性更强，并且能够更好地利用JavaScript中函数的特性。
