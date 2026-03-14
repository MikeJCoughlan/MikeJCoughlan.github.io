---
layout: default
title: Blog
---

[Home](/) | [Projects](/projects) | [Blog](/blog) | [Publications](/#selected-publications) | [Contact](/#contact)

# Blog

I also write on Substack at [coughlanm.substack.com](https://coughlanm.substack.com).

{% for post in site.posts %}
- [{{ post.title }}]({{ post.url }}) — {{ post.date | date: "%B %d, %Y" }}
{% endfor %}
