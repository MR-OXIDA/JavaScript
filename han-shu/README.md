# 函数

### 定义函数

在编程中，函数是一段可重复使用的代码块，用于执行特定的任务或计算。函数可以接受输入参数，执行一系列操作，并返回一个结果。

在JavaScript中，可以使用函数声明或函数表达式来定义函数。下面是两种定义函数的方式：

1. 函数声明：

```javascript
function functionName(parameter1, parameter2) {
  // 函数体，执行一系列操作
  // 可以使用参数进行计算
  // 可以使用 return 语句返回结果
  return result;
}
```

2. 函数表达式：

```javascript
const functionName = function(parameter1, parameter2) {
  // 函数体，执行一系列操作
  // 可以使用参数进行计算
  // 可以使用 return 语句返回结果
  return result;
};
```

在函数定义中，functionName是函数的名称，可以根据需要自行命名。parameter1和parameter2是函数的参数，用于接收传递给函数的值。函数体是一系列语句，用于执行特定的操作。可以使用参数进行计算，并使用return语句返回结果。

下面是一个简单的示例，展示了如何定义一个函数并使用它：

```javascript
function addNumbers(num1, num2) {
  const sum = num1 + num2;
  return sum;
}

const result = addNumbers(5, 10);
console.log(result); // 输出 15
```

在上面的示例中，我们定义了一个名为addNumbers的函数，它接受两个参数num1和num2，并返回它们的和。然后，我们调用这个函数，并将结果存储在result变量中，并将结果打印到控制台。

### 调用函数

在JavaScript中，调用函数的语法与其他编程语言类似。你可以通过函数名后面加上一对括号来调用函数，并在括号内传递参数（如果有的话）。

下面是一个简单的例子，展示了如何在JavaScript中调用函数：

```javascript
// 定义一个简单的函数
function sayHello() {
  console.log("Hello, World!");
}

// 调用函数
sayHello();
```

在这个例子中，我们定义了一个名为`sayHello`的函数，它会在控制台打印出"Hello, World!"。然后我们通过写下`sayHello()`来调用这个函数，这样函数就会执行，并且在控制台打印出"Hello, World!"。

如果函数需要参数，你可以在调用函数时传递这些参数。例如：

```javascript
// 定义一个带有参数的函数
function greet(name) {
  console.log("Hello, " + name + "!");
}

// 调用带有参数的函数
greet("Alice");
```

在这个例子中，我们定义了一个名为`greet`的函数，它接受一个参数`name`。当我们调用`greet("Alice")`时，函数会在控制台打印出"Hello, Alice!"。

### 关键字`arguments`

在 JavaScript 中，"arguments" 是一个特殊的对象，它包含了函数被调用时传递的所有参数。你可以使用它来获取传递给函数的参数列表，即使你没有在函数定义中显式地声明这些参数。下面是一个示例：

```javascript
function sum() {
  var total = 0;
  for (var i = 0; i < arguments.length; i++) {
    total += arguments[i];
  }
  return total;
}

console.log(sum(1, 2, 3)); // 输出 6
console.log(sum(4, 5, 6, 7)); // 输出 22
```

在这个例子中，函数 `sum` 没有定义任何参数，但是通过使用 `arguments` 对象，我们可以在函数内部访问传递给函数的参数。

### rest 参数

在 JavaScript 中，rest 参数是一种特殊的语法，用于表示函数可以接受可变数量的参数，并将这些参数封装为一个数组。它使用三个连续的点号（...）后跟一个参数名来表示。

下面是一个使用 rest 参数的示例：

```javascript
function sum(...numbers) {
  let total = 0;
  for (let i = 0; i < numbers.length; i++) {
    total += numbers[i];
  }
  return total;
}

console.log(sum(1, 2, 3)); // 输出 6
console.log(sum(4, 5, 6, 7)); // 输出 22
```

在这个例子中，函数 `sum` 使用了 rest 参数 `...numbers` 来接受可变数量的参数。传递给函数的参数会被封装为一个数组 `numbers`，然后我们可以在函数内部对它进行操作。

使用 rest 参数的好处是可以方便地处理不确定数量的参数，而不需要使用 `arguments` 对象或手动处理参数列表。你可以像操作普通数组一样在函数内部操作 rest 参数。

需要注意的是，rest 参数必须是函数的最后一个参数，因为它会收集所有剩余的参数。如果你在函数定义中同时使用了 rest 参数和其他参数，rest 参数必须放在最后。

总结一下，JavaScript 中的 rest 参数是一种用于表示函数可以接受可变数量参数的语法，它将这些参数封装为一个数组供函数内部使用。
