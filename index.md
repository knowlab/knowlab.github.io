---
layout: default
home: true
---

{% include_relative info.md %}

<hr/>
## Latest news | [all updates](/updates/)
{% for post in site.categories.news limit:3%}

{% capture this_year %}{{ post.date | date: "%Y" }}{% endcapture %}
{% capture next_year %}{{ post.previous.date | date: "%Y" }}{% endcapture %}

{% if forloop.first %}
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

<div style="color: #999999;margin:60px 0 20px 0;font-style: italic;text-align: center;font-size: 90%">Acknowledgement: Logo designed by Yuchen Wu</div>
