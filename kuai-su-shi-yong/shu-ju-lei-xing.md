# 数据类型

JavaScript中有多种数据类型，包括基本数据类型和引用数据类型。

1. 基本数据类型（Primitive Data Types）:
   * 字符串（String）：表示文本数据，用引号（单引号或双引号）括起来，例如："Hello World"。
   * 数字（Number）：表示数值数据，包括整数和浮点数，例如：10、3.14。
   * 布尔值（Boolean）：表示逻辑值，只有两个取值：true（真）和false（假）。
   * undefined：表示未定义的值，当变量声明但未赋值时，默认为undefined。
   * null：表示空值，表示变量的值为空。
   * Symbol：表示唯一的标识符，用于创建对象的属性名。
2. 引用数据类型（Reference Data Types）:
   * 对象（Object）：表示复杂的数据结构，可以包含多个属性和方法。例如：{ name: "John", age: 25 }。
   * 数组（Array）：表示有序的数据集合，可以包含多个值。例如：\[1, 2, 3, 4]。
   * 函数（Function）：表示可执行的代码块，可以被调用和重复使用。

JavaScript是一种动态类型的语言，变量的数据类型可以根据赋值的值自动推断，也可以在运行时动态改变变量的数据类型。

例如：

```javascript
var name = "John"; // 字符串类型
var age = 25; // 数字类型
var isStudent = true; // 布尔类型

var person = { name: "John", age: 25 }; // 对象类型

var numbers = [1, 2, 3, 4]; // 数组类型

function sayHello() {
  console.log("Hello!");
} // 函数类型
```

这些数据类型在JavaScript中具有不同的特性和用途，了解它们对于编写有效的JavaScript代码非常重要。

### BigInt

BigInt是JavaScript中的一种数据类型，用于表示任意精度的整数。它可以用来表示非常大或非常小的整数，超出了常规的Number类型的表示范围。

在JavaScript中，可以使用BigInt函数来创建一个BigInt值。例如：

```javascript
const bigNum = BigInt(123456789012345678901234567890);
console.log(bigNum); // 输出：123456789012345678901234567890n
```

BigInt值以后缀`n`结尾，以表示它是一个BigInt类型。

与常规的Number类型不同，BigInt类型可以进行任意精度的整数运算，而不会丢失精度。例如：

```javascript
const num1 = BigInt(123456789012345678901234567890);
const num2 = BigInt(987654321098765432109876543210);
const sum = num1 + num2;
console.log(sum); // 输出：1111111110111111111011111111100n
```

需要注意的是，BigInt类型不能与常规的Number类型进行混合运算，需要使用BigInt函数将常规的整数转换为BigInt类型。例如：

```javascript
const num1 = BigInt(1234567890);
const num2 = 9876543210n; // 直接使用n后缀创建BigInt值
const sum = num1 + num2;
console.log(sum); // 输出：11111111100n
```

另外，BigInt类型也支持常见的数学运算符（如加法、减法、乘法、除法和求余等）和比较运算符（如等于、大于、小于等）。

请注意，BigInt类型在旧版本的浏览器中可能不被支持，因此在使用之前，请确保你的浏览器支持BigInt类型或使用最新的浏览器版本。
