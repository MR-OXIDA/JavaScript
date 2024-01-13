# throw语句

`throw` 语句是 JavaScript 中用于手动抛出（或引发）错误的机制。它允许你在代码中显式地创建并抛出一个错误对象，以便在程序执行过程中触发错误的处理逻辑。

`throw` 语句通常与 `try...catch` 语句一起使用，以便在 `try` 块中抛出错误，并在相应的 `catch` 块中捕获和处理该错误。

下面是 `throw` 语句的基本语法：

```javascript
throw expression;
```

在这里，`expression` 是一个可以求值为任意值的表达式，通常是一个错误对象。

下面是一个示例，演示了如何使用 `throw` 语句手动抛出一个错误：

```javascript
function divide(a, b) {
  if (b === 0) {
    throw new Error('除数不能为零');
  }
  return a / b;
}

try {
  console.log(divide(10, 0));
} catch (error) {
  console.log('捕获到错误：', error.message);
}
```

在上面的示例中，我们定义了一个 `divide` 函数，它接受两个参数 `a` 和 `b`，并尝试计算 `a` 除以 `b` 的结果。如果 `b` 的值为零，我们使用 `throw` 语句抛出一个自定义错误对象。然后，在 `try` 块中，我们调用 `divide` 函数并尝试计算结果。如果错误被抛出，控制流会立即跳转到相应的 `catch` 块，我们可以在其中捕获并处理错误。
