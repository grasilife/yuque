# 数学公式

可视化编辑器支持所见即所得的公式编辑。

# 快速入门

你可以在菜单的「实验室」中找到插入公式等入口。随后在公式编辑区域输入 LaTeX 语法即可实时预览。例如我在输入框输入下面代码：

```plain
\sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6}
```

即可以看到公式内容为：<div id="xzvazg" data-type="math" data-display="block" data-align="center" data-src="https://cdn.yuque.com/__latex/7871fbdd01f5f3d83f6f52968e565f35.svg" data-text="%5Csum_%7Bi%3D0%7D%5En%20i%5E2%20%3D%20%5Cfrac%7B(n%5E2%2Bn)(2n%2B1)%7D%7B6%7D" data-width="195" data-height="52"><img src="https://cdn.yuque.com/__latex/7871fbdd01f5f3d83f6f52968e565f35.svg" width="195"/></div>

# 布局和对齐方式

公式支持行内模式和块级模式。行内模式将会嵌入到文本中，被文本内容环绕；块级模式将会是独占一行，不会有文本环绕，会有留白。

只有在块级模式下才支持对齐方式，目前支持左对齐，居中对齐、右对齐三种方式。

# 更多支持

目前采用[ KaTex](https://khan.github.io/KaTeX/) 库生成 *LaTeX *数学公式，因此有一个门槛是你需要熟知一点 LaTeX 语法，你可以参考：

* [Latex 语法](http://meta.math.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference)
* [Katex 支持的 Latex 命令](https://github.com/Khan/KaTeX/wiki/Function-Support-in-KaTeX)

