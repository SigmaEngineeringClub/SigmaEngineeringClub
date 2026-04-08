---
description: >- # this means to ignore newlines until "baseurl:"
  総（シグマで）工（エンジニアリングが好きな有志が）会（集まる社内サークル）
layout: libdoc/page
permalink: index.html # To avoid: Warning: Empty `slug` generated for '/'.
unlisted: true
---

<ul>
  {% for author in site.authors %}
    <li>
      <h2>{{ author.name }}</h2>
      <h3>{{ author.position }}</h3>
      <p>{{ author.content | markdownify }}</p>
    </li>
  {% endfor %}
</ul>
