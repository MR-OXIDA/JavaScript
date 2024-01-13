# 循环

在JavaScript中，循环用于重复执行一段代码，直到满足某个条件为止。JavaScript提供了几种类型的循环，包括for循环、while循环和do-while循环。

1. for循环： for循环是一种常用的循环结构，用于指定一个初始值、一个终止条件和一个递增或递减步长。它的语法如下：

```javascript
for (初始值; 终止条件; 步长) {
  // 循环体代码
}
```

例如，以下代码将打印出从1到5的数字：

```javascript
for (let i = 1; i <= 5; i++) {
  console.log(i);
}
```

2. while循环： while循环在每次迭代之前检查一个条件，如果条件为真，则执行循环体内的代码。它的语法如下：

```javascript
while (条件) {
  // 循环体代码
}
```

例如，以下代码将打印出从1到5的数字：

```javascript
let i = 1;
while (i <= 5) {
  console.log(i);
  i++;
}
```

3. do-while循环： do-while循环与while循环类似，但它会先执行一次循环体，然后再检查条件。如果条件为真，则继续执行循环。它的语法如下：

```javascript
do {
  // 循环体代码
} while (条件);
```

例如，以下代码将打印出从1到5的数字：

```javascript
let i = 1;
do {
  console.log(i);
  i++;
} while (i <= 5);
```

这些是JavaScript中常用的循环结构。你可以根据具体的需求选择合适的循环类型来实现重复执行的逻辑。

### 循环 for ...in

`for...in`循环是JavaScript中的一种循环类型，用于遍历对象的属性。它的语法如下：

```javascript
for (variable in object) {
  // 循环体
}
```

在每次循环中，`variable`会被赋值为对象的一个属性名，然后执行循环体。这个循环会遍历对象的可枚举属性，包括自身属性和继承属性。下面是一个示例：

```javascript
const obj = { a: 1, b: 2, c: 3 };

for (let key in obj) {
  console.log(key + ': ' + obj[key]);
}
```

输出结果为：

```
a: 1
b: 2
c: 3
```

需要注意的是，`for...in`循环并不保证遍历属性的顺序，因此在实际使用中应谨慎处理。此外，`for...in`循环也会遍历对象的原型链上的属性，如果不希望遍历继承属性，可以使用`hasOwnProperty`方法进行过滤。

```javascript
for (let key in obj) {
  if (obj.hasOwnProperty(key)) {
    console.log(key + ': ' + obj[key]);
  }
}
```

这样就只会输出对象自身的属性。
