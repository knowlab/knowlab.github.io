---
layout: page
title: Publications
permalink: /publications/
--- 
### selected publications
<div class="selectedPub">
{% for post in site.categories.selected limit:3%}
{{post.excerpt}}
{% endfor %}
</div>

### recent publications (2017 ~)
{% for post in site.categories.paper %}

{% capture this_year %}{{ post.date | date: "%Y" }}{% endcapture %}

{% assign prev = post %}
{% for p in site.categories.paper %}
   {% if p.title == post.title %}
    {% break %}
   {% endif %}   
   {% assign prev = p %}
{% endfor %}
{% capture next_year %}{{ prev.date | date: "%Y" }}{% endcapture %}

{% if forloop.first %}
### {{this_year}} 
{% endif %}

{% if forloop.last %}

{% else %}
   {% if this_year != next_year %}
### {{this_year}}
   {% endif %}
{% endif %}
- {{post.content}}
{% endfor %}


