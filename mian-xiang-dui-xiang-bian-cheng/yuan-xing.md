# 原型

在 JavaScript 中，每个对象都有一个原型（prototype）。原型是一个对象，它包含共享的属性和方法，可以被其他对象继承和共享。当我们访问一个对象的属性或方法时，如果该对象本身没有这个属性或方法，JavaScript 就会去它的原型链上查找。

原型链是一系列对象的链接，每个对象都有一个指向它的原型的引用。当我们访问一个对象的属性时，JavaScript 会先在对象本身查找，如果找不到，就会沿着原型链向上查找，直到找到该属性或到达原型链的末尾（通常是 Object.prototype）。

在 JavaScript 中，原型是通过构造函数来创建的。每个函数都有一个 `prototype` 属性，它指向一个对象，这个对象就是该函数的原型。当我们使用 `new` 关键字创建一个对象时，这个对象的原型会被设置为构造函数的 `prototype` 属性。

下面是一个使用原型的简单示例：

```javascript
// 定义一个构造函数
function Person(name, age) {
  this.name = name;
  this.age = age;
}

// 在构造函数的原型上定义方法
Person.prototype.sayHello = function() {
  console.log("Hello, my name is " + this.name);
};

// 创建一个对象
const person1 = new Person("John", 30);

// 调用对象的方法
person1.sayHello();  // 输出: Hello, my name is John
```

在上面的示例中，我们定义了一个 `Person` 构造函数，并在其原型上定义了一个 `sayHello` 方法。当我们使用 `new Person()` 创建一个对象时，这个对象会继承 `Person` 构造函数的原型，从而可以访问到 `sayHello` 方法。

原型的使用可以帮助我们实现对象的继承和共享属性和方法。通过在原型上定义方法，我们可以让所有通过同一个构造函数创建的对象共享这些方法，从而节省内存空间。
