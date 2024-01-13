# 解构赋值

解构赋值是一种在 JavaScript 中从数组或对象中提取值并赋给变量的语法。它可以让你更方便地访问和使用复杂的数据结构。

解构赋值的语法有两种形式：数组解构和对象解构。

1.  数组解构：

    ```javascript
    const array = [1, 2, 3];
    const [a, b, c] = array;
    console.log(a); // 输出 1
    console.log(b); // 输出 2
    console.log(c); // 输出 3
    ```

    在上面的例子中，我们通过解构赋值将数组 `array` 中的值分别赋给了变量 `a`、`b` 和 `c`。
2.  对象解构：

    ```javascript
    const obj = { x: 1, y: 2 };
    const { x, y } = obj;
    console.log(x); // 输出 1
    console.log(y); // 输出 2
    ```

    在上面的例子中，我们通过解构赋值将对象 `obj` 中的属性值分别赋给了变量 `x` 和 `y`。

解构赋值还支持默认值和嵌套结构的情况：

```javascript
const array = [1, 2];
const [a, b, c = 3] = array;
console.log(a); // 输出 1
console.log(b); // 输出 2
console.log(c); // 输出 3

const obj = { x: 1, y: { z: 2 } };
const { x, y: { z } } = obj;
console.log(x); // 输出 1
console.log(z); // 输出 2
```

解构赋值在处理函数参数、处理返回值等场景中非常有用，可以简化代码并提高可读性。
