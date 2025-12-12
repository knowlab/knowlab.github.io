---
layout: default
home: true
---

{% include_relative info.md %}

<div class="h_title">Latest news | <a href="/updates/">all updates</a></div>


<ul class="grid-list">
{% for post in site.categories.news limit:6%}

{% capture this_year %}{{ post.date | date: "%Y" }}{% endcapture %}
{% capture next_year %}{{ post.previous.date | date: "%Y" }}{% endcapture %}



<li markdown="1"> ({{ post.date | date: "%-d %B %Y"}}) {% if post.related_image %}
  <img src="{{post.related_image}}" width="700px" style="filter: drop-shadow(0.35rem 0.35rem 0.4rem rgba(0, 0, 0, 0.3)); margin-bottom:20px"/>
  {% endif %}  {{ post.title }} {% if post.categories contains 'events'%}
  <a href="{{ post.url }}">Event Details</a>
  {% endif %} 
</li>
{% if forloop.last %}

{% else %}
    {% if this_year != next_year %}
### {{next_year}}
    {% endif %}
{% endif %}
{% endfor %}

</ul>
<div style="color: #999999;margin:60px 0 20px 0;font-style: italic;text-align: center;font-size: 90%">Acknowledgement: Logo designed by Yuchen Wu</div>
