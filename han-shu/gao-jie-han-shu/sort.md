# sort

`sort()`方法是JavaScript中数组的一个原生方法，用于对数组元素进行排序。它会直接修改原数组，而不会创建一个新的排序后的数组。

以下是`sort()`方法的基本语法：

```javascript
array.sort(compareFunction)
```

参数说明：

* `compareFunction`（可选）：用于指定排序的顺序。它是一个比较函数，可以自定义排序规则。如果不提供该参数，则默认按照Unicode编码进行排序。

下面是一个示例，演示如何使用`sort()`方法对一个数组进行排序：

```javascript
var numbers = [3, 1, 4, 2, 5];

// 升序排序
numbers.sort(function(a, b) {
  return a - b;
});

console.log(numbers); // 输出 [1, 2, 3, 4, 5]
```

在上面的示例中，我们通过传递一个比较函数给`sort()`方法来实现升序排序。比较函数接受两个参数`a`和`b`，并返回一个负数、零或正数，表示`a`应该在`b`之前、与`b`相等、或在`b`之后。通过返回`a - b`，我们实现了升序排序。如果要进行降序排序，可以返回`b - a`。
