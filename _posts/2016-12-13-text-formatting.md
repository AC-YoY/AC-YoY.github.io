---
layout: post
title: "文本样式"
date: 2016-12-13 20:23:00
description: 文本样式
tags: text
share: false
---

# 着重色(Accent colors)

着重色主要用在一些比较重要的元素上，比如像是链接，按钮，图标等。目前在使用的着重色是<span class="label" style="background-color:#3CA2A2; color:#444444">#3CA2A2</span>。在theme.scss中还有一些其他的预定义颜色，就在文件开头`$accent-color`处，例如<span class="label" style="background-color:#C38FD6; color:#444444">#C38FD6</span>, <span class="label" style="background-color:#8FD6B3; color:#444444">#8FD6B3</span>, <span class="label" style="background-color:#35B4DE; color:#444444">#35B4DE</span>, <span class="label" style="background-color:#D2E354; color:#444444">#D2E354</span>, <span class="label" style="background-color:#52B54B; color:#444444">#52B54B</span>。你也可以直接试试效果（把鼠标移动上去试试看！）

<script>
  $('.label').hover(function(){
    var color = $(this).text();
    [].forEach.call($('a'), function(item) {
      item.style.color = color
    })
  })
</script>

<style>
  .label{
    cursor: default;
  }
</style>

# 文本样式示例

这是一些正常大小的文本。

# 一号标题

## 二号标题

### 三号标题

#### 四号标题

##### 五号标题

# 着重标记（Emphasis）

斜体： `*asterisks*` -> *asterisks* 或 `_underscores_` -> _underscores_

加粗： `**asterisks**` -> **asterisks** 或 `___underscores___` -> ___underscores___

你乐意也可以组合使用

# 引用和记号（blockquotes & notes）

{% highlight bash %}
> Blockquotes

{% endhighlight bash %}

也可以将引用的前面的记号换成其他的

{% highlight bash %}
>Note
{: .note}

{% endhighlight bash %}

>Note
{: .note}

{% highlight bash %}
>Warning
{: .note .warning}

{% endhighlight bash %}

>Warning
{: .note .warning}

# 键盘按键

如果你想表示一组快捷键怎么办？
{% highlight bash %}
`Ctrl`{: .key} + `A`{:.key}
{% endhighlight bash %}

使用`Ctrl`{: .key} + `A`{: .key}可以全选哦
