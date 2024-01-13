# 嵌入到HTML

JavaScript可以通过嵌入到HTML文档中来实现与网页的交互和动态效果。在HTML文件中，可以使用`<script>`标签来引入JavaScript代码。

有几种方式可以将JavaScript代码嵌入到HTML中：

1. 内联方式：可以直接在HTML标签中使用`<script>`标签来嵌入JavaScript代码。例如：

```html
<script>
  // JavaScript代码
</script>
```

在`<script>`标签中，可以编写任意的JavaScript代码，包括变量定义、函数声明、事件处理等。

2. 外部文件方式：可以将JavaScript代码保存到一个独立的.js文件中，然后使用`<script>`标签的`src`属性来引入外部文件。例如：

```html
<script src="script.js"></script>
```

在上面的例子中，`script.js`是存储JavaScript代码的文件名。浏览器会自动下载并执行该文件中的代码。

无论是内联方式还是外部文件方式，JavaScript代码都可以访问和修改HTML文档中的元素，以实现动态交互效果。例如，可以通过JavaScript来修改元素的样式、内容、属性，或者响应用户的事件（如点击、鼠标移动等）。

需要注意的是，一般情况下，将`<script>`标签放在HTML文件的`<head>`或`<body>`标签内都是可以的。但为了提高页面加载性能，推荐将JavaScript代码放在`<body>`标签的底部，这样可以确保在JavaScript代码执行之前，页面的其他内容已经加载完成。
