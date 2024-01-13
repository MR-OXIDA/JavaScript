# JavaScript的对象

在JavaScript中，对象是一种复合数据类型，用于存储多个键值对（属性和值）的集合。对象可以用来表示现实世界中的实体，如人、车、商品等，或者用来表示更抽象的概念，如配置项、用户信息等。

对象的创建有多种方式，其中最常见的是使用对象字面量表示法（{}）或使用new关键字和Object构造函数。例如：

```javascript
// 使用对象字面量表示法创建对象
const person = {
  name: 'John',
  age: 30,
  gender: 'male'
};

// 使用new关键字和Object构造函数创建对象
const car = new Object();
car.brand = 'Toyota';
car.model = 'Camry';
car.year = 2021;
```

对象的属性可以通过点号（.）或方括号（\[]）来访问。例如：

```javascript
console.log(person.name); // 输出：John
console.log(car['brand']); // 输出：Toyota
```

对象的属性可以是任意的JavaScript值，包括字符串、数字、布尔值、函数、数组、甚至其他对象。例如：

```javascript
const product = {
  name: 'iPhone',
  price: 999.99,
  isAvailable: true,
  getDescription: function() {
    return `The ${this.name} is available for ${this.price} dollars.`;
  },
  features: ['5G support', 'Face ID', 'Dual camera']
};

console.log(product.getDescription()); // 输出：The iPhone is available for 999.99 dollars.
console.log(product.features[0]); // 输出：5G support
```

对象还可以通过赋值来修改或添加属性。例如：

```javascript
person.age = 35; // 修改属性值
person.job = 'Engineer'; // 添加新属性

console.log(person.age); // 输出：35
console.log(person.job); // 输出：Engineer
```

需要注意的是，JavaScript中的对象是引用类型，这意味着多个变量可以引用同一个对象。修改一个变量所引用的对象会影响到其他引用该对象的变量。例如：

```javascript
const obj1 = { name: 'Alice' };
const obj2 = obj1;

obj2.name = 'Bob';

console.log(obj1.name); // 输出：Bob
```

这是因为obj1和obj2引用了同一个对象，所以对其中一个对象的修改会影响到另一个对象。

对象也可以作为参数传递给函数，或作为函数的返回值。这使得对象在JavaScript中被广泛用于数据的组织和传递。

这只是JavaScript对象的基础知识，对象还有很多高级特性和用法，如原型继承、对象方法、对象解构等。
