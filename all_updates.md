---
layout: default
title: all updates
permalink: /updates/
---

{% for post in site.categories.news%}

{% capture this_year %}{{ post.date | date: "%Y" }}{% endcapture %}
{% capture next_year %}{{ post.previous.date | date: "%Y" }}{% endcapture %}

{% if forloop.first %}
### All updates along the years
### {{this_year}}
{% endif %}

- ({{ post.date | date: "%-d %B %Y"}}) {{ post.title }}

{% if forloop.last %}

{% else %}
    {% if this_year != next_year %}
### {{next_year}}
    {% endif %}
{% endif %}
{% endfor %}