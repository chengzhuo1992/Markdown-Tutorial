Markdown指南

[TOC]

## 前言

这份指南是基于GitHub Flavored Markdown的，使用方法与显示效果，与其他编辑器上的差异甚微。

## 块元素（Block Elements)

### 段落和换行符

段落，通常指的是一行或者多行连续的文本。

默认情况下，段落之间是以多个空行进行分隔的。我们只需要按下`回车键` 就可以完成段落分隔。

![para02](/imgs/para02.png)

<center>这是段落分隔</center>

有些编辑器中，会忽略掉换行。进行换行操作的时候，可以使用`Shift` + `回车`。

![para01](/imgs/para01.png)

<center>这是换行</center>

也许有的编辑器不支持，你可以尝试在文字后面输入`两个空格` 

![lb01](/imgs/lb01.png)

或者输入`<br/>`

![lb02](/imgs/lb02.png)

## 标题

创建标题，可以在文本行的开头输入1-6个井号，`#`。不同个数的`#`，代表着标题的等级。就像在Word中，一个井号，`#`，代表着一级标题。两个井号，`##`，代表着二级标题。

**注意，`#`后面，要空一格再输入标题**

标题的显示效果以及**无空格的错误示范**：

![tit01](/imgs/tit01.png)

所以大家记得要加空格

## 引用

引用，近些年在文章中使用的越来越多了。下面的显示效果，你一定不陌生。

> 这是一段引用文字。

你只需要在文字前面输入`>`就可以（最后在`>`后加空格，虽然有些编辑器会帮你补全这个空格）

``` markdown
> 这是一段引用文字。
```

**注意，如果回车后不想继续使用这个符号所代表的功能，再一次按下回车，如下**

> 第一段引用
>
> （回车后会这样，但是不想引用了，可以继续按下回车，这一行文字的引用就会消失）

## 列表

列表的话，分为有序列表，和无序列表。

**你可以使用`*`或者`+`,`-`来创建无序列表。**

```markdown
* 这是无序列表1
+ 这是无序列表2
```

显示效果：

* 这是无序列表1

+ 这是无序列表2

**可以使用`1.`来创建有序列表，注意别少了那一点**

```markdown
1. 这是有序列表1
2. 这是有序列表2
```

显示效果：

1. 这是有序列表1
2. 这是有序列表2

## 任务列表

任务列表就是在列表前面加一个符号，来表示列表事件是否完成。一般可以用来记录待办事项。

- [ ] 待办事项
- [x] 已办事项

你可以使用`- [ ]`和`- [x]`来表示待办事项和已办事项。

一般情况下，任务列表钱的方框是可以交互的，你可以鼠标点击。

代码如下：

``` markdown
- [ ] 待办事项
- [x] 已办事项
```

## 代码块

Github显示代码块的符号与原始Markdown的有所不同。

**但Github的这种方式在很多编辑器中都使用，因为相对原来的表示方式，这种表示方式比较简单**

在Github中，你只需要输入\`\`\` ，**然后**按下 `回车`。除此之外，我们可以在```后面加上代码使用的语言，就会有代码高亮。

```python
def highlight():
    print('Ok, give you the highlighting')
```

这一段代码可以这样写：

```markdown
​```python
def highlight():
    print('Ok, give you the highlighting')
​```
```

`这个符号，在键盘的这个位置：

![code](/imgs/code.png)

在英文状态下，输入即可。

在原始的Markdown中，使用`<pre><code>`和`</code></pre>`来表示代码块。在绝大多数的编辑器中都是支持的，但是使用过程相对比较麻烦。

```markdown
<pre><code>
This is a code block.
</code></pre>
```

## 表格

使用表格的方法，相对有点复杂。不过也是有迹可循的。

表格一般由标题和内容组成。下图中，红色部分就是标题，蓝色部分就是内容。Markdown语言，有点仿照表格的样子。

![table](/imgs/table.png)

表格是由横线和竖线组成的。横线和竖线，在键盘的这些位置：

![table2](/imgs/table2.png)

同时，表格也是由行和列组成，**我们可以用换行来表示行，那么用什么来表示列呢？**

在表格中，是用竖线来表示列的。

现在，我们可以使用换行来表示行，竖线表示列，那么如何区分标题和内容呢？

Markdown是使用横线来区分标题和内容的。

所以，在Markdown中绘制表格，可以这样写：

```Markdown
| title 1| title 2|
|---------|---|
|content1| content2|
| content3 |content4|
```

显示效果是这样的：

| title 1  | title 2  |
| -------- | -------- |
| content1 | content2 |
| content3 | content4 |

**你会发现：我写的绘制表格的源码，并不美观。横线的多少，竖线后要不要空格，这些都随意。你看，它不是照样显示嘛**

但，我们平时使用表格的时候，貌似都需要居中。

```markdown
| title 1| title 2|
|:-:|---:|
|content1| content2|
| content3 |content4|
```

使用冒号来进行左对齐，居中和右对齐。左对齐的话，将冒号放在横线的左边，居中的话，将冒号放在横线的两端，右对齐的话，将冒号放在横线的右端。

显示效果如下：

| title 1  |  title 2 |
| :------: | -------: |
| content1 | content2 |
| content3 | content4 |

## 脚注

脚注的表示，我们可以这样记忆：

我们平时表示平方的时候，可以这样表示，2^2，2的平方。平方的显示效果，是不是和脚注很像。

所以脚注的表示方式，是这样的

```markdown
我就是脚注[^脚注]
```

显示效果：

我就是脚注[^脚注]

我们还可以给脚注加下附加信息。

```markdown
我就是脚注[^脚注]
[^脚注]:我就是长这样的
```

显示效果：

我就是脚注[^脚注]

[^脚注]:我就是长这样的

## 水平线（分割线）

在知乎的回答中，经常会有分割线的出现（像这样）：

---

创建分割线，只需要输入`---`或者`***`，然后按下`回车`就行了
