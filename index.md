---
layout: default
title: スイーツ侍の楽天経済圏ノート
---
# スイーツ侍の楽天経済圏ノート

スイーツ侍の漫画で、楽天のお得と選び方をやさしく整理するブログです。

## 記事一覧
<ul class="post-list">
{% for post in site.posts %}
<li><span class="date">{{ post.date | date: "%Y.%m.%d" }}</span><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>
