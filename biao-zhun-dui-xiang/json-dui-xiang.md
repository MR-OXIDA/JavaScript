# JSON对象

JSON（JavaScript Object Notation）是一种常用的数据交换格式，用于在不同的系统之间传递和存储数据。在 JavaScript 中，JSON 对象是一个全局对象，提供了用于解析和生成 JSON 数据的方法。

要解析 JSON 数据并将其转换为 JavaScript 对象，可以使用 `JSON.parse()` 方法。这个方法接受一个 JSON 字符串作为参数，并返回一个对应的 JavaScript 对象。例如：

```javascript
const jsonStr = '{"name": "John", "age": 30, "city": "New York"}';
const obj = JSON.parse(jsonStr);

console.log(obj.name);  // 输出: John
console.log(obj.age);   // 输出: 30
console.log(obj.city);  // 输出: New York
```

要将 JavaScript 对象转换为 JSON 字符串，可以使用 `JSON.stringify()` 方法。这个方法接受一个 JavaScript 对象作为参数，并返回对应的 JSON 字符串。例如：

```javascript
const obj = {name: "John", age: 30, city: "New York"};
const jsonStr = JSON.stringify(obj);

console.log(jsonStr);  // 输出: {"name":"John","age":30,"city":"New York"}
```

JSON 支持的数据类型包括字符串、数字、布尔值、对象、数组和 null。在 JavaScript 中，这些类型的值可以直接转换为 JSON 字符串，而且 JSON 字符串也可以转换为相应的 JavaScript 值。
