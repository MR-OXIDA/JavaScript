# Error对象

`Error` 对象是 JavaScript 中用于表示错误的内置对象之一。它用于创建自定义错误，并提供有关错误的信息。

您可以使用 `new Error()` 语法创建一个新的 `Error` 对象。例如：

```javascript
const myError = new Error('这是一个自定义错误');
```

在上面的示例中，我们创建了一个名为 `myError` 的 `Error` 对象，并传递了一个错误消息作为参数。

`Error` 对象还具有一些常用的属性，例如 `name` 和 `message`。`name` 属性表示错误的名称，而 `message` 属性包含错误的描述信息。您可以通过访问这些属性来获取有关错误的详细信息。例如：

```javascript
console.log(myError.name); // 输出: "Error"
console.log(myError.message); // 输出: "这是一个自定义错误"
```

除了 `Error` 对象，JavaScript 还提供了其他一些内置错误对象，如 `SyntaxError`、`TypeError`、`ReferenceError` 等。这些错误对象具有特定的用途和属性，以便更好地表示不同类型的错误。

在实际的开发中，您可以使用 `try...catch` 语句来捕获和处理错误。`try` 块用于包含可能引发错误的代码，而 `catch` 块用于处理捕获到的错误。例如：

```javascript
try {
  // 可能引发错误的代码
  throw new Error('这是一个错误');
} catch (error) {
  // 处理错误
  console.log(error.name); // 输出: "Error"
  console.log(error.message); // 输出: "这是一个错误"
}
```

通过使用 `try...catch` 语句，您可以在发生错误时执行特定的错误处理逻辑，以避免程序崩溃或产生意外结果。
