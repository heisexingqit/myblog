---
title: 在PopupWindow控件中使用ListView点击失效
date: 2023-03-24 15:50:02
tags: [android, bug]
categories: android
description: 一个来源于代码复制的坑
cover: https://md-pic-1300959784.cos.ap-nanjing.myqcloud.com/img/202303220934051.jpg
comments: false
---

# 在PopupWindow控件中使用ListView点击失效

## 场景还原

`PopupWindow` 是一个常用控件，我通常用来 {% label 弹出选择列表 blue %}

在前面的开发中通常是写一个 {% label 固定的 green%} 含多个 `TextView` 控件的 `LinearLayout` 布局，并且分别设置 每个 `TextView` 的点击事件

这次的需求需要动态更新弹出框选项列表，因此就加了一个 `ListView` ，准备用 `ArrayAdapter` 来实现， {% label 布局用系统自带的 orange %} 

<img src="https://md-pic-1300959784.cos.ap-nanjing.myqcloud.com/img/202303241727272.png" alt="系统自带layout" style="zoom: 67%;" />

由于是系统自带的布局，因此跟之前设计 {% label 不统一 red %}，之前设计的如下：

<img src="https://md-pic-1300959784.cos.ap-nanjing.myqcloud.com/img/202303241727273.png" alt="之前的固定样式" style="zoom:67%;" />

索性就新建了一个 `Layout` 布局，复制了之前的 `TextView` 组件，{% label 样式问题解决了 red %} 。

<img src="https://md-pic-1300959784.cos.ap-nanjing.myqcloud.com/img/202303241727274.png" alt="自定义layout" style="zoom:67%;" />

结果噩梦开始，在加上 `setOnItemClickListener` 后，点击Item失效了......

## 尝试方法

1. 开始以为是 `onItemClick` 里面的事件出现了问题，尝试把事件改为 `Toast` ，最终确定是点击事件未触发。

2. 网络搜索，能搜索到相似帖子，说点击事件被组件吸收，但是尝试了 {% label 都没用 orange %} ……
3. 以为是 `PopupWindow` 控件的Bug问题，因此开始在布局上进行 {% label 各种乱尝试 blue%} 。
4. 在 {% label 浪费了好长时间 purple%} 后，终于选择了最麻烦的Debug方法。
5. 新建一个 `TestActivity` 测试无 `PopupWindow` 组件，能否正常运行。
   - 能的话就是  `PopupWindow` 的问题
   - 不能的话就是 `Layout` 的问题


## 解决方法

最终发现，在新建的 `TestActivity` 中依然无法触发点击。这下心凉半截，直接对准 `ItemLayout` 进行测试，发现是给TextView设置了 **可点击**，如下：

```xml
android:clickable="true"
android:focusable="true"
```

这组属性使得 `TextView` 把点击事件吸收了， **{% label 去掉就ok了 blue %}** ，但是在之前的 `View` 中，这个设置必须加上才能 `TextView` 设置点击事件。

## 反思

分析问题 **{% label 过于急躁 red %}** ，浪费了太多时间。如果能一早能 **{% label 冷静分析 green %}**  ，用 **{% label 最正确 green %}** 的Debug方式，就不会白费那么长时间了。

