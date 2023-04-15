---
title: cmd批量修改文件后缀名
date: 2023-04-11 00:00:00
categories: other
tags: [cmd]
description: 一句命令批量修改文件后缀
cover: https://md-pic-1300959784.cos.ap-nanjing.myqcloud.com/img/202303220934939.jpg
comments: false
---

> 直接使用`Windows命令符`实现递归子文件夹修改所有文件后缀名

# 方法

1. 通过文件管理器打开目标文件夹，在地址栏输入`cmd`，回车 `enter` 弹出命令行输入窗口，如下图：

   <img src="https://md-pic-1300959784.cos.ap-nanjing.myqcloud.com/img/202304151129620.png" alt="image-20230411181152344" style="zoom:67%;" />

   <img src="https://md-pic-1300959784.cos.ap-nanjing.myqcloud.com/img/202304151129621.png" alt="image-20230411190004743" style="zoom:67%;" />

   *空白处右键点击 `在终端打开` powershell不行，**必须是cmd**

2. 这里分两种情况：

   - `不递归子文件夹`，仅修改本文件夹的所有文件后缀名（默认为7z）

     ```cmd
     ren * *.7z
     ```

   - `递归子文件夹`，修改文件夹的所有文件后缀名（默认为7z）

     ```cmd
     for /r . %f in (*) do ren "%f" *.7z
     ```

3. 完成

# 备注

删除指定后缀名的文件，指令为 `for /r . %f in (*.7z) do del "%f"`

删除包含 `str` 的文件名文件，指令为 `for /r . %f in (*str*) do del "%f"`

`删除不包含文件夹`
