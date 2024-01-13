# 标签函数

标签函数（Tagged Template）是 JavaScript 中的一种特殊函数调用形式。它允许我们在模板字符串前面使用一个函数，这个函数被称为标签函数。标签函数可以对模板字符串进行处理，并返回一个新的字符串。

标签函数的语法如下：

```javascript
tag`template string`
```

在这个语法中，`tag` 是一个函数名，后面跟着一个模板字符串。当标签函数被调用时，它会将模板字符串的各个部分作为参数传递给函数。标签函数可以对这些参数进行处理，然后返回一个新的字符串。

下面是一个标签函数的示例：

```javascript
function highlight(strings, ...values) {
  let result = '';
  for (let i = 0; i < strings.length; i++) {
    result += strings[i];
    if (i < values.length) {
      result += `<span class="highlight">${values[i]}</span>`;
    }
  }
  return result;
}

const name = 'Alice';
const age = 25;
const message = highlight`Hello, my name is ${name} and I am ${age} years old.`;

console.log(message);
```

在这个示例中，`highlight` 是一个标签函数。它接收两个参数：`strings` 和 `values`。`strings` 是一个包含模板字符串中普通文本的数组，`values` 是一个包含模板字符串中表达式的数组。

标签函数 `highlight` 将模板字符串中的普通文本和表达式拼接在一起，并用 `<span class="highlight">` 标签将表达式部分进行了高亮处理。最后返回一个新的字符串。

在示例中，`message` 的值将会是 `Hello, my name is Alice and I am 25 years old.`，其中 `${name}` 和 `${age}` 被包裹在 `<span class="highlight">` 标签中。

标签函数在处理模板字符串时非常有用，可以用于实现自定义的字符串处理逻辑，比如国际化、安全过滤等。
