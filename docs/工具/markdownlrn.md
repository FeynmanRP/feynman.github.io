> Started on 2021-08-21
> 
> First version on 2021-8-21
>
>Author :FeynmanRP

- [markdown语法](#markdown语法)
  - [Headers 标题](#headers-标题)
  - [Blockquotes 引用](#blockquotes-引用)
  - [Lists 列表](#lists-列表)
  - [Emphasis 加粗和斜体](#emphasis-加粗和斜体)
  - [Code 代码](#code-代码)
    - [Inline Code 行内代码](#inline-code-行内代码)
    - [Code Block 代码块](#code-block-代码块)
  - [Links 链接](#links-链接)
  - [Images 图片](#images-图片)
- [References](#references)

**说明**：作为一名合格的开发者，`markdown`文本编辑方法几乎是必备技能。本文主要介绍`markdown`所需的主要语法,介绍顺序以我认为常用频率自上向下进行说明。那就让我们先来认识一下什么是`markdown`吧

>Markdown是一种轻量级标记语言，创始人为约翰·格鲁伯。它允许人们使用易读易写的纯文本格式编写文档，然后转换成有效的XHTML（或者HTML）文档。由于Markdown的轻量化、易读易写特性，并且对于图片，图表、数学式都有支持，目前许多网站都广泛使用Markdown来撰写帮助文档或是用于论坛上发表消息。——[维基百科](https://zh.wikipedia.org/wiki/Markdown)

# markdown语法
## Headers 标题
**格式：**`1～6个#` **+** `标题名称`

**例子：**
```markdown
# 一级标题
## 二级标题
...
###### 六级标题
```

```
# 一级标题
## 二级标题
...
###### 六级标题
```

## Blockquotes 引用

**格式：**`>` + `引用内容`

**例子：**
```markdown
> We are trying to prove ourselves wrong as quickly as possible, because only in that way can we find progress.——Richard Philips Feynman
```
> We are trying to prove ourselves wrong as quickly as possible, because only in that way can we find progress.——Richard Philips Feynman

**补充：**
引用格式并一定局限于引用他人，比如我也用它写一些文章信息

## Lists 列表

**例子：**markdown
```
- item1
* item2
    - item3
1. item01
1. item02
    1.item03
    1.ttem04
- [x] This is a complete item
- [ ] This is a incomplete item
```
- item1
* item2
    - item3
1. item01
1. item02
    1.item03
    1.item04

- [x] This is a complete item
- [ ] This is a incomplete item

## Emphasis 加粗和斜体

**斜体格式：**

`*` `内容` `*` 或

`_` `内容` `_`

**粗体格式：**

`**` `内容` `**` 或

`__` `内容` `__`

**例子：**
```
_我是斜体_
**我是粗体**
_我是斜体_
__我是粗体__
混合使用：
*我是斜体里的 __粗体__*
```
_我是斜体_

**我是粗体**

_我是斜体_

__我是粗体__

混合使用：

*我是斜体里的 __粗体__*

## Code 代码
### Inline Code 行内代码
**格式：**
\` 内容\`

通常嵌入于句中

**例子：**
```
我正在学习`Python`,`C++`,`Jave`这三门语言
```
我正在学习`Python`,`C++`,`Jave`这三门语言

### Code Block 代码块
**格式：**

\```<代码语言>

代码

\```

**例子：**

\```python

print('Hello,world!')

print('You are so beautiful!')

\```


```python

print('Hello,world!')
print('You are so beautiful!')

```
**补充：**
在最开始三个反撇后可以加代码的语言名称或简写以在渲染时获得高亮支持。一般支持的代码高亮会有很多，比如：`shell`、`bash`、`c`、`cpp`、`java`、`objectivec`、`python`、`swift`等

## Links 链接
**格式：**

`[网站说明](网站地址)`

不需要说明的话，可以直接写链接在两侧加上<>

**例子：**

```markdown
[百度](httpswww.baidu.com)
<https://www.baidu.com>
```

[百度](https://baidu.com)

<https://www.baidu.com>

## Images 图片
**格式：**

`![图片说明](图片链接)`

**例子：**
```
![年轻时的费曼](https://avatars.githubusercontent.com/u/58167131?s=400&u=a67382dd2f3e90241cd5742ff9eb7a5c511a0dbe&v=4)
```


![年轻时的费曼](https://avatars.githubusercontent.com/u/58167131?s=400&u=a67382dd2f3e90241cd5742ff9eb7a5c511a0dbe&v=4)



# References
[面向开发的Markdown学习](https://thu-ios.github.io/tutorials/lecture/markdown.html)

[GitHub Guides | Mastering Markdown](https://guides.github.com/features/mastering-markdown/)