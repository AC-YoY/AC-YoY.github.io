---
layout: post
title: "Text formatting"
date: 2015-11-02 16:25:06
tags: jekyll
description: Text formatting examples.
---

# Accent colors

Accent color is color for some important elements, such as links, buttons, icons. Currently accent color is <span class="label" style="background-color:#3CA2A2; color:#444444">#3CA2A2</span>. This theme has some more predefined colors available in **theme.scss**, under variable `$accent-color` in the beginning of the file, such as <span class="label" style="background-color:#C38FD6; color:#444444">#C38FD6</span>, <span class="label" style="background-color:#8FD6B3; color:#444444">#8FD6B3</span>, <span class="label" style="background-color:#35B4DE; color:#444444">#35B4DE</span>, <span class="label" style="background-color:#D2E354; color:#444444">#D2E354</span>, <span class="label" style="background-color:#52B54B; color:#444444">#52B54B</span>. You can use one of them (just hover over the label to see accent color in action) or define your own!

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

# Text formating example

Some examples of text formating for some common text elements.

# Headers

# Header1

## Header2

### Header3

#### Header4

# Emphasis

Italics: `*asterisks*` -> *asterisks* or `_underscores_` -> _underscores_.

Bold: `**asterisks**` -> **asterisks** or `__underscores__` -> __underscores__.

You also can combine them: `**asterisks and _underscores_**` -> **asterisks and _underscores_**.

# Blockquotes and notes

{% highlight bash %}
>Blockquotes
{% endhighlight bash %}

>Blockquotes

Using very cool [feature](http://kramdown.gettalong.org/quickref.html#block-attributes) of kramdown which allows to assign any attribute to a block-level element I've added note and warning:

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

# Keyboard buttons

In case you need to show some keyboard shortcuts, like `Ctrl`{: .key}+`A`{:.key} use following construction:

{% highlight bash %}
`Ctrl`{: .key}+`A`{:.key}
{% endhighlight bash %}

Example of keyboard shortcut in terminal:

`Ctrl`{: .key} + `A`{: .key} = Move cursor to beginning of line
`Ctrl`{: .key} + `E`{: .key} = Move cursor to end of line
`Ctrl`{: .key} + `C`{: .key} = kills the current process.
`Ctrl`{: .key} + `Z`{: .key} = sends the current process to the background.
`Ctrl`{: .key} + `D`{: .key} = logs you out.
`Ctrl`{: .key} + `R`{: .key} = finds the last command matching the entered letters.