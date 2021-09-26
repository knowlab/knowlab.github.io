---
layout: page
title: Articles
permalink: /blog/
--- 
{% for post in site.categories.blog %}


[{{post.title}}]({{post.url}})
<div class="excerpt">{{ post.excerpt }}
{% assign minutes = post.content | number_of_words | divided_by: 180 %}
<span class="blog-meta">by {{ post.author.name }} on {{ post.date | date: '%b %d, %Y' }}. {{minutes}} min read.
</span>
</div>

{% endfor %}


