---
title: kptakahashi
description: ポートフォリオとか
layout: libdoc/page
unlisted: true
permalink: /Members/kptakahashi

Category: Members
order: 100
---

ふふふ

{% for category in site.categories %}
<article>
    {% capture category_name %}{{ category | first}}{% endcapture %}
    <h3 id="tag.{{ category_name }}">{{ category_name }}</h3>
    <ul>
        {% for post in site.categories[category_name] %}
        <li>{{ post.date }}: <a href="{{ post.url }}">{{ post.title }}</a></li>
        {% endfor %}
    </ul>
</article>
{% endfor %}
