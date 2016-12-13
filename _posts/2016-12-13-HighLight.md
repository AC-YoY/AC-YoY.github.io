---
layout: post
title: "Welcome To My Blog"
date: 2016-12-13 23:03:00
description: 关于blog中的高亮效果
tags: HighLight
share: false
---

# HihtLight / 高亮
## YAML 语法的几个高亮效果
YML:
{% highlight yml %}
// 注释！？
基本yml高亮效果
{% endhighlight yml %}

XML(使用linenos指令可以给代码块添加行号):
{% highlight xml linenos %}
{% raw %}
<?xml version="1.0" encoding="UTF-8"?>
<rss version="2.0" xmlns:atom="http://www.w3.org/2005/Atom">
    <channel>
    <title>{{ site.name }}</title>
    <description>{{ site.description }}</description>
    <link>{{site.baseurl | prepend:site.url}}</link>
    <atom:link href="{{site.baseurl | prepend:site.url}}/feed.xml" rel="self" type="application/rss+xml" />
    {% for post in site.posts limit:10 %}
        <item>
        <title>{{ post.title }}</title>
        <description>{{ post.content | xml_escape }}</description>
        <pubDate>{{ post.date | date: "%a, %d %b %Y %H:%M:%S %z" }}</pubDate>
        <link>{{post.url | prepend:site.baseurl | prepend:site.url}}</link>
        <guid isPermaLink="true">{{post.url | prepend:site.baseurl | prepend:site.url}}</guid>
        </item>
    {% endfor %}
    </channel>
</rss>
{% endraw %}
{% endhighlight xml %}

JSON:
{% highlight json %}
{"employees":[
    {"firstName":"John", "lastName":"Doe"},
    {"firstName":"Anna", "lastName":"Smith"},
    {"firstName":"Peter", "lastName":"Jones"}
]}
{% endhighlight json %}

SQL:
{% highlight SQL %}
select count(*) as cm_content_nodes
from alf_node nd, alf_qname qn, alf_namespace ns
where qn.ns_id = ns.id
    and nd.type_qname_id = qn.id
    and ns.uri = 'http://www.alfresco.org/model/content/1.0'
    and qn.local_name = 'content';
{% endhighlight SQL %}

Jawa:
{% highlight java %}
private String getToken(HttpClient client) throws UnsupportedEncodingException{
    Cookie[] cookies = client.getState().getCookies();
    for (Cookie cookie : cookies){
        if (cookie.getName().equals("Alfresco-CSRFToken") {
          return URLDecoder.decode(cookie.getValue(), "UTF-8");
        }
    }
    return null;
}
{% endhighlight java %}

## MarkDown语法的高亮

```javascript
    // 这里是markdown本身的代码高亮块，写个js试试看
    // 同时因为jekyll对markdown本身支持不够好
    // 在_config.yml中更换成了kramdown
    var test = function() {
        console.log("Hello World!")
    }
    test()
```

```json
{"employees":[
    {"firstName":"John", "lastName":"Doe"},
    {"firstName":"Anna", "lastName":"Smith"},
    {"firstName":"Peter", "lastName":"Jones"}
]}
```

```sql
select count(*) as cm_content_nodes
from alf_node nd, alf_qname qn, alf_namespace ns
where qn.ns_id = ns.id
    and nd.type_qname_id = qn.id
    and ns.uri = 'http://www.alfresco.org/model/content/1.0'
    and qn.local_name = 'content';
```

```java
private String getToken(HttpClient client) throws UnsupportedEncodingException{
    Cookie[] cookies = client.getState().getCookies();
    for (Cookie cookie : cookies){
        if (cookie.getName().equals("Alfresco-CSRFToken") {
          return URLDecoder.decode(cookie.getValue(), "UTF-8");
        }
    }
    return null;
}
```
