---
layout: post
title: "social icons"
date: 2016-12-13 23:20:00
description: 需要用图标？除了常见的几个社交用按键，还有更多可供选择
tags: icon
share: false
---

# 图标

现在使用中的一些图标：
<ul class="social-media">
  <li>
    <a title="Github"
      href="https://github.com/{{ site.social.github }}"
      target="_blank"><i class="fa fa-github fa-2x"></i></a>
  </li>
  <li>
    <a title="StackOverflow"
      href="http://stackoverflow.com/users/1252056/{{ site.social.stackoverflow }}"
      target="_blank"><i class="fa fa-stack-overflow fa-2x"></i></a>
  </li>
  <li>
    <a title="LinkedIn"
      href="https://www.linkedin.com/in/{{ site.social.linkedin }}"
      target="_blank"><i class="fa fa-linkedin fa-2x"></i></a>
  </li>
  <li>
    <a title="Instagram"
      href="https://instagram.com/{{ site.social.instagram }}"
      target="_blank"><i class="fa fa-instagram fa-2x"></i></a>
  </li>
  <li>
    <a title="Last.fm"
      href="http://lastfm.com/user/{{ site.social.lastfm }}"
      target="_blank"><i class="fa fa-lastfm fa-2x"></i></a>
  </li>
  <li>
    <a title="RSS"
      href="{{site.url}}/{{ site.social.rss }}"
      target="_blank"><i class="fa fa-rss fa-2x"></i></a>
  </li>
</ul>

## 需要一个新的图标？

- 在这儿找一个好用的图标: [Font Awesome Icons](https://fortawesome.github.io/Font-Awesome/icons/)
- 添加到 `_config.yml`中去
- 在 `social.html` 文件中添加代码来检查图标是否存在 :

{% highlight html %}
{% raw %}
 {% if site.social.variable %}
  <li>
    <a title="{{ site.social.<your_social_variable> }}"
       href="{{site.url}}/{{ site.social.<your_social_variable> }}"
       target="_blank"><font_awesome_icon></i></a>
  </li>
{% endif %}
{% endraw %}
{% endhighlight html %}
