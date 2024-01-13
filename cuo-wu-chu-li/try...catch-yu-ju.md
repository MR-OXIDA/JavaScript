# try...catch 语句

`try...catch` 语句是 JavaScript 中用于捕获和处理错误的语法结构。它允许您在代码块中包含可能引发错误的代码，并在错误发生时执行相应的错误处理逻辑。

`try...catch` 语句的基本语法如下：

```javascript
try {
  // 可能引发错误的代码
} catch (error) {
  // 处理错误的代码
}
```

在 `try` 块中，您可以放置可能会引发错误的代码。如果在 `try` 块中的代码引发了错误，JavaScript 引擎将立即跳转到 `catch` 块，并将错误对象作为参数传递给 `catch` 块中的变量（通常命名为 `error`）。

在 `catch` 块中，您可以编写处理错误的代码逻辑。您可以访问错误对象的属性，如 `name` 和 `message`，以获取关于错误的详细信息，并根据需要采取适当的措施。

以下是一个示例，演示了如何使用 `try...catch` 语句来处理可能引发错误的代码：

```javascript
try {
  const result = someFunction(); // 可能引发错误的函数调用
  console.log(result); // 如果没有错误发生，打印结果
} catch (error) {
  console.log('发生了错误：' + error.message); // 处理错误，打印错误消息
}
```

在上面的示例中，我们调用了一个名为 `someFunction` 的函数，它可能引发错误。如果没有错误发生，我们将打印结果。如果发生错误，我们将在控制台中打印错误消息。

您还可以使用多个 `catch` 块来处理不同类型的错误。例如：

```javascript
try {
  // 可能引发错误的代码
} catch (error1) {
  // 处理特定类型的错误
} catch (error2) {
  // 处理其他类型的错误
}
```

在这种情况下，第一个匹配到的 `catch` 块将处理错误。如果第一个 `catch` 块无法处理错误，将继续查找下一个匹配的 `catch` 块。

希望这可以帮助您理解 `try...catch` 语句的用法。
