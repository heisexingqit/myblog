---
title: Android开发中Dialog填充满父容器
date: 2023-04-10 00:00:00
categories: android
tags: [android, dialog]
description: Dialog无法填充满父容器Debug
cover: https://md-pic-1300959784.cos.ap-nanjing.myqcloud.com/img/202303220934951.jpg
comments: false
---

在`Android原生开发`中，通常会使用**自定义的Dailog**来设计二级面板，其自带一个`黑色半透明`的遮蔽效果。但是想要将**`Dialog`填充满父容器**，是需要一些**尝试**的。

## 环境介绍

自定义`Dialog`类，加载自定义布局`layout`并进行数据绑定，同时创建**接口**进行信息传递。

其中 **布局的根容器** 相关属性如下： 

```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="@color/photo_editor_white"
    android:orientation="vertical"
    android:padding="20dp">
    ...
</LinearLayout>
```

由于主`Activity`背景为**黑色**，因此设置`Dialog`背景为**白色**，同时有一定的内边距。

## 默认情况

默认代码就是

```java
MyDialog mydialog = new MyDialog(this);
drawDialog.getWindow().setGravity(Gravity.BOTTOM);//从底部弹出
mydialog.show();
```

通常来说弹出框的**大小跟布局文件根容器属性无关**，虽然根容器设置了`match_parent`但是实际上默认尺寸是`wrap_content`，也就是说**根据实际的容器内组件大小**来确定。下图是空组件的效果：

<img src="https://md-pic-1300959784.cos.ap-nanjing.myqcloud.com/img/202304151128182.png" alt="image-20230410192650267" style="zoom:50%;" />

**横向可变，纵向有一个底边距*

## 布局设置

通过Java代码设置其**横向实际宽度**为`match_parent`，只需加上下面两句即可。

```java
Window window = drawDialog.getWindow();
window.setLayout(ViewGroup.LayoutParams.MATCH_PARENT, ViewGroup.LayoutParams.WRAP_CONTENT);
```

效果如下：

<img src="https://md-pic-1300959784.cos.ap-nanjing.myqcloud.com/img/202304151128183.png" alt="image-20230410193025768" style="zoom:50%;" />

**横向有一个左右边距，纵向有一个底边距*

## 背景设置

之后尝试了很多方法，最后发现只需要加上

```java
Window window = drawDialog.getWindow()
window.setBackgroundDrawableResource(android.R.color.transparent);
```

即可，效果如下：

<img src="https://md-pic-1300959784.cos.ap-nanjing.myqcloud.com/img/202304151128184.png" alt="image-20230410193620628" style="zoom:50%;" />

**左右填满，底边距消除*

## 备注

`window.setBackgroundDrawableResource(android.R.color.transparent);`是设计容器背景颜色为透明色，其实里面随便填一种颜色都能实现同样的效果，比如 `window.setBackgroundDrawableResource(android.R.color.black);`等。