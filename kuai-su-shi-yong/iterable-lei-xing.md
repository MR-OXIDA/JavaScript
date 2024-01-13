# iterable类型

iterable类型是指可以迭代的对象，它们可以使用循环来访问其元素。在JavaScript中，许多内置的数据结构和对象都是可迭代的，例如数组、字符串、Set集合和Map集合。

可迭代对象具有一个名为Symbol.iterator的特殊方法，该方法返回一个迭代器对象。迭代器对象用于按顺序访问可迭代对象的每个元素。

迭代器对象有一个next()方法，该方法返回一个包含两个属性的对象：value和done。value表示当前迭代的元素值，done表示迭代是否结束。当done为true时，表示迭代已经完成。

可以使用for...of循环或者使用迭代器的next()方法来遍历可迭代对象的元素。例如，可以使用for...of循环遍历一个数组的元素，或者使用迭代器的next()方法逐个获取Set集合或Map集合的元素。

下面是一个示例，展示了如何使用for...of循环遍历数组的元素：

```javascript
const arr = [1, 2, 3, 4, 5];

for (const element of arr) {
  console.log(element);
}
```

输出结果为：

```
1
2
3
4
5
```
