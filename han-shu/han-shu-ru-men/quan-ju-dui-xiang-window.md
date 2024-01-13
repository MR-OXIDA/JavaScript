# 全局对象window

全局对象 `window` 是在浏览器环境中使用 JavaScript 时的顶层对象。它代表了浏览器窗口或标签页，并提供了许多与浏览器交互的方法和属性。

在浏览器中，全局对象 `window` 包含了全局作用域中定义的所有变量和函数。这意味着如果你在全局作用域中声明一个变量或函数，它们会成为 `window` 对象的属性和方法。

例如，如果你在全局作用域中声明了一个变量 `x`，你可以通过 `window.x` 来访问它。同样，如果你在全局作用域中定义了一个函数 `foo`，你可以通过 `window.foo()` 来调用它。

除了用户定义的变量和函数，`window` 对象还包含了许多内置的属性和方法，用于与浏览器进行交互。例如，`window.alert()` 可以显示一个警告框，`window.location` 可以获取当前页面的 URL，`window.document` 可以访问 DOM（文档对象模型）。

需要注意的是，`window` 对象只在浏览器环境中存在，如果你在其他 JavaScript 执行环境（如 Node.js）中运行代码，是没有 `window` 对象的。

下面是一些示例代码，展示了如何使用 `window` 对象：

```javascript
// 全局作用域中声明变量和函数
var x = 10;

function foo() {
  console.log('Hello, world!');
}

// 访问全局变量和调用函数
console.log(window.x); // 输出 10
window.foo(); // 输出 "Hello, world!"

// 使用内置的 window 对象属性和方法
window.alert('This is an alert!');
console.log(window.location.href);
console.log(window.document.title);
```
