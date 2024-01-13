# map/reduce

### **map方法**

`map()`方法是 JavaScript 数组对象的一个内置方法，用于对数组中的每个元素执行指定的操作，并返回一个新的数组，新数组的元素是原始数组经过操作后的结果。

`map()`方法接受一个回调函数作为参数，该回调函数会被依次应用于数组中的每个元素。回调函数接受三个参数：当前元素的值、当前元素的索引和原始数组本身。回调函数可以返回一个新的值，该值将成为新数组中对应位置的元素。

下面是一个使用`map()`方法的示例：

```javascript
var numbers = [1, 2, 3, 4, 5];

var doubledNumbers = numbers.map(function(number) {
  return number * 2;
});

console.log(doubledNumbers); // 输出 [2, 4, 6, 8, 10]
```

在这个示例中，`map()`方法将数组`numbers`中的每个元素都乘以2，并返回一个新的数组`doubledNumbers`。

你还可以使用箭头函数来简化代码：

```javascript
var numbers = [1, 2, 3, 4, 5];

var doubledNumbers = numbers.map(number => number * 2);

console.log(doubledNumbers); // 输出 [2, 4, 6, 8, 10]
```

`map()`方法是一个非常有用的数组方法，可以方便地对数组中的元素进行转换和处理。

### reduce()方法

`reduce()`方法是一个用于数组操作的高阶函数，它在每个元素上应用一个函数，以将数组减少为单个值。这个方法在函数式编程中非常有用，可以用于求和、计算平均值、查找最大/最小值等。

`reduce()`方法接受两个参数：一个回调函数和一个可选的初始值。回调函数接受四个参数：累加器（accumulator）、当前值（current value）、当前索引（current index）和原始数组（source array）。回调函数返回的值将成为下一次调用回调函数时的累加器的值。

下面是一个使用`reduce()`方法计算数组元素之和的示例：

```javascript
const numbers = [1, 2, 3, 4, 5];

const sum = numbers.reduce((accumulator, currentValue) => {
  return accumulator + currentValue;
}, 0);

console.log(sum); // 输出 15
```

在上面的示例中，初始值为0，回调函数将累加器和当前值相加，并返回结果。`reduce()`方法会遍历数组中的每个元素，并将结果累加到累加器中。

请注意，`reduce()`方法是数组的原型方法，因此可以直接在数组上调用。
