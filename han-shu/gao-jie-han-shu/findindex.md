# findIndex

`findIndex()`方法是JavaScript中数组的一个原生方法，用于查找数组中满足指定条件的第一个元素的索引，并返回该索引。如果没有找到符合条件的元素，则返回-1。

以下是`findIndex()`方法的基本语法：

```javascript
array.findIndex(callback[, thisArg])
```

参数说明：

* `callback`：用于测试每个元素的函数。函数接收三个参数：`element`（当前元素）、`index`（当前索引）、`array`（调用`findIndex()`方法的数组）。
* `thisArg`（可选）：执行回调函数时使用的this值。

`findIndex()`方法会从数组的第一个元素开始遍历，直到找到一个满足条件的元素，然后返回该元素的索引。如果没有找到符合条件的元素，则返回-1。

以下是一个示例，演示如何使用`findIndex()`方法：

```javascript
const fruits = ['apple', 'banana', 'orange', 'mango'];

const index = fruits.findIndex(fruit => fruit === 'orange');
console.log(index); // 输出：2
```

在上面的示例中，我们有一个水果数组`fruits`，我们使用`findIndex()`方法查找元素值为'orange'的索引。由于'orange'位于数组的第三个位置（索引为2），所以`findIndex()`方法返回2。
