---
layout: default
title: 予算と用途で選ぶ｜楽天市場の人気商品と価格の動き
description: お歳暮・クリスマスケーキ・おせち・ふるさと納税・ギフトを、予算と用途ごとに一覧にしました。価格と記録開始からの最安値を毎日更新しています。
permalink: /erabu/
---
# 予算と用途で選ぶ

{% include pr.html %}

楽天市場の商品を、予算と用途ごとに一覧にしています。価格と、記録を始めてからの最安値を毎日更新しています。

{% assign groups = site.data.shelf_index | where_exp: "e", "e.active == true" | group_by: "group" %}
{% assign shown = 0 %}
{% for g in groups %}{% if g.items.size > 0 %}{% assign shown = shown | plus: 1 %}

<h2>{{ g.name | escape }}</h2>

<ul class="post-list">
{% for e in g.items %}<li><span class="date">更新 {{ e.updated | escape }}／{{ e.count | escape }}件</span><a href="{{ '/erabu/' | append: e.shelf_id | append: '/' | relative_url | escape }}">{{ e.label | escape }}</a></li>
{% endfor %}</ul>

{% endif %}{% endfor %}
{% if shown == 0 %}

一覧は準備中です。

{% endif %}
