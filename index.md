---
layout: default
title: 首页
---

## 🐾 最新日记

{% for post in site.posts limit:10 %}
### [{{ post.title }}]({{ post.url }})
*{{ post.date | date: "%Y年%m月%d日" }}*

{{ post.excerpt | strip_html | truncatewords: 40 }}

---
{% endfor %}
