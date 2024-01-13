# 构造函数

JavaScript 中的构造函数是用于创建对象的特殊函数。构造函数可以用来定义对象的属性和方法，并且可以通过 `new` 关键字来实例化对象。

下面是一个简单的构造函数的示例：

```javascript
function Person(name, age) {
  this.name = name;
  this.age = age;
}

// 使用构造函数创建对象实例
var person1 = new Person("John", 25);
var person2 = new Person("Jane", 30);

console.log(person1.name); // 输出 "John"
console.log(person2.age); // 输出 30
```

在上面的示例中，`Person` 是一个构造函数，它接受两个参数 `name` 和 `age`。在构造函数内部，我们使用 `this` 关键字来引用新创建的对象，然后给对象赋予属性。

通过使用 `new` 关键字，我们可以实例化 `Person` 构造函数，并创建两个不同的对象 `person1` 和 `person2`。每个对象都有自己的属性值。

构造函数还可以定义对象的方法。例如，我们可以将一个方法添加到 `Person` 构造函数中：

```javascript
function Person(name, age) {
  this.name = name;
  this.age = age;

  this.sayHello = function() {
    console.log("Hello, my name is " + this.name);
  };
}

var person = new Person("John", 25);
person.sayHello(); // 输出 "Hello, my name is John"
```

在上面的示例中，我们在构造函数中定义了一个名为 `sayHello` 的方法。通过 `new` 关键字创建的对象实例可以调用这个方法。

构造函数还可以使用原型链来共享方法。这样可以节省内存，因为每个对象实例都不需要保存方法的副本。这是 JavaScript 中的常见做法。
