# 包装对象

JavaScript 中的包装对象是一种特殊的对象，它们可以将基本数据类型（如字符串、数字和布尔值）包装起来，使其具有对象的特性和功能。这样做的目的是为了方便在基本数据类型和对象之间进行转换。

在 JavaScript 中，有三种常见的包装对象：String、Number 和 Boolean。当我们对基本数据类型调用它们对应的方法时，JavaScript 会临时创建一个对应的包装对象，使我们能够访问这些方法。例如：

```javascript
var str = "Hello";
var strObj = new String(str);

console.log(typeof str);      // 输出 "string"
console.log(typeof strObj);   // 输出 "object"

console.log(str.length);      // 输出 5
console.log(strObj.length);   // 输出 5
```

在上面的示例中，我们首先创建了一个字符串 `str`，然后使用 `new String()` 创建了一个包装对象 `strObj`。尽管它们的值相同，但它们的类型不同。`typeof` 操作符返回 "string" 和 "object" 分别表示它们的类型。

由于包装对象是对象，我们可以使用点号运算符访问它们的属性和方法。例如，我们可以使用 `length` 属性获取字符串的长度。

需要注意的是，当我们对包装对象进行比较时，JavaScript 会进行自动拆包（即将包装对象转换为基本数据类型）。因此，以下比较表达式的结果将会是 `true`：

```javascript
var num = 42;
var numObj = new Number(num);

console.log(num == numObj);   // 输出 true
console.log(num === numObj);  // 输出 false
```

在上面的示例中，虽然 `num` 和 `numObj` 的值相同，但由于它们的类型不同，使用 `==` 进行比较时会自动拆包，返回 `true`。而使用 `===` 进行比较时，不会进行自动拆包，因此返回 `false`。

