---
title: Markdown 教程
published: 2025-01-20
pinned: false
description: 一个简单的 Markdown 博客文章示例。
tags: [Markdown, 博客]
category: 示例
licenseName: "Unlicensed"
author: emn178
sourceLink: "https://github.com/emn178/markdown"
draft: false
---

# Markdown 教程

这个 Markdown 示例展示了如何编写 Markdown 文件。本文档集成了核心语法和扩展语法 (GFM)。

- [区块元素](#区块元素)
  - [段落和换行](#段落和换行)
  - [标题](#标题)
  - [区块引用](#区块引用)
  - [列表](#列表)
  - [代码块](#代码块)
  - [分隔线](#分隔线)
  - [表格](#表格)
- [行内元素](#行内元素)
  - [链接](#链接)
  - [强调](#强调)
  - [代码](#代码)
  - [图片](#图片)
  - [删除线](#删除线)
- [其他](#其他)
  - [自动链接](#自动链接)
  - [反斜杠转义](#反斜杠转义)
- [行内 HTML](#行内-html)

## 区块元素

### 段落和换行

#### 段落

HTML 标签：`<p>`

由一行或多行文本组成，前后要有空行。（只包含**空格**或**制表符**的行被视为空行。）

代码：

    这将是
    行内的。

    这是第二个段落。

预览：

---

这将是
行内的。

这是第二个段落。

---

#### 换行

HTML 标签：`<br />`

在一行的末尾输入**两个或多个空格**。

代码：

    这将不会是
    行内的。

预览：

---

这将不会是  
行内的。

---

### 标题

Markdown 支持两种样式的标题：Setext 和 atx。

#### Setext

HTML 标签：`<h1>`, `<h2>`

使用任意数量的**等号 (=)** 表示 `<h1>`，使用**连字符 (-)** 表示 `<h2>`。

代码：

    这是 H1
    =============
    这是 H2
    -------------

预览：

---

# 这是 H1

## 这是 H2

---

#### atx

HTML 标签：`<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>`

在行首使用 1-6 个**井号 (#)**，对应 `<h1>` - `<h6>`。

代码：

    # 这是 H1
    ## 这是 H2
    ###### 这是 H6

预览：

---

# 这是 H1

## 这是 H2

###### 这是 H6

---

（可选）你可以“闭合” atx 样式的标题。闭合的井号**不需要**与开头的井号数量一致。

代码：

    # 这是 H1 #
    ## 这是 H2 ##
    ### 这是 H3 ######

预览：

---

# 这是 H1

## 这是 H2

### 这是 H3

---

### 区块引用

HTML 标签：`<blockquote>`

Markdown 使用电子邮件样式的 **>** 字符进行区块引用。最好在每一行前面都加上 >。

代码：

    > 这是一个包含两个段落的区块引用。Lorem ipsum dolor sit amet,
    > consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    > Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
    >
    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    > id sem consectetuer libero luctus adipiscing.

预览：

---

> 这是一个包含两个段落的区块引用。Lorem ipsum dolor sit amet,
> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
> Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
>
> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
> id sem consectetuer libero luctus adipiscing.

---

Markdown 也允许你偷懒，只在段落的第一行前面加上 >。

代码：

    > 这是一个包含两个段落的区块引用。Lorem ipsum dolor sit amet,
    consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    id sem consectetuer libero luctus adipiscing.

预览：

---

> 这是一个包含两个段落的区块引用。Lorem ipsum dolor sit amet,
> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
> Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
> id sem consectetuer libero luctus adipiscing.

---

区块引用可以嵌套（即引用中包含引用），只需添加额外的 > 级数。

代码：

    > 这是第一层引用。
    >
    > > 这是嵌套的区块引用。
    >
    > 回到第一层。

预览：

---

> 这是第一层引用。
>
> > 这是嵌套的区块引用。
>
> 回到第一层。

---

区块引用可以包含其他 Markdown 元素，包括标题、列表和代码块。

代码：

    > ## 这是一个标题。
    >
    > 1.   这是第一个列表项。
    > 2.   这是第二个列表项。
    >
    > 这里有一个示例代码：
    >
    >     return shell_exec("echo $input | $markdown_script");

预览：

---

> ## 这是一个标题。
>
> 1.  这是第一个列表项。
> 2.  这是第二个列表项。
>
> 这里有一个示例代码：
>
>     return shell_exec("echo $input | $markdown_script");

---

### 列表

Markdown 支持有序（编号）和无序（项目符号）列表。

#### 无序列表

HTML 标签：`<ul>`

无序列表使用**星号 (\*)**、**加号 (+)** 和**连字符 (-)**。

代码：

    *   红色
    *   绿色
    *   蓝色

预览：

---

- 红色
- 绿色
- 蓝色

---

等同于：

代码：

    +   红色
    +   绿色
    +   蓝色

以及：

代码：

    -   红色
    -   绿色
    -   蓝色

#### 有序列表

HTML 标签：`<ol>`

有序列表使用数字后跟英文句点：

代码：

    1.  Bird
    2.  McHale
    3.  Parish

预览：

---

1.  Bird
2.  McHale
3.  Parish

---

有时可能会无意中触发有序列表，例如这样写：

代码：

    1986. What a great season.

预览：

---

1986. What a great season.

---

你可以使用**反斜杠 (\\)** 转义句点：

代码：

    1986\. What a great season.

预览：

---

1986\. What a great season.

---

#### 缩进元素

##### 列表中的区块引用

要在列表项中放入区块引用，引用的 > 分隔符需要缩进：

代码：

    *   带区块引用的列表项：

        > 这是列表项内部的
        > 一个区块引用。

预览：

---

- 带区块引用的列表项：

  > 这是列表项内部的
  > 一个区块引用。

---

##### 列表中的代码块

要在列表项中放入代码块，代码块需要缩进两次 —— **8 个空格**或**两个制表符**：

代码：

    *   带代码块的列表项：

            <这里是代码>

预览：

---

- 带代码块的列表项：

      <这里是代码>

---

##### 嵌套列表

代码：

    * A
      * A1
      * A2
    * B
    * C

预览：

---

- A
  - A1
  - A2
- B
- C

---

### 代码块

HTML 标签：`<pre>`

将块的每一行缩进至少 **4 个空格**或 **1 个制表符**。

代码：

    这是一个普通段落：

        这是一个代码块。

预览：

---

这是一个普通段落：

    这是一个代码块。

---

代码块会一直持续，直到遇到没有缩进的行（或文章结束）。

在代码块中，**_& 符号 (&)_** 和**尖括号 (< 和 >)** 会自动转换为 HTML 实体。

代码：

        <div class="footer">
            &copy; 2004 Foo Corporation
        </div>

预览：

---

    <div class="footer">
        &copy; 2004 Foo Corporation
    </div>

---

以下围栏代码块和语法高亮部分是扩展语法，你可以使用另一种方式编写代码块。

#### 围栏代码块 (Fenced Code Blocks)

只需将代码包裹在 ` ``` ` 中（如下所示），就不需要缩进四个空格。

代码：

    这是一个示例：

    ```
    function test() {
      console.log("看到这个函数前的空行了吗？");
    }
    ```

预览：

---

这是一个示例：

```
function test() {
  console.log("看到这个函数前的空行了吗？");
}
```

---

#### 语法高亮

在围栏代码块中，添加可选的语言标识符，我们将通过语法高亮显示它 ([支持的语言](https://github.com/github/linguist/blob/master/lib/linguist/languages.yml))。

代码：

    ```ruby
    require 'redcarpet'
    markdown = Redcarpet.new("Hello World!")
    puts markdown.to_html
    ```

预览：

---

```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```

---

### 分隔线

HTML 标签：`<hr />`
在一行中放置**三个或更多的连字符 (-)、星号 (*) 或下划线 (_)**。你可以在这些字符之间使用空格。

代码：

    * * *
    ***
    *****
    - - -
    ---------------------------------------
    ___

预览：

---

---

---

---

---

---

---

---

### 表格

HTML 标签：`<table>`

这是一个扩展语法。

使用**竖线 (|)** 分隔列，使用**连字符 (-)** 分隔表头，并使用**冒号 (:)** 进行对齐。

外侧的**竖线 (|)** 和对齐方式是可选的。每个单元格至少需要 **3 个分隔符**来分隔表头。

代码：

```
| 左对齐 | 居中对齐 | 右对齐 |
|:-------|:--------:|-------:|
|aaa     |bbb       |ccc     |
|ddd     |eee       |fff     |

 A | B
---|---
123|456


A |B
--|--
12|45
```

预览：

---

| 左对齐 | 居中对齐 | 右对齐 |
| :----- | :------: | -----: |
| aaa    |   bbb    |    ccc |
| ddd    |   eee    |    fff |

| A   | B   |
| --- | --- |
| 123 | 456 |

| A   | B   |
| --- | --- |
| 12  | 45  |

---

## 行内元素

### 链接

HTML 标签：`<a>`

Markdown 支持两种样式的链接：行内式和引用式。

#### 行内式

行内链接格式如下：`[链接文本](URL "标题")`

标题是可选的。

代码：

    这是一个 [示例](http://example.com/ "标题") 行内链接。

    [这个链接](http://example.net/) 没有标题属性。

预览：

---

这是一个 [示例](http://example.com/ "标题") 行内链接。

[这个链接](http://example.net/) 没有标题属性。

---

如果你引用的是同一服务器上的本地资源，可以使用相对路径：

代码：

    详情请参阅我的 [关于](/about/) 页面。

预览：

---

详情请参阅我的 [关于](/about/) 页面。

---

#### 引用式

你可以预先定义链接引用。格式如下：`[id]: URL "标题"`

标题也是可选的。然后你引用该链接，格式如下：`[链接文本][id]`

代码：

    [id]: http://example.com/  "这里是可选标题"
    这是一个 [示例][id] 引用式链接。

预览：

---

[id]: http://example.com/ "这里是可选标题"

这是一个 [示例][id] 引用式链接。

---

即：

- 方括号包含链接标识符（**不区分大小写**，可选地从左边距缩进最多三个空格）；
- 紧跟一个冒号；
- 紧跟一个或多个空格（或制表符）；
- 紧跟链接的 URL；
- 链接 URL 可选地被尖括号包裹；
- 可选地紧跟链接的标题属性，包裹在双引号、单引号或括号中。

以下三个链接定义是等效的：

代码：

    [foo]: http://example.com/  "这里是可选标题"
    [foo]: http://example.com/  '这里是可选标题'
    [foo]: http://example.com/  (这里是可选标题)
    [foo]: <http://example.com/>  "这里是可选标题"

使用一组空的方括号，链接文本本身将被用作名称。

代码：

    [Google]: http://google.com/
    [Google][]

预览：

---

[Google]: http://google.com/

[Google][]

---

### 强调

HTML 标签：`<em>`, `<strong>`

Markdown 将**星号 (\*)** 和**下划线 (\_)** 视为强调指标。**单个分隔符**将是 `<em>`；**双分隔符**将是 `<strong>`。

代码：

    *单个星号*

    _单个下划线_

    **双星号**

    __双下划线__

预览：

---

_单个星号_

_单个下划线_

**双星号**

**双下划线**

---

但如果你在 \* 或 \_ 两侧加空格，它将被视为字面意义上的星号或下划线。

你可以使用反斜杠转义它：

代码：

    \*这段文字被字面意义上的星号包裹\*

预览：

---

\*这段文字被字面意义上的星号包裹\*

---

### 代码

HTML 标签：`<code>`

使用**反引号 (`)** 包裹。

代码：

    使用 `printf()` 函数。

预览：

---

使用 `printf()` 函数。

---

要在代码段中包含字面意义的反引号，可以使用**多个反引号**作为开启和关闭分隔符：

代码：

    ``这里有一个字面意义的反引号 (`)。``

预览：

---

``这里有一个字面意义的反引号 (`)。``

---

包裹代码段的反引号分隔符可以包含空格 —— 开启后一个，关闭前一个。这允许你在代码段的开头或结尾放置字面意义的反引号：

代码：

    代码段中的单个反引号：`` ` ``

    代码段中的反引号包裹字符串：`` `foo` ``

预览：

---

代码段中的单个反引号：`` ` ``

代码段中的反引号包裹字符串：`` `foo` ``

---

### 图片

HTML 标签：`<img />`

Markdown 使用的图片语法旨在模拟链接语法，允许两种样式：行内式和引用式。

#### 行内式

行内图片语法如下：`![替代文本](URL "标题")`

标题是可选的。

代码：

    ![替代文本](/path/to/img.jpg)

    ![替代文本](/path/to/img.jpg "可选标题")

预览：

---

![替代文本](https://s2.loli.net/2024/08/20/5fszgXeOxmL3Wdv.webp)

![替代文本](https://s2.loli.net/2024/08/20/5fszgXeOxmL3Wdv.webp "可选标题")

---

即：

- 一个感叹号：!；
- 紧跟一组方括号，包含图片的 alt 属性文本；
- 紧跟一组括号，包含图片的 URL 或路径，以及包裹在双引号或单引号中的可选标题属性。

#### 引用式

引用式图片语法如下：`![替代文本][id]`

代码：

    [img id]: https://s2.loli.net/2024/08/20/5fszgXeOxmL3Wdv.webp  "可选标题属性"
    ![替代文本][img id]

预览：

---

[img id]: https://s2.loli.net/2024/08/20/5fszgXeOxmL3Wdv.webp "可选标题属性"

![替代文本][img id]

---

### 删除线

HTML 标签：`<del>`

这是一个扩展语法。

GFM 添加了删除文本的语法。

代码：

```
~~错误的文本。~~
```

预览：

---

~~错误的文本。~~

---

## 其他

### 自动链接

Markdown 支持一种快捷样式，用于为 URL 和电子邮件地址创建“自动”链接：只需用尖括号包裹 URL 或电子邮件地址即可。

代码：

    <http://example.com/>

    <address@example.com>

预览：

---

<http://example.com/>

<address@example.com>

---

GFM 会自动链接标准 URL。

代码：

```
https://github.com/emn178/markdown
```

预览：

---

https://github.com/emn178/markdown

---

### 反斜杠转义

Markdown 允许你使用反斜杠转义来生成字面意义的字符，否则这些字符在 Markdown 的格式语法中具有特殊含义。

代码：

    \*字面意义上的星号\*

预览：

---

\*字面意义上的星号\*

---

Markdown 为以下字符提供反斜杠转义：

代码：

    \   反斜杠
    `   反引号
    *   星号
    _   下划线
    {}  花括号
    []  方括号
    ()  括号
    #   井号
    +   加号
    -   减号（连字符）
    .   英文句点
    !   感叹号

## 行内 HTML

对于 Markdown 语法未涵盖的任何标记，你只需直接使用 HTML 即可。无需特别声明或界定即可从 Markdown 切换到 HTML；只需直接使用标签。

代码：

    这是一个普通段落。

    <table>
        <tr>
            <td>Foo</td>
        </tr>
    </table>

    这是另一个普通段落。

预览：

---

这是一个普通段落。

<table>
    <tr>
        <td>Foo</td>
    </tr>
</table>

这是另一个普通段落。

---

请注意，Markdown 格式语法在**块级 HTML 标签内不会被处理**。

与块级 HTML 标签不同，Markdown 语法在**行内级标签内会被处理**。

代码：

    <span>**生效**</span>

    <div>
        **不生效**
    </div>

预览：

---

<span>**生效**</span>

<div>
  **不生效**
</div>
