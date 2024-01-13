# generator生成器

生成器（Generators）是 JavaScript 中的一种特殊函数，它可以在函数执行过程中暂停和恢复。与普通函数不同，生成器可以生成一个迭代器（Iterator），用于逐步产生值的序列。

生成器函数使用 `function*` 关键字定义，并使用 `yield` 关键字在函数体内部暂停执行并返回一个值。每次调用生成器函数时，都会返回一个迭代器对象，可以使用这个迭代器对象的 `next()` 方法来获取生成器函数中 `yield` 关键字返回的值。

下面是一个简单的生成器函数的示例：

```javascript
function* numberGenerator() {
  yield 1;
  yield 2;
  yield 3;
}

const generator = numberGenerator();

console.log(generator.next()); // { value: 1, done: false }
console.log(generator.next()); // { value: 2, done: false }
console.log(generator.next()); // { value: 3, done: false }
console.log(generator.next()); // { value: undefined, done: true }
```

在上面的示例中，`numberGenerator` 是一个生成器函数，它会生成一个包含数字 1、2 和 3 的序列。我们通过调用 `numberGenerator()` 获取一个迭代器对象，并使用 `next()` 方法逐步获取生成器函数中 `yield` 返回的值。每次调用 `next()` 方法时，生成器函数会从上次暂停的地方继续执行，直到遇到下一个 `yield` 关键字或函数结束。

生成器函数的一个重要特性是可以使用 `yield*` 关键字委托给另一个生成器函数或可迭代对象。这样可以方便地组合多个生成器函数。

生成器函数在处理大量数据、异步编程、惰性计算等方面非常有用，它们提供了一种更简洁、更灵活的方式来处理序列数据的生成和处理。
