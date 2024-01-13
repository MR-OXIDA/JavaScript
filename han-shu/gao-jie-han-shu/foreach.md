# forEach

JavaScript中的forEach()方法是用于数组的迭代方法。它接受一个回调函数作为参数，并对数组中的每个元素执行该回调函数。

forEach()方法的语法如下：

```javascript
array.forEach(callback(currentValue, index, array), thisArg)
```

参数说明：

* callback：必需，表示要对数组中的每个元素执行的回调函数。该回调函数可以接受三个参数：
  * currentValue：当前正在处理的元素。
  * index：当前元素在数组中的索引。
  * array：正在被遍历的数组。
* thisArg（可选）：表示在执行回调函数时使用的this值。

forEach()方法会按照数组的顺序依次遍历数组中的每个元素，并对每个元素执行回调函数。它不会返回新的数组，而是直接修改原始数组。

下面是一个示例，展示了如何使用forEach()方法遍历数组并打印每个元素：

```javascript
const array = [1, 2, 3, 4, 5];

array.forEach((element, index) => {
  console.log(`Element at index ${index}: ${element}`);
});
```

输出结果为：

```
Element at index 0: 1
Element at index 1: 2
Element at index 2: 3
Element at index 3: 4
Element at index 4: 5
```

请注意，forEach()方法无法在遍历过程中使用break或return语句来提前退出循环。如果需要在遍历过程中提前退出循环，可以考虑使用其他方法，例如for循环或some()方法。
