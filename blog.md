---
layout: page
title: Blog
permalink: /blog/
---

Textos sobre estudos, trabalho, leituras e outros interesses, do mais recente ao mais antigo.

<ul class="post-list">
  {% for post in site.posts %}
  <li>
    <time class="post-meta" datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: '%d/%m/%Y' }}</time>
    <h2><a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></h2>
  </li>
  {% endfor %}
</ul>

[Acompanhe por RSS]({{ '/feed.xml' | relative_url }}).
