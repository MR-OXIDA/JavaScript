# 数组

JavaScript数组是一种用于存储和操作多个值的数据结构。它可以包含任意类型的值，包括数字、字符串、布尔值、对象和其他数组。以下是一些关于JavaScript数组的重要信息：

1.  创建数组： 可以使用数组字面量（`[]`）或`Array`构造函数来创建数组。例如：

    ```javascript
    let myArray = []; // 空数组
    let myArray = [1, 2, 3]; // 包含三个数字的数组
    let myArray = new Array(); // 空数组
    let myArray = new Array(1, 2, 3); // 包含三个数字的数组
    ```
2.  访问和修改数组元素： 数组的元素可以通过索引来访问和修改。索引从0开始，表示数组中的位置。例如：

    ```javascript
    let myArray = [1, 2, 3];
    console.log(myArray[0]); // 输出 1
    myArray[1] = 5; // 修改第二个元素为 5
    ```
3.  数组长度： 可以使用`length`属性获取数组的长度（即元素的个数）。例如：

    ```javascript
    let myArray = [1, 2, 3];
    console.log(myArray.length); // 输出 3
    ```
4.  数组方法： JavaScript提供了许多用于操作数组的内置方法，例如`push()`、`pop()`、`shift()`、`unshift()`、`slice()`、`splice()`等。这些方法可以用于添加、删除、替换和提取数组元素。例如：

    ```javascript
    let myArray = [1, 2, 3];
    myArray.push(4); // 在数组末尾添加元素
    myArray.pop(); // 删除数组末尾的元素
    myArray.splice(1, 1); // 删除索引为1的元素
    ```
5.  迭代数组： 可以使用循环语句（如`for`循环、`forEach`方法）来迭代数组中的元素。例如：

    ```javascript
    let myArray = [1, 2, 3];
    for (let i = 0; i < myArray.length; i++) {
      console.log(myArray[i]);
    }
    myArray.forEach(function(element) {
      console.log(element);
    });
    ```
6.  多维数组： JavaScript数组还支持多维数组，即数组的元素也可以是数组。这样可以创建二维、三维甚至更高维度的数组。例如：

    ```javascript
    let myArray = [[1, 2], [3, 4]];
    console.log(myArray[0][1]); // 输出 2
    ```

这些只是JavaScript数组的基本概念和用法，还有很多其他操作和方法可以用于处理数组。
