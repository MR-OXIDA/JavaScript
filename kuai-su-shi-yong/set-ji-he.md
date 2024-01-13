# Set集合

Set是JavaScript中的一种集合类型，它允许你存储唯一的值，而且可以使用任意类型的值作为元素。Set的特点包括：

* 元素的存储顺序与插入顺序一致。
* 每个元素在Set中是唯一的，不会重复。
* 可以快速添加、删除和查询元素。

下面是Set的基本操作示例：

```javascript
// 创建一个空的Set
const set = new Set();

// 添加元素
set.add('value1');
set.add('value2');

// 检查元素是否存在
console.log(set.has('value2')); // 输出: true

// 删除元素
set.delete('value1');

// 获取Set的大小
console.log(set.size); // 输出: 1

// 清空Set
set.clear();
```

Set还提供了一些其他的方法，如`values()`和`entries()`，可以用于遍历Set中的值或值对。

```javascript
const set = new Set();
set.add('value1');
set.add('value2');

// 遍历值
for (let value of set.values()) {
  console.log(value);
}

// 遍历值和索引
for (let entry of set.entries()) {
  console.log(entry[0] + ': ' + entry[1]);
}
```

Set是一种非常有用的数据结构，特别适用于需要存储唯一值的情况。它提供了高效的元素查询和去重功能，可以简化代码并提高性能。
