# filter

`filter()`方法是一个用于数组操作的高阶函数，它根据指定的条件过滤数组中的元素，并返回一个新的数组，包含满足条件的元素。

`filter()`方法接受一个回调函数作为参数，该回调函数用于定义过滤条件。回调函数接受三个参数：当前值（current value）、当前索引（current index）和原始数组（source array）。回调函数应返回一个布尔值，表示当前元素是否满足条件。

下面是一个使用`filter()`方法筛选出偶数的示例：

```javascript
const numbers = [1, 2, 3, 4, 5];

const evenNumbers = numbers.filter((value) => {
  return value % 2 === 0;
});

console.log(evenNumbers); // 输出 [2, 4]
```

在上面的示例中，回调函数检查每个元素是否为偶数（通过对2取余判断）。满足条件的元素将被保留在新数组`evenNumbers`中。

请注意，`filter()`方法是数组的原型方法，因此可以直接在数组上调用。它返回一个新的数组，而不会修改原始数组。
