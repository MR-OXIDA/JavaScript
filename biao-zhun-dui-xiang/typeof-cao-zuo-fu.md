# typeof操作符

`typeof` 是一个 JavaScript 操作符，用于确定给定值的数据类型。它返回一个表示数据类型的字符串。

下面是一些常见的 `typeof` 操作符的使用示例：

```javascript
console.log(typeof 42); // "number"
console.log(typeof "Hello"); // "string"
console.log(typeof true); // "boolean"
console.log(typeof undefined); // "undefined"
console.log(typeof null); // "object" （这是一个历史遗留问题，实际上 null 是一个原始值）
console.log(typeof [1, 2, 3]); // "object"
console.log(typeof { name: "John", age: 30 }); // "object"
console.log(typeof function() {}); // "function"
```

需要注意的是，`typeof` 操作符对于大多数数据类型都能返回正确的结果，但对于一些特殊情况可能会有一些限制。例如，`typeof null` 返回的是 "object"，这是 JavaScript 的历史遗留问题。

此外，`typeof` 对于函数返回的是 "function"，这是因为在 JavaScript 中，函数也是对象的一种特殊类型。

在使用 `typeof` 进行类型检查时，需要注意它的局限性，并且在特定情况下可能需要使用其他方法来进行更准确的类型判断。
