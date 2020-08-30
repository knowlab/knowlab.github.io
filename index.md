---
layout: default
home: true
---

{% include_relative info.md %}

{% for post in site.categories.news limit:3%}

{% capture this_year %}{{ post.date | date: "%Y" }}{% endcapture %}
{% capture next_year %}{{ post.previous.date | date: "%Y" }}{% endcapture %}

{% if forloop.first %}
### Latest 3 pieces of news | [all updates](/updates/)
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

### Collaborators
- Prof Richard Dobson, KCL
