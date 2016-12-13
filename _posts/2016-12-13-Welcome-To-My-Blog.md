---
layout: post
title: "Welcome To My Blog"
date: 2016-12-13 16:36:00
description: 终于有了自己的小屋
tags: Hello
share: true
---

# Welcome
我要尽量保证blog的更新

## 基本功能测试
由于`jekyll`用到了`YAML Front Matter`，必须熟悉它的语法

```
### 关于图片（静态资源的使用）
+ 使用整个图片
![My helpful screenshot]({{ site.baseurl | prepend:site.url}}/images/dice_layout.png){:
.center-image }*骰子布局图*[原链接](https://ac-yoy.github.io/FrontEndProjects/Layout/dice/diceLayout.html)
+ 行内图片
![Battery Widget]({{ site.url | append:site.baseurl }}/images/batWid1.png)
