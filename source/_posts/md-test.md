---
title: 页面样式测试
date: 2023-03-18 15:09:01
tags: [markdown, blog, butterfly]
categories: blog
description: 对于Markdown基础样式 和 Beautiful自带外挂标签样式 进行汇总和测试页面。
cover: https://md-pic-1300959784.cos.ap-nanjing.myqcloud.com/img/202303181756744.jpeg
comments: false
---

# Markdown基本样式

## 标题

```markdown
# H1
## H2
### H3
#### H4
##### H5
###### H6
```


## 强调

{% tabs %}
<!-- tab 代码 -->

```markdown
Emphasis, aka italics, with *asterisks* or _underscores_.

Strong emphasis, aka bold, with **asterisks** or __underscores__.

Combined emphasis with **asterisks and _underscores_**.

Strikethrough uses two tildes. ~~Scratch this.~~
```

<!-- endtab -->

<!-- tab 效果 -->

Emphasis, aka italics, with *asterisks* or _underscores_.

Strong emphasis, aka bold, with **asterisks** or __underscores__.

Combined emphasis with **asterisks and _underscores_**.

Strikethrough uses two tildes. ~~Scratch this.~~

<!-- endtab -->

{% endtabs %}



## 列表

{% tabs %}
<!-- tab 代码 -->

```markdown
1. 项目1
	1. 项目1.1
2. 项目2 
3. 项目3
	1. 项目3.1
	
- 项目a
- 项目b
- 项目c
	- 项目d

- [ ] 任务1 
- [ ] 任务2
- [x] 任务3 
```

<!-- endtab -->

<!-- tab 效果 -->

1. 项目1
   1. 项目1.1
2. 项目2 
3. 项目3
   1. 项目3.1

- 项目a
- 项目b
- 项目c
  - 项目d
- [ ] 任务1 
- [ ] 任务2
- [x] 任务3 

<!-- endtab -->

{% endtabs %}



## 内联HTML

{% tabs %}
<!-- tab 代码 -->

```markdown
<p>To reboot your computer, press <kbd>ctrl</kbd>+<kbd>alt</kbd>+<kbd>del</kbd>.</p>
```

<!-- endtab -->

<!-- tab 效果 -->


<p>To reboot your computer, press <kbd>ctrl</kbd>+<kbd>alt</kbd>+<kbd>del</kbd>.</p>

<!-- endtab -->

{% endtabs %}



## 脚注和链接

{% tabs %}
<!-- tab 代码 -->

```markdown
正文[^脚注1]

复用少时：[百度](https://www.baidu.com/ "搜索引擎")

复用多时：[百度][id]，[百度][id]，[百度][id]

正文链接：[跳转到一级标题](#一级标题)

[^脚注1]: 测试脚注
[id]: www.baidu.com "搜索引擎"
```

<!-- endtab -->

<!-- tab 效果 -->

正文[^脚注1]

复用少时：[百度](https://www.baidu.com/ "搜索引擎")

复用多时：[百度][id]，[百度][id]，[百度][id]

正文链接：[跳转到一级标题](#一级标题)

[^脚注1]: 测试脚注

[id]: www.baidu.com "搜索引擎"

<!-- endtab -->

{% endtabs %}



## 图片

{% tabs %}
<!-- tab 代码 -->

```markdown
常用

![alt text](https://hexo.io/icon/favicon-196x196.png "Logo Title Text 1")

复用多时

![alt text][logo]

[logo]: https://hexo.io/icon/favicon-196x196.png "Logo Title Text 2"
```

<!-- endtab -->

<!-- tab 效果 -->

常用

![alt text](https://hexo.io/icon/favicon-196x196.png "Logo Title Text 1")

复用多时

![alt text][logo]

[logo]: https://hexo.io/icon/favicon-196x196.png "Logo Title Text 2"

<!-- endtab -->

{% endtabs %}



## 代码块

Inline `code` has `back-ticks around` it.

```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```

```python
s = "Python syntax highlighting"
print s
```

```plaintext
No language indicated, so no syntax highlighting.
But let's throw in a <b>tag</b>.
```



## 表格

{% tabs %}
<!-- tab 代码1 -->

```markdown
|                |ASCII                          |HTML                         |
|----------------|-------------------------------|-----------------------------|
|Single backticks|`'Isn't this fun?'`            |'Isn't this fun?'            |
|Quotes          |`"Isn't this fun?"`            |"Isn't this fun?"            |
|Dashes          |`-- is en-dash, --- is em-dash`|-- is en-dash, --- is em-dash|
```
<!-- endtab -->

<!-- tab 效果1 -->


|                  | ASCII                           | HTML                          |
| ---------------- | ------------------------------- | ----------------------------- |
| Single backticks | `'Isn't this fun?'`             | 'Isn't this fun?'             |
| Quotes           | `"Isn't this fun?"`             | "Isn't this fun?"             |
| Dashes           | `-- is en-dash, --- is em-dash` | -- is en-dash, --- is em-dash |

<!-- endtab -->

<!-- tab 代码2 -->

冒号用来对其列

```markdown
| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned |  |
| col 2 is      | centered      |    |
| zebra stripes | are neat      |   
```
<!-- endtab -->

<!-- tab 效果2 -->

| Tables        |      Are      | Cool |
| ------------- | :-----------: | ---: |
| col 3 is      | right-aligned |      |
| col 2 is      |   centered    |      |
| zebra stripes |   are neat    |      |

<!-- endtab -->

<!-- tab 代码3 -->

外侧|可以删除，同时可以用内联Markdown样式

```markdown
Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3
```
<!-- endtab -->

<!-- tab 效果3 -->

| Markdown | Less      | Pretty     |
| -------- | --------- | ---------- |
| *Still*  | `renders` | **nicely** |
| 1        | 2         | 3          |

<!-- endtab -->

{% endtabs %}



## 块引用

> Blockquotes are very handy in email to emulate reply text.
>
> This line is part of the same quote.

长句引用

> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can put Markdown into a blockquote.

---

## 水平线

{% tabs %}
<!-- tab 代码 -->

共三种

```markdown
---

Hyphens

***

Asterisks

___

Underscores
```
<!-- endtab -->

<!-- tab 效果 -->

Hyphens

***

Asterisks

___

Underscores

---

<!-- endtab -->

{% endtabs %}



## 换行

{% tabs %}
<!-- tab 代码 -->

```markdown
Here's a line for us to start with.

This line is separated from the one above by two newlines, so it will be a *separate paragraph*.

This line is also a separate paragraph, but...
This line is only separated by a single newline, so it's a separate line in the *same paragraph*.
```

<!-- endtab -->

<!-- tab 效果 -->

Here's a line for us to start with.

This line is separated from the one above by two newlines, so it will be a *separate paragraph*.

This line is also a separate paragraph, but...
This line is only separated by a single newline, so it's a separate line in the *same paragraph*.

<!-- endtab -->

{% endtabs %}



##  视频

在b站视频下面**点击分享**，嵌入代码，直接就是**html**的代码块，粘贴可用。



<div align="center">
    <iframe src="//player.bilibili.com/player.html?aid=327623069&bvid=BV1JA411h7Gw&cid=171385214&page=1&autoplay=false" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"></iframe>
</div>
**用div包裹 `align="center"` 居中；*

**在 url 中 加入 autoplay=false，防止自动播放。*

## 公式

公式块

$$
x\frac{\partial f}{\partial x} = 2\sqrt{a}x
$$

内联公式 $\theta=x^2$


$$
\left\{
\begin{array}{ll}
K_{1}=z_{k},&L_{1}=f(x_{k},y_{k},z_{k}),\\
K_{2}=z_{k}+\frac{h}{2}L_{1},&L_{2}=f\left(x_{k}+\frac{h}{2},y_{k}+\frac{h}{2}K_{1},z_{k}+\frac{h}{2}h_{1}\right),\\
K_{3}=z_{k}+\frac{h}{2}L_{2},&L_{3}=f\left(x_{k}+\frac{h}{2},y_{k}+\frac{h}{2}K_{2},z_{k}+\frac{h}{2}L_{2}\right),\\
K_{4}=z_{k}+hL_{3},&L_{4}=f\left(x_{k}+h,y_{k}+hK_{3},z_{k}+hL_{3}
\right).\\
\end{array}
\right.
\tag{4}
$$


## 其他

<u>下划线</u>

:happy:**（失效）**

 🥳 **（直接是字符）**

$a_a$ **（\$a_a\$）**

H~2~0 **（失效）**

X^2^**（失效）**

==文字高亮== **（失效）**

# 外挂标签 (*)

## Note(Bootstrap Callout)

{% tabs %}

<!-- tab 用法1 -->

```markdown
{% note [class] [no-icon] [style] %}
Any content (support inline tags too.io).
{% endnote %}
```

- class：	【可选】标识，不同的标识有不同的配色（ default / primary / success / info / warning / danger ）
- no-icon：【可选】不显示 icon
- style：【可选】可以覆盖配置中的 style（simple/modern/flat/disabled）

<!-- endtab -->

<!-- tab 代码1 -->

```markdown
{% note simple %}
默认 提示块标签
{% endnote %}

{% note default simple %}
default 提示块标签
{% endnote %}

{% note primary simple %}
primary 提示块标签
{% endnote %}

{% note success simple %}
success 提示块标签
{% endnote %}

{% note info simple %}
info 提示块标签
{% endnote %}

{% note warning simple %}
warning 提示块标签
{% endnote %}

{% note danger simple %}
danger 提示块标签
{% endnote %}
```

<!-- endtab -->

<!-- tab 效果1 -->

{% note simple %}
默认 提示块标签
{% endnote %}

{% note default simple %}
default 提示块标签
{% endnote %}

{% note primary simple %}
primary 提示块标签
{% endnote %}

{% note success simple %}
success 提示块标签
{% endnote %}

{% note info simple %}
info 提示块标签
{% endnote %}

{% note warning simple %}
warning 提示块标签
{% endnote %}

{% note danger simple %}
danger 提示块标签
{% endnote %}

<!-- endtab -->

<!-- tab 用法2 -->

```markdown
{% note [color] [icon] [style] %}
Any content (support inline tags too.io).
{% endnote %}
```

- color：【可选】顔色(default / blue / pink / red / purple / orange / green)
- icon：【可选】可配置自定义 icon (只支持 fontawesome 图标, 也可以配置 no-icon )
- style：【可选】可以覆盖配置中的 style（simple/modern/flat/disabled）

<!-- endtab -->

<!-- tab 代码2 -->

```markdown
{% note 'fab fa-cc-visa' simple %}
你是刷 Visa 还是 UnionPay
{% endnote %}
{% note blue 'fas fa-bullhorn' simple %}
2021年快到了....
{% endnote %}
{% note pink 'fas fa-car-crash' simple %}
小心开车 安全至上
{% endnote %}
{% note red 'fas fa-fan' simple%}
这是三片呢？还是四片？
{% endnote %}
{% note orange 'fas fa-battery-half' simple %}
你是刷 Visa 还是 UnionPay
{% endnote %}
{% note purple 'far fa-hand-scissors' simple %}
剪刀石头布
{% endnote %}
{% note green 'fab fa-internet-explorer' simple %}
前端最讨厌的浏览器
{% endnote %}
```

<!-- endtab -->

<!-- tab 效果2 -->

{% note 'fab fa-cc-visa' simple %}
你是刷 Visa 还是 UnionPay
{% endnote %}
{% note blue 'fas fa-bullhorn' simple %}
2021年快到了....
{% endnote %}
{% note pink 'fas fa-car-crash' simple %}
小心开车 安全至上
{% endnote %}
{% note red 'fas fa-fan' simple%}
这是三片呢？还是四片？
{% endnote %}
{% note orange 'fas fa-battery-half' simple %}
你是刷 Visa 还是 UnionPay
{% endnote %}
{% note purple 'far fa-hand-scissors' simple %}
剪刀石头布
{% endnote %}
{% note green 'fab fa-internet-explorer' simple %}
前端最讨厌的浏览器
{% endnote %}

<!-- endtab -->

{% endtabs %}



## 隐藏文本

{% tabs %}

<!-- tab 内联用法 -->

```markdown
{% hideInline content,display,bg,color %}
```

- content: 文本內容
- display: 按钮显示的文字(可选)
- bg: 按钮的背景颜色(可选)
- color: 按钮文字的颜色(可选)

<!-- endtab -->

<!-- tab 内联代码-->

```markdown
哪个英文字母最酷？ {% hideInline 因为西装裤(C装酷),查看答案,#FF7242,#fff %}

门里站着一个人? {% hideInline 闪 %}
```

<!-- endtab -->

<!-- tab 内联效果-->

哪个英文字母最酷？ {% hideInline 因为西装裤(C装酷),查看答案,#FF7242,#fff %}

门里站着一个人? {% hideInline 闪 %}

<!-- endtab -->

<!-- tab 块用法 -->

```markdown
{% hideBlock display,bg,color %}
content
{% endhideBlock %}
```

- content: 文本內容
- display: 按钮显示的文字(可选)
- bg: 按钮的背景颜色(可选)
- color: 按钮文字的颜色(可选)

<!-- endtab -->

<!-- tab 块代码-->

```markdown
查看答案
{% hideBlock 查看答案 %}
傻子，怎么可能有答案
{% endhideBlock %}
```

<!-- endtab -->

<!-- tab 块效果-->

查看答案
{% hideBlock 查看答案 %}
傻子，怎么可能有答案
{% endhideBlock %}

<!-- endtab -->

<!-- tab 大块用法 -->

```markdown
{% hideToggle display,bg,color %}
content
{% endhideToggle %}
```

{% hideToggle display,bg,color %}
content
{% endhideToggle %}

<!-- endtab -->

<!-- tab 大块代码 -->


```markdown
{% hideToggle Butterfly安装方法 %}
在你的博客根目录里

git clone -b master https://github.com/jerryc127/hexo-theme-butterfly.git themes/Butterfly

如果想要安装比较新的dev分支，可以

git clone -b dev https://github.com/jerryc127/hexo-theme-butterfly.git themes/Butterfly

{% endhideToggle %}
```

<!-- endtab -->

<!-- tab 大块效果 -->

{% hideToggle Butterfly安装方法 %}
在你的博客根目录里

git clone -b master https://github.com/jerryc127/hexo-theme-butterfly.git themes/Butterfly

如果想要安装比较新的dev分支，可以

git clone -b dev https://github.com/jerryc127/hexo-theme-butterfly.git themes/Butterfly

{% endhideToggle %}

<!-- endtab -->

{% endtabs %}



## 折叠框

{% tabs %}

<!-- tab 用法 -->

```markdown
{% folding 参数（可选）, 标题 %}
![](https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper/abstract/41F215B9-261F-48B4-80B5-4E86E165259E.jpeg)
{% endfolding %}
```

- 颜色：blue, cyan, green, yellow, red
- 状态：状态填写 open 代表默认打开。

<!-- endtab -->

<!-- tab 代码 -->

```markdown
{% folding 查看图片测试 %}

![](https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper/abstract/41F215B9-261F-48B4-80B5-4E86E165259E.jpeg)

{% endfolding %}

{% folding cyan open, 查看默认打开的折叠框 %}

这是一个默认打开的折叠框。

{% endfolding %}

{% folding green, 查看代码测试 %}
假装这里有代码块（代码块没法嵌套代码块）
{% endfolding %}

{% folding yellow, 查看列表测试 %}

- haha
- hehe

{% endfolding %}

{% folding red, 查看嵌套测试 %}

{% folding blue, 查看嵌套测试2 %}

{% folding 查看嵌套测试3 %}

hahaha <span><img src='https://cdn.jsdelivr.net/gh/volantis-x/cdn-emoji/tieba/%E6%BB%91%E7%A8%BD.png' style='height:24px'></span>

{% endfolding %}

{% endfolding %}

{% endfolding %}
```

<!-- endtab -->

<!-- tab 效果 -->

{% folding 查看图片测试 %}

![](https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper/abstract/41F215B9-261F-48B4-80B5-4E86E165259E.jpeg)

{% endfolding %}

{% folding cyan open, 查看默认打开的折叠框 %}

这是一个默认打开的折叠框。

{% endfolding %}

{% folding green, 查看代码测试 %}
假装这里有代码块（代码块没法嵌套代码块）
{% endfolding %}

{% folding yellow, 查看列表测试 %}

- haha
- hehe

{% endfolding %}

{% folding red, 查看嵌套测试 %}

{% folding blue, 查看嵌套测试2 %}

{% folding 查看嵌套测试3 %}

hahaha <span><img src='https://cdn.jsdelivr.net/gh/volantis-x/cdn-emoji/tieba/%E6%BB%91%E7%A8%BD.png' style='height:24px'></span>

{% endfolding %}

{% endfolding %}

{% endfolding %}

<!-- endtab -->

{% endtabs %}

## Tabs菜单

{% tabs %}

<!-- tab 用法 -->

```markdown
{% tabs Unique name, [index] %}
<!-- tab [Tab caption] [@icon] -->
Any content (support inline tags too).
<!-- endtab -->
{% endtabs %}

Unique name   : Unique name of tabs block tag without comma.
                Will be used in #id's as prefix for each tab with their index numbers.
                If there are whitespaces in name, for generate #id all whitespaces will replaced by dashes.
                Only for current url of post/page must be unique!
[index]       : Index number of active tab.
                If not specified, first tab (1) will be selected.
                If index is -1, no tab will be selected. It's will be something like spoiler.
                Optional parameter.
[Tab caption] : Caption of current tab.
                If not caption specified, unique name with tab index suffix will be used as caption of tab.
                If not caption specified, but specified icon, caption will empty.
                Optional parameter.
[@icon]       : FontAwesome icon name (full-name, look like 'fas fa-font')
                Can be specified with or without space; e.g. 'Tab caption @icon' similar to 'Tab caption@icon'.
                Optional parameter.
```
<!-- endtab -->

<!-- tab 代码 -->

```markdown
{% tabs test1 %}默认第一个， {% tabs test2, 3 %}预选第三个，{% tabs test3, -1 %}不预选
<!-- tab -->
**This is Tab 1.**
<!-- endtab -->

<!-- tab -->
**This is Tab 2.**
<!-- endtab -->

<!-- tab -->
**This is Tab 3.**
<!-- endtab -->
{% endtabs %}
```

<!-- endtab -->

<!-- tab 效果 -->

{% tabs %}
<!-- tab -->
**This is Tab 1.**
<!-- endtab -->

<!-- tab -->
**This is Tab 2.**
<!-- endtab -->

<!-- tab -->
**This is Tab 3.**
<!-- endtab -->

{% endtabs %}

<!-- endtab -->

<!-- tab 图标Tab代码 -->

```markdown
{% tabs test4 %}
<!-- tab 第一个Tab -->
**tab名字为第一个Tab**
<!-- endtab -->

<!-- tab @fab fa-apple-pay -->
**只有图标 没有Tab名字**
<!-- endtab -->

<!-- tab 炸弹@fas fa-bomb -->
**名字+icon**
<!-- endtab -->
{% endtabs %}
```

<!-- endtab -->

<!-- tab 图标Tab效果 -->

{% tabs test4 %}
<!-- tab 第一个Tab -->
**tab名字为第一个Tab**
<!-- endtab -->

<!-- tab @fab fa-apple-pay -->
**只有图标 没有Tab名字**
<!-- endtab -->

<!-- tab 炸弹@fas fa-bomb -->
**名字+icon**
<!-- endtab -->
{% endtabs %}

<!-- endtab -->

{% endtabs %}

## Button

{% tabs %}
<!-- tab 用法-->

```markdown
{% btn [url],[text],[icon],[color] [style] [layout] [position] [size] %}

[url]         : 链接
[text]        : 按钮文字
[icon]        : [可选] 图标
[color]       : [可选] 按钮背景顔色(默认style时）
                      按钮字体和边框顔色(outline时)
                      default/blue/pink/red/purple/orange/green
[style]       : [可选] 按钮样式 默认实心
                      outline/留空
[layout]      : [可选] 按钮佈局 默认为line
                      block/留空
[position]    : [可选] 按钮位置 前提是设置了layout为block 默认为左边
                      center/right/留空
[size]        : [可选] 按钮大小
                      larger/留空
```

<!-- endtab -->

<!-- tab 代码 -->


```markdown
This is my website, click the button {% btn 'https://butterfly.js.org/',Butterfly %}
This is my website, click the button {% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right %}
This is my website, click the button {% btn 'https://butterfly.js.org/',Butterfly,,outline %}
This is my website, click the button {% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline %}
This is my website, click the button {% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,larger %}
```

<!-- endtab -->

<!-- tab 效果 -->

This is my website, click the button {% btn 'https://butterfly.js.org/',Butterfly %}
This is my website, click the button {% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right %}
This is my website, click the button {% btn 'https://butterfly.js.org/',Butterfly,,outline %}
This is my website, click the button {% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline %}
This is my website, click the button {% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,larger %}

<!-- endtab -->

<!-- tab 代码2 -->

```markdown
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,block %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,block center larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,block right outline larger %}
```

<!-- endtab -->

<!-- tab 效果2 -->

{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,block %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,block center larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,block right outline larger %}

<!-- endtab -->

<!-- tab 代码3 -->

**一行多个**

```markdown
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,blue larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,pink larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,red larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,purple larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,orange larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,green larger %}
```

<!-- endtab -->

<!-- tab 效果3 -->

{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,blue larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,pink larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,red larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,purple larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,orange larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,green larger %}

<!-- endtab -->

<!-- tab 代码4 -->

```markdown
<div class="btn-center">
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline blue larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline pink larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline red larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline purple larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline orange larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline green larger %}
</div>
```
<!-- endtab -->

<!-- tab 效果4 -->

<div class="btn-center">
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline blue larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline pink larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline red larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline purple larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline orange larger %}
{% btn 'https://butterfly.js.org/',Butterfly,far fa-hand-point-right,outline green larger %}
</div>
<!-- endtab -->

{% endtabs %}



## 内联Img

{% tabs %}
<!-- tab 用法-->

```markdown
{% inlineImg [src] [height] %}

[src]      :    图片链接
[height]   ：   图片高度限制【可选】
```
<!-- endtab -->

<!-- tab 代码 -->

```markdown
你看我长得漂亮不

![](https://i.loli.net/2021/03/19/2P6ivUGsdaEXSFI.png)

我觉得很漂亮 {% inlineImg https://i.loli.net/2021/03/19/5M4jUB3ynq7ePgw.png 150px %}
```

<!-- endtab -->

<!-- tab 效果 -->

你看我长得漂亮不

![](https://i.loli.net/2021/03/19/2P6ivUGsdaEXSFI.png)

我觉得很漂亮 {% inlineImg https://i.loli.net/2021/03/19/5M4jUB3ynq7ePgw.png 150px %}

<!-- endtab -->

{% endtabs %}



## 文本背景色

{% tabs %}
<!-- tab 用法-->

```markdown
{% label text color %}
```

<!-- endtab -->

<!-- tab 代码 -->

```markdown
臣亮言：{% label 先帝 %}创业未半，而{% label 中道崩殂 blue %}。今天下三分，{% label 益州疲敝 pink %}，此诚{% label 危急存亡之秋 red %}也！然侍衞之臣，不懈于内；{% label 忠志之士 purple %}，忘身于外者，盖追先帝之殊遇，欲报之于陛下也。诚宜开张圣听，以光先帝遗德，恢弘志士之气；不宜妄自菲薄，引喻失义，以塞忠谏之路也。
宫中、府中，俱为一体；陟罚臧否，不宜异同。若有{% label 作奸 orange %}、{% label 犯科 green %}，及为忠善者，宜付有司，论其刑赏，以昭陛下平明之治；不宜偏私，使内外异法也。
```

<!-- endtab -->

<!-- tab 效果 -->

臣亮言：{% label 先帝 %}创业未半，而{% label 中道崩殂 blue %}。今天下三分，{% label 益州疲敝 pink %}，此诚{% label 危急存亡之秋 red %}也！然侍衞之臣，不懈于内；{% label 忠志之士 purple %}，忘身于外者，盖追先帝之殊遇，欲报之于陛下也。诚宜开张圣听，以光先帝遗德，恢弘志士之气；不宜妄自菲薄，引喻失义，以塞忠谏之路也。
宫中、府中，俱为一体；陟罚臧否，不宜异同。若有{% label 作奸 orange %}、{% label 犯科 green %}，及为忠善者，宜付有司，论其刑赏，以昭陛下平明之治；不宜偏私，使内外异法也。

<!-- endtab -->

{% endtabs %}



## 时间线

{% tabs %}
<!-- tab 用法-->

```markdown
{% timeline title,color %}
<!-- timeline title -->
xxxxx
<!-- endtimeline -->
<!-- timeline title -->
xxxxx
<!-- endtimeline -->
{% endtimeline %}

color：
default(留空) / blue / pink / red / purple / orange / green
```

<!-- endtab -->

<!-- tab 代码 -->

```markdown
{% timeline 2022 %}
<!-- timeline 01-02 -->
这是测试页面
<!-- endtimeline -->
{% endtimeline %}
```

<!-- endtab -->

<!-- tab 效果 -->

{% timeline 2022 %}
<!-- timeline 01-02 -->
这是测试页面
<!-- endtimeline -->
{% endtimeline %}

<!-- endtab -->

{% endtabs %}



## 友情链接

{% tabs %}
<!-- tab 用法-->

```markdown
{% flink %}
xxxxxx
{% endflink %}
```

<!-- endtab -->

<!-- tab 代码 -->

```markdown
{% flink %}
- class_name: 友情链接
  class_desc: 那些人，那些事
  link_list:
    - name: JerryC
      link: https://jerryc.me/
      avatar: https://jerryc.me/img/avatar.png
      descr: 今日事,今日毕
    - name: Hexo
      link: https://hexo.io/zh-tw/
      avatar: https://d33wubrfki0l68.cloudfront.net/6657ba50e702d84afb32fe846bed54fba1a77add/827ae/logo.svg
      descr: 快速、简单且强大的网志框架

- class_name: 网站
  class_desc: 值得推荐的网站
  link_list:
    - name: Youtube
      link: https://www.youtube.com/
      avatar: https://i.loli.net/2020/05/14/9ZkGg8v3azHJfM1.png
      descr: 视频网站
    - name: Weibo
      link: https://www.weibo.com/
      avatar: https://i.loli.net/2020/05/14/TLJBum386vcnI1P.png
      descr: 中国最大社交分享平台
    - name: Twitter
      link: https://twitter.com/
      avatar: https://i.loli.net/2020/05/14/5VyHPQqR6LWF39a.png
      descr: 社交分享平台
{% endflink %}
```

<!-- endtab -->

<!-- tab 效果 -->

{% flink %}

- class_name: 友情链接
  class_desc: 那些人，那些事
  link_list:
    - name: JerryC
      link: https://jerryc.me/
      avatar: https://jerryc.me/img/avatar.png
      descr: 今日事,今日毕
    - name: Hexo
      link: https://hexo.io/zh-tw/
      avatar: https://d33wubrfki0l68.cloudfront.net/6657ba50e702d84afb32fe846bed54fba1a77add/827ae/logo.svg
      descr: 快速、简单且强大的网志框架

- class_name: 网站
  class_desc: 值得推荐的网站
  link_list:
    - name: Youtube
      link: https://www.youtube.com/
      avatar: https://i.loli.net/2020/05/14/9ZkGg8v3azHJfM1.png
      descr: 视频网站
    - name: Weibo
      link: https://www.weibo.com/
      avatar: https://i.loli.net/2020/05/14/TLJBum386vcnI1P.png
      descr: 中国最大社交分享平台
    - name: Twitter
      link: https://twitter.com/
      avatar: https://i.loli.net/2020/05/14/5VyHPQqR6LWF39a.png
      descr: 社交分享平台

{% endflink %}

<!-- endtab -->

{% endtabs %}
