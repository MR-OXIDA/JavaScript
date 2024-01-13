# class继承

在 JavaScript 中，你可以使用 `class` 关键字来实现类和继承的机制。类提供了一种更简洁、更易于理解和组织代码的方式来创建对象，并且可以通过继承来共享属性和方法。

让我们来看一个示例：

```javascript
class Animal {
  constructor(name) {
    this.name = name;
  }

  speak() {
    console.log(this.name + " makes a sound");
  }
}

class Dog extends Animal {
  constructor(name, breed) {
    super(name);
    this.breed = breed;
  }

  speak() {
    console.log(this.name + " barks");
  }
}

const dog = new Dog("Buddy", "Golden Retriever");
dog.speak(); // 输出: Buddy barks
```

在上面的例子中，我们定义了一个 `Animal` 类和一个 `Dog` 类。`Dog` 类继承自 `Animal` 类，通过使用 `extends` 关键字来指定继承关系。

`Animal` 类有一个构造函数 `constructor` 和一个 `speak` 方法。`Dog` 类也有一个构造函数 `constructor` 和一个 `speak` 方法。在 `Dog` 类的构造函数中，我们使用 `super` 关键字来调用父类 `Animal` 的构造函数，并传递相应的参数。

通过继承，`Dog` 类获得了 `Animal` 类的属性和方法，并且可以在子类中进行扩展或重写。在上面的例子中，`Dog` 类重写了 `speak` 方法，使得狗的叫声与动物的叫声不同。

通过使用类和继承，我们可以更好地组织和管理对象的属性和方法，并实现代码的复用和扩展。
