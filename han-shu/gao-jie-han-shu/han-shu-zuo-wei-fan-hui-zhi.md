# 函数作为返回值

在JavaScript中，函数可以作为返回值。这意味着你可以在一个函数中定义另一个函数，并将其作为返回值返回给调用者。

下面是一个示例，展示了如何在一个函数中定义并返回另一个函数：

```javascript
function createMultiplier(multiplier) {
  return function (number) {
    return number * multiplier;
  };
}

const double = createMultiplier(2);
console.log(double(5)); // 输出：10

const triple = createMultiplier(3);
console.log(triple(5)); // 输出：15
```

在上面的例子中，`createMultiplier()`函数接受一个参数`multiplier`，并返回一个匿名函数。返回的函数接受一个参数`number`，并返回`number * multiplier`的结果。

通过调用`createMultiplier()`函数并传入不同的参数，我们可以创建不同的函数。在示例中，我们分别创建了`double`和`triple`两个函数，它们分别将输入的数字乘以2和3。

当我们调用`double(5)`时，返回的匿名函数会将5乘以2，得到结果10。同样，调用`triple(5)`时，返回的匿名函数会将5乘以3，得到结果15。

这种将函数作为返回值的技术在JavaScript中被广泛应用，可以用于创建闭包、实现函数柯里化等高级编程技巧。
