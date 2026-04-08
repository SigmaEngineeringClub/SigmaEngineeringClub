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
{% if category contains "kptakahashi/blog" %}
<article>
    {% capture category_name %}{{ category | first}}{% endcapture %}
    <h3 id="tag.{{ category_name }}">BLOG</h3>
    <ul>
        {% for post in site.categories[category_name] %}
        <li>{{ post.date | date : "%F" }}: <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a> {{ site.author }}</li>
        {% endfor %}
    </ul>
</article>
{% endif %}
{% endfor %}

{% for author in site.authors %}
<article>
    <h3 id="author.{{ author_name }}">{{ author }}</h3>
    <ul>
        {% for post in site.author[author] %}
        <li>{{ post.date | date : "%F" }}: <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
        {% endfor %}
    </ul>
</article>
{% endfor %}

<ul>
  {% for author in site.authors %}
    <li>
      <h2>{{ author.name }}</h2>
      <h3>{{ author.position }}</h3>
      <p>{{ author.content | markdownify }}</p>
    </li>
  {% endfor %}
</ul>