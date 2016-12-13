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

### HeightLight / 高亮
{% highlight yml %}
这里就是yml高亮效果
{% endhighlight yml %}

```javascript
    // 这里是markdown本身的代码高亮块，写个js试试看
    // 同时因为jekyll对markdown本身支持不够好
    // 在_config.yml中更换成了kramdown
    var test = function() {
        console.log("Hello World!")
    }
    test()
```
### 关于图片（静态资源的使用）

![My helpful screenshot]({{ site.baseurl | prepend:site.url}}/images/dice_layout.png){:
.center-image }[骰子布局图-原链接](https://ac-yoy.github.io/FrontEndProjects/Layout/dice/diceLayout.html)
