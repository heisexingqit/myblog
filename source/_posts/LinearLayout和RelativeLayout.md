---
title: LinearLayout和RelativeLayout简述
date: 2023-04-12 00:00:00
categories: android
tags: [android, layout]
description: 线性布局和相对布局的个人理解
cover: https://md-pic-1300959784.cos.ap-nanjing.myqcloud.com/img/202303220934950.jpg
comments: false
---

# LinearLayout

`特点：单层平面，普遍用于包裹多个控件，可嵌套`

**优点**

- 理解和使用简单
- weight自适应填充空白

缺点

- 图层不能相互覆盖

## 用途

`LinearLayout` 的单图层特点，结合 `weight` 属性可以快速根据页面结构进行设计。

下面举几个例子：

1. 在**登录输入框**设计中，使用 `LinearLayout` 作为**外框**，内部可添加 `EditText` 和 `ImageView` 等诸多组件。

   ![image-20230412095202466](https://md-pic-1300959784.cos.ap-nanjing.myqcloud.com/img/202304151128185.png)

   如上图所示，在 `EditText` 左右加入许多自定义图标，并用LinearLayout包裹，这是一种常见的设计方式。为了提升用户体验，`LinearLayout` 也可以作为**点击事件的载体**。

2. 在WebView这类自带点击事件的组件中，除了**JS进行交互**外。还可以通过**外部包裹一个LinearLayout**，同时重载 `dispatchTouchEvent` 方法关闭WebView本身的点击效果，最终实现WebView的整体点击效果（`实际是穿过WebView层点击到LinearLayout）`

3. 在较为复杂的布局中，可以通过多重嵌套，并设置不同的 `orientation` 来进行设计，例如下面的电影列表item设计：

​		<img src="https://md-pic-1300959784.cos.ap-nanjing.myqcloud.com/img/202304151128186.png" alt="image-20230412100758861" style="zoom:50%;" />

# RelativeLayout

`特点：定位准确，可以设计多图层覆盖`

**优点：**

- 可以实现更加准确的定位
- 可以**多图层覆盖**

**缺点：**

- 设计约束较为复杂

## 用途

`RelativeLayout` 弥补了 `LinearLayout` 的单图层特点，可以**多图层覆盖悬浮效果**。常见于翻页按钮，加载遮蔽板等，这些有多图层的要求。

RelativeLayout的图层遮蔽关系是 `从上到下，下面的组件遮蔽上面的`

下面举几个例子：

1. 为了提升用户体验，通常会设计 `加载遮蔽` 页面，通过一个布局将整个或者部分页面遮蔽住，此时需要考虑**多图层**的效果，因此用 `RelativeLayout` 较为合适，例如：

   - 非遮蔽的加载圈：![image-20230412101318763](https://md-pic-1300959784.cos.ap-nanjing.myqcloud.com/img/202304151128187.png)
   - 半透明的遮蔽加载圈：<img src="https://md-pic-1300959784.cos.ap-nanjing.myqcloud.com/img/202304151128189.png" alt="image-20230412101734489" style="zoom: 80%;" />

   **注意，遮蔽页面需要设置 `可点击` 否则是能够穿过点击到下方组件的*

2. 常用的翻页按钮，悬浮与页面两侧，也要用 `RelativeLayout` 进行设置，例如：

   <img src="https://md-pic-1300959784.cos.ap-nanjing.myqcloud.com/img/202304151128190.png" alt="image-20230412102039880" style="zoom:80%;" />

# 总结

​		在使用过程中，还有其他许多布局能够选择，但是这两种最为基础。通常来讲，整体根布局为 `RelativeLayout` ，这样就可以进行**多图层**的设置，而 `LinearLayout` 则用来制作其中的各种**组件块**。

