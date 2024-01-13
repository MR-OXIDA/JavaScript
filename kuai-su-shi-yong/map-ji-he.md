# Map集合

Map是JavaScript中的一种集合类型，它允许你存储键值对，并且可以使用任意类型的值作为键或值。Map的特点包括：

* 键值对的存储顺序与插入顺序一致。
* 键可以是任意类型的值，包括对象和函数。
* 可以通过键快速查找对应的值。
* 可以动态添加、删除和修改键值对。

下面是Map的基本操作示例：

```javascript
// 创建一个空的Map
const map = new Map();

// 添加键值对
map.set('key1', 'value1');
map.set('key2', 'value2');

// 获取值
console.log(map.get('key1')); // 输出: value1

// 检查键是否存在
console.log(map.has('key2')); // 输出: true

// 删除键值对
map.delete('key1');

// 获取Map的大小
console.log(map.size); // 输出: 1

// 清空Map
map.clear();
```

除了基本操作，Map还提供了一些其他的方法，如`keys()`、`values()`和`entries()`，可以用于遍历Map中的键、值或键值对。

```javascript
const map = new Map();
map.set('key1', 'value1');
map.set('key2', 'value2');

// 遍历键
for (let key of map.keys()) {
  console.log(key);
}

// 遍历值
for (let value of map.values()) {
  console.log(value);
}

// 遍历键值对
for (let entry of map.entries()) {
  console.log(entry[0] + ': ' + entry[1]);
}
```

Map是一种非常有用的数据结构，特别适用于需要存储和查找键值对的情况。它提供了灵活性和高效性，可以满足各种需求。
