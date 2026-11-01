---
layout: default
title: Articles
permalink: /articles/
---
<div id="articles"><h1>Articles</h1>{% if site.posts.size == 0 %}<p>Stories coming soon.</p>{% else %}<ul class="posts noList">{% for post in site.posts %}<li><span class="date">{{ post.date | date_to_string }}</span><h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3><p class="description">{{ post.description | default: post.excerpt | strip_html | strip_newlines | truncate: 160 }}</p></li>{% endfor %}</ul>{% endif %}</div>