---
layout: page
title: Tags
description: 哈哈，你找到了我的文章基因库
keywords: 分类
comments: false
menu: 分类
permalink: /tags/
---

<section class="container posts-content">
{% assign sorted_tags = site.tags | sort %}
{% for tag in sorted_tags %}
<h3 id="{{ tag[0] }}">{{ tag | first | replace: "-"," " }}</h3>
<ol class="posts-list">
{% for post in tag.last %}
<li class="posts-list-item">
<a class="posts-list-name" href="{{ site.url }}{{ post.url }}">{{ post.title }}</a>
<span class="posts-list-meta">{{ post.date | date:"%Y-%m-%d" }}</span>
</li>
{% endfor %}
</ol>
{% endfor %}
</section>
<!-- /section.content -->
