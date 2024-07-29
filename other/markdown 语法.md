# 简介
官方教程：https://markdown.com.cn/basic-syntax/

Markdown是一种纯文本格式的标记语言。通过简单的标记语法，它可以使普通文本内容具有一定的格式。

相比WYSIWYG编辑器

**优点：** 1、因为是纯文本，所以只要支持Markdown的地方都能获得一样的编辑效果，可以让作者摆脱排版的困扰，专心写作。 2、操作简单。比如\:WYSIWYG编辑时标记个标题，先选中内容，再点击导航栏的标题按钮，选择几级标题。要三个步骤。而Markdown只需要在标题内容前加#即可

**缺点：** 1、需要记一些语法（当然，是很简单。五分钟学会）。 2、有些平台不支持Markdown编辑模式。

# 1. 标题

在想要设置为标题的文字前面加#来表示 一个#是一级标题，二个#是二级标题，以此类推。支持六级标题。

注：标准语法一般在#后跟个空格再写文字，貌似简书不加空格也行。

示例：

```Shell
# 这是一级标题
## 这是二级标题
### 这是三级标题
#### 这是四级标题
##### 这是五级标题
###### 这是六级标题
```

效果如下：

# 这是一级标题

## 这是二级标题

### 这是三级标题

#### 这是四级标题

##### 这是五级标题

###### 这是六级标题

# 2. 字体
* 加粗：用两个\*或\_包围文本
例：`**文本**` 效果：**文本**

* 斜体：用一个\*或\_包围文本
例：`*文本*` 效果：*文本*

* 斜体加粗：用三个\*或\_包围文本
例：`***文本***` 效果：___文本___

* 删除线：用两个\~\~号包围文本
例：`~~文本~~` 效果：~~文本~~

* 下划线：Markdown自身没有实现下划线，但它是HTML的子集，实现了\<u\>标签
例：`<u>文本</u>` 效果：<u>文本</u>

* 高亮：CommonMark中并未定义普通文本高亮。可通过HTML标签\<mark\>实现：
例：`<mark>文本</mark>` 效果：<mark>文本</mark>

* 上标：用一个\^包围文本
例：`文本^上标^` 效果：文本^上标^

* 下标：用一个\~包围文本
例：`文本~下标~` 效果：文本~下标~

* 小号字体：`<small>小号字体</small>` 效果：<small>小号字体</small>
* 大号字体：`<big>大号字体</big>` 效果：<big>大号字体</big>

示例
```
**这是加粗效果**
*这是斜体效果*
***这是斜体加粗***
~~这是删除线效果~~
<u>这是下划线效果</u>
<mark>这是高亮效果</mark>
```
效果：

**这是加粗效果**
*这是斜体效果*
***这是斜体加粗***
~~这是删除线效果~~
<u>这是下划线效果</u>
<mark>这是高亮效果</mark>

# 3. 引用

在引用的文字前加>即可。引用也可以嵌套，如加两个>>三个>>> n个... 貌似可以一直加下去，但没神马卵用

示例：

```Shell
>这是引用的内容
>>这是引用的内容
>>>>>>>>>>这是引用的内容
```

效果如下：

>这是引用的内容
>>这是引用的内容
>>>>>>>>>>这是引用的内容

# 4. 列表

### 无序列表

语法： 无序列表用 - + \* 任何一种都可以

```Markdown
- 列表内容
+ 列表内容
* 列表内容

注意：- + * 跟内容之间都要有一个空格
```

效果如下：

*   列表内容

*   列表内容

*   列表内容

### 有序列表

语法： 数字加点

```Markdown
1. 列表内容
2. 列表内容
3. 列表内容

注意：序号跟内容之间要有空格
```

效果如下：

1.  列表内容

2.  列表内容

3.  列表内容

### 可选列表

    [ ] 未勾选状态
    [x] 勾选状态

效果如下：

*   [ ] 未勾选状态
*   [x] 勾选状态

### 列表嵌套

**上一级和下一级之间敲三个空格即可**

*   一级无序列表内容

    *   二级无序列表内容

    *   二级无序列表内容

    *   二级无序列表内容

*   一级无序列表内容

    1.  二级有序列表内容

    2.  二级有序列表内容

    3.  二级有序列表内容

1.  一级有序列表内容

    *   二级无序列表内容

    *   二级无序列表内容

    *   二级无序列表内容

2.  一级有序列表内容

    1.  二级有序列表内容

    2.  二级有序列表内容

    3.  二级有序列表内容


# 5. 分割线

三个或者三个以上的 - 或者 \* 都可以。

示例：

```YAML
---
----
***
*****
```

效果如下： 可以看到，显示效果是一样的。

---
----
***
*****

![https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/0647aedc24f64dafb375492c71a6a41b\~tplv-k3u1fbpfcp-zoom-in-crop-mark:1512:0:0:0.awebp](https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/0647aedc24f64dafb375492c71a6a41b\~tplv-k3u1fbpfcp-zoom-in-crop-mark:1512:0:0:0.awebp)

# 6. 图片
图床：[github + vscode + picgo](https://blog.csdn.net/qq_44314954/article/details/122951033)

语法：

```
![图片alt](图片地址 ''图片title'')

图片alt就是显示在图片下面的文字，相当于对图片内容的解释。
图片title是图片的标题，当鼠标移到图片上时显示的内容。title可加可不加
```

示例：

```
![test.png](https://s2.loli.net/2024/07/23/jEGc2keoyUaOMd5.png "测试")
```

效果如下：

![test.png](https://s2.loli.net/2024/07/23/jEGc2keoyUaOMd5.png "测试")

使用本地图片示例
```
![测试图片](../images/test.jpg)
![本地图片](本地图片地址)

// 点击图片跳转链接
[![测试图片](../images/test.jpg)](https://baidu.com)
```

![测试图片](../images/test.jpg)

[![测试图片](../images/test.jpg)](https://baidu.com)

**上传本地图片直接点击导航栏的图片标志，选择图片即可**

markdown格式追求的是简单、多平台统一。那么图片的存储就是一个问题，需要用图床，提供统一的外链，这样就不用在不同的平台去处理图片的问题了。才能做到书写一次，各处使用。 关于图床的选择我写了一篇文章，对网上存在的各种方法做了总结，需要的朋友可以看看。[markdown图床](https://link.juejin.cn?target=https%3A%2F%2Fwww.jianshu.com%2Fp%2Fea1eb11db63f)

# 7. 超链接

语法：

```LESS
[超链接名](超链接地址 "超链接title")
title可加可不加
```

示例：

```LESS
[百度](http://baidu.com)
```

效果如下：

[百度](http://baidu.com)

注：Markdown本身语法不支持链接在新页面中打开，貌似简书做了处理，是可以的。别的平台可能就不行了，如果想要在新页面中打开的话可以用html语言的a标签代替。

```Properties
<a href="超链接地址" target="_blank">超链接名</a>

示例
<a href="https://www.jianshu.com/u/1f5ac0cf6a8b" target="_blank">简书</a>
```
### 禁用自动URL链接
如果您不希望自动链接URL，则可以通过将URL表示为带反引号的代码来删除该链接。
```
`http://www.example.com`
```

呈现的输出如下所示：
`http://www.example.com`


# 8. 表格

语法：

```diff
表头|表头|表头
---|:--:|---:
内容|内容|内容
内容|内容|内容

第二行分割表头和内容。
- 有一个就行，为了对齐，多加了几个
文字默认居左
-两边加：表示文字居中
-右边加：表示文字居右
注：原生的语法两边都要用 | 包起来。此处省略
```

示例：

```diff
姓名|技能|排行
--|:--:|--:
刘备|哭|大哥
关羽|打|二哥
张飞|骂|三弟
```

效果如下：

姓名|技能|排行
--|:--:|--:
刘备|哭|大哥
关羽|打|二哥
张飞|骂|三弟

![https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/1061ed202571411399f2af731f856881\~tplv-k3u1fbpfcp-zoom-in-crop-mark:1512:0:0:0.awebp](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/1061ed202571411399f2af731f856881\~tplv-k3u1fbpfcp-zoom-in-crop-mark:1512:0:0:0.awebp)

# 9. 代码

语法： 单行代码：代码之间分别用一个反引号(`)包起来

代码块：代码之间分别用三个反引号包起来，且两边的反引号单独占一行
> 注：为了防止转译，前后三个反引号处加了小括号，实际是没有的。这里只是用来演示，实际中去掉两边小括号即可。

示例：

单行代码

```Go
`create database hero;`
```

代码块

````Kotlin
(```)
    function fun(){
         echo "这是一句非常牛逼的代码";
    }
    fun();
(```)
````

效果如下：

单行代码：`create database hero;`

代码块

```
function fun(){
  echo "这是一句非常牛逼的代码";
}
fun();
```

# 10. 流程图

````Properties
```flow
st=>start: 开始
op=>operation: My Operation
cond=>condition: Yes or No?
e=>end
st->op->cond
cond(yes)->e
cond(no)->op
```
````

效果如下： 简书不支持流程图，所以截了个图

![https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/eb4970178a2f46d9bf70f99c34f4f50b\~tplv-k3u1fbpfcp-zoom-in-crop-mark:1512:0:0:0.awebp](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/eb4970178a2f46d9bf70f99c34f4f50b\~tplv-k3u1fbpfcp-zoom-in-crop-mark:1512:0:0:0.awebp)

流程图.png

# 11. 上下标

实现下标与上标的三种方法：

方法1（符号）：
```
下标 ：θ~1~ 
上标 ：θ^2^
```
结果如下：
下标 ：θ~1~ 
上标 ：θ^2^

方法2（HTML标签）：
```
下标 ：θ<sub>1</sub>
上标 ：θ<sup>2</sup>
```

结果如下：
下标 ：θ<sub>1</sub>
上标 ：θ<sup>2</sup>

方法3（公式块）：
```
$$
下标 ：θ_1 ，上标 ：θ^2
$$
```


公式：θ~1~x~1~+θ~2~x~2~^2^+θ~3~x~3~^3^
写法：
```
θ~1~x~1~+θ~2~x~2~^2^+θ~3~x~3~^3^
```

# 12. 数学公式
https://blog.csdn.net/wzk4869/article/details/126863936

行内公式使用方法，比如这个化学公式：$\ce{Hg^2+ ->[I-] HgI2 ->[I-] [Hg^{II}I4]^2-}$

块公式使用方法如下：
$$H(D_2) = -\left(\frac{2}{4}\log_2 \frac{2}{4} + \frac{2}{4}\log_2 \frac{2}{4}\right) = 1$$

矩阵：
```
$$
  \begin{pmatrix}
  1 & a_1 & a_1^2 & \cdots & a_1^n \\
  1 & a_2 & a_2^2 & \cdots & a_2^n \\
  \vdots & \vdots & \vdots & \ddots & \vdots \\
  1 & a_m & a_m^2 & \cdots & a_m^n \\
  \end{pmatrix}
$$
```

# 13. 注音
注音符号，用法如下：

Markdown Nice 这么好用，简直是{喜大普奔|hē hē hē hē}呀！

# 14. 使用 Emoji 表情
有两种方法可以将表情符号添加到Markdown文件中：将表情符号复制并粘贴到Markdown格式的文本中，或者键入emoji shortcodes。

### 复制和粘贴表情符号
在大多数情况下，您可以简单地从Emojipedia 等来源复制表情符号并将其粘贴到文档中。许多Markdown应用程序会自动以Markdown格式的文本显示表情符号。从Markdown应用程序导出的HTML和PDF文件应显示表情符号。

Tip: 如果您使用的是静态网站生成器，请确保将HTML页面编码为UTF-8。.
### 使用表情符号简码
一些Markdown应用程序允许您通过键入表情符号短代码来插入表情符号。这些以冒号开头和结尾，并包含表情符号的名称。

去露营了！ :tent: 很快回来。

真好笑！ :joy:
呈现的输出如下所示：

去露营了！⛺很快回来。

真好笑！😂

Note: 注意：您可以使用此表情符号简码列表，但请记住，表情符号简码因应用程序而异。有关更多信息，请参阅Markdown应用程序的文档。


# 脚注
示例：
```
Here's a simple footnote,[^1] and here's a longer one.[^bignote]

[^1]: This is the first footnote.

[^bignote]: Here's one with multiple paragraphs and code.

    Indent paragraphs to include them in the footnote.

    `{ my code }`

    Add as many paragraphs as you like.
```

效果如下：
Here's a simple footnote,[^1] and here's a longer one.[^bignote]

[^1]: This is the first footnote.

[^bignote]: Here's one with multiple paragraphs and code.

    Indent paragraphs to include them in the footnote.

    `{ my code }`

    Add as many paragraphs as you like.
