---
layout: default
home: true
---

{% include_relative info.md %}

<div class="h_title">Latest news | <a href="/updates/">all updates</a></div>
<h2 style="color: #bf5d3c;text-align: center">We are hiring: <a href="/vacancies">Research Fellow in Clinical Text Analytics</a></h2> 
{% for post in site.categories.news limit:5%}

{% capture this_year %}{{ post.date | date: "%Y" }}{% endcapture %}
{% capture next_year %}{{ post.previous.date | date: "%Y" }}{% endcapture %}

{% if forloop.first %}
### {{this_year}}
{% endif %}

- ({{ post.date | date: "%-d %B %Y"}}) {% if post.related_image %}
  <img src="{{post.related_image}}" width="500px" style="filter: drop-shadow(0.35rem 0.35rem 0.4rem rgba(0, 0, 0, 0.3)); margin-bottom:20px"/>
  {% endif %}  {{ post.title }} {% if post.categories contains 'events'%}
  <a href="{{ post.url }}">Event Details</a>
  {% endif %} 
{% if forloop.last %}

{% else %}
    {% if this_year != next_year %}
### {{next_year}}
    {% endif %}
{% endif %}
{% endfor %}


<div class="h_title">Latest blog articles | <a href="/blog">all articles</a></div>
{% for post in site.categories.blog limit:2%}
[{{post.title}}]({{post.url}})
<div class="excerpt">{{ post.excerpt }}
{% assign minutes = post.content | number_of_words | divided_by: 180 %}
<span class="blog-meta">by {{ post.author.name }} on {{ post.date | date: '%b %d, %Y' }}. {{minutes}} min read.
</span>
</div>
{% endfor %}
<div style="color: #999999;margin:60px 0 20px 0;font-style: italic;text-align: center;font-size: 90%">Acknowledgement: Logo designed by Yuchen Wu</div>
